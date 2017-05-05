# Makefile for AmigaOS 4

SRC= devices.cpp dynamic_limits.cpp effects.cpp flood_map.cpp items.cpp \
lightsource.cpp map_constructors.cpp map.cpp marathon2.cpp media.cpp     \
monsters.cpp pathfinding.cpp physics.cpp placement.cpp platforms.cpp player.cpp \
projectiles.cpp scenery.cpp weapons.cpp world.cpp

OBJ=$(SRC:.cpp=.o)

libgameworld.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a