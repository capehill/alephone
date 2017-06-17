# Makefile for AmigaOS 4

HEADERS=-I../XML -I../TCPMess -I../Sound -I../RenderOther -I../RenderMain -I../Network -I../Network/Metaserver -I../ModelView -I../Misc -I../Lua \
-I../LibNAT -I../Input -I../GameWorld -I../Files -I../FFmpeg -I../Expat -I../CSeries -I.. \
-I/SDK/local/newlib/include/SDL2 \
-I/CODE/ports/boost_1_54_0

HEADER_PATHS=XML TCPMess Sound RenderOther RenderMain Network Network/Metaserver ModelView \
Misc Lua LibNAT Input GameWorld Files FFmpeg Expat CSeries .

HP2=$(addprefix -I, $(HEADER_PATHS))

SRC= shell.cpp shell_misc.cpp

OBJS= $(SRC:.cpp=.o)

DEFINES= -DSDL -DHAVE_OPENGL -DHAVE_LUA -DHAVE_UNISTD_H -DHAVE_MEMMOVE #-D__USE_AMIGAOS_NAMESPACE__ #HAVE_LUA HAVE_SDL_IMAGE

CFLAGS=-O2 -ggdb $(HEADERS) $(DEFINES) -Wall

# This is a bit messy, I'm too lazy to sort out the correct linkage order (if there is one)
LIBS= Sound/libsound.a XML/libxml.a Network/libnetwork.a \
RenderOther/librenderother.a RenderMain/librendermain.a \
ModelView/libmodelview.a Lua/liblua.a Misc/libmisc.a LibNAT/liblibnat.a \
Input/libinput.a GameWorld/libgameworld.a FFmpeg/libffmpeg.a \
Expat/libexpat.a CSeries/libcseries.a TCPMess/libtcpmess.a XML/libxml.a Files/libfiles.a \
RenderOther/librenderother.a

export # pass the variables to submakes

alephone: $(OBJS) libs
	g++ -o $@ $(OBJS) $(LIBS) -lSDL2 -lSDL2_ttf -lSDL2_net -lpthread -lfreetype -lz
	echo done

%.o:%.cpp
	echo $(HP2)
	g++ -o $@ -c $< $(CFLAGS) $(HP2)

libs:
	echo libs
	make -C XML
	make -C TCPMess
	make -C Sound
	make -C RenderOther
	make -C RenderMain
	make -C Network
	make -C ModelView
	make -C Misc
	make -C Lua
	make -C LibNAT
	make -C Input
	make -C GameWorld
	make -C Files
	make -C FFmpeg
	make -C Expat
	make -C CSeries

clean:
	make -C XML clean
	make -C TCPMess clean
	make -C Sound clean
	make -C RenderOther clean
	make -C RenderMain clean
	make -C Network clean
	make -C ModelView clean
	make -C Misc clean
	make -C Lua clean
	make -C LibNAT clean
	make -C Input clean
	make -C GameWorld clean
	make -C Files clean
	make -C FFmpeg clean
	make -C Expat clean
	make -C CSeries clean
	echo cleaned
