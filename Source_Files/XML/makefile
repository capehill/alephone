# Makefile for AmigaOS 4

SRC=XML_MakeRoot.cpp XML_LevelScript.cpp QuickSave.cpp Plugins.cpp InfoTree.cpp

OBJ=$(SRC:.cpp=.o)

libxml.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a
