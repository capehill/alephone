# Makefile for AmigaOS 4
 
CPP_SRC= AStream.cpp crc.cpp FileHandler.cpp find_files_sdl.cpp \
game_wad.cpp import_definitions.cpp Packing.cpp preprocess_map_sdl.cpp \
preprocess_map_shared.cpp resource_manager.cpp SDL_rwops_ostream.cpp wad.cpp \
wad_prefs.cpp wad_sdl.cpp WadImageCache.cpp

C_SRC= #SDL_rwops_zzip.c


OBJ=$(CPP_SRC:.cpp=.o) $(C_SRC:.c=.o)

libfiles.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

%.o:%.c
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a

