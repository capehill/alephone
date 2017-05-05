# Makefile for AmigaOS 4

SRC= joystick_sdl.cpp mouse_sdl.cpp


OBJ=$(SRC:.cpp=.o)

libinput.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a