# Makefile for AmigaOS 4

SRC= ChaseCam.cpp computer_interface.cpp fades.cpp FontHandler.cpp \
game_window.cpp HUDRenderer.cpp HUDRenderer_Lua.cpp HUDRenderer_OGL.cpp \
HUDRenderer_SW.cpp Image_Blitter.cpp images.cpp motion_sensor.cpp        \
OGL_Blitter.cpp OGL_LoadScreen.cpp overhead_map.cpp OverheadMap_OGL.cpp   \
OverheadMap_SDL.cpp OverheadMapRenderer.cpp screen.cpp screen_drawing.cpp  \
sdl_fonts.cpp sdl_resize.cpp Shape_Blitter.cpp TextLayoutHelper.cpp        \
TextStrings.cpp ViewControl.cpp


OBJ=$(SRC:.cpp=.o)

librenderother.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a