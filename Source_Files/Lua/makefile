# Makefile for AmigaOS 4

C_SRC= lapi.c lauxlib.c lbaselib.c lbitlib.c lcode.c lctype.c ldblib.c ldebug.c \
ldo.c ldump.c lfunc.c lgc.c linit.c liolib.c llex.c lmathlib.c lmem.c lobject.c \
lopcodes.c loslib.c lparser.c lstate.c lstring.c lstrlib.c ltable.c ltablib.c    \
ltm.c lundump.c lvm.c lzio.c

CPP_SRC= lua_hud_objects.cpp lua_hud_script.cpp lua_map.cpp lua_monsters.cpp \
lua_objects.cpp lua_player.cpp lua_projectiles.cpp lua_saved_objects.cpp      \
lua_script.cpp lua_serialize.cpp

OBJ=$(C_SRC:.c=.o) $(CPP_SRC:.cpp=.o)

liblua.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

%.o:%.c
	gcc $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a