# Makefile for AmigaOS 4

SRC=CommunicationsChannel.cpp Message.cpp MessageDispatcher.cpp MessageHandler.cpp MessageInflater.cpp

OBJ=$(SRC:.cpp=.o)

libtcpmess.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a