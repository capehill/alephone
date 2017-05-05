# Makefile for AmigaOS 4
 
CPP_SRC= Movie.cpp

C_SRC= #SDL_ffmpeg.c

OBJ=$(CPP_SRC:.cpp=.o) $(C_SRC:.c=.o)

libffmpeg.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

%.o:%.c
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a

