# Makefile for AmigaOS 4
 
SRC= BStream.cpp byte_swapping.cpp csalerts_sdl.cpp cscluts_sdl.cpp \
csdialogs_sdl.cpp csmisc_sdl.cpp cspaths_sdl.cpp csstrings.cpp FilmProfile.cpp \
mytm_sdl.cpp

OBJ=$(SRC:.cpp=.o)

libcseries.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a
