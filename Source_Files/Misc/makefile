# Makefile for AmigaOS 4

SRC= ActionQueues.cpp CircularByteBuffer.cpp Console.cpp DefaultStringSets.cpp \
game_errors.cpp interface.cpp Logging.cpp PlayerImage_sdl.cpp PlayerName.cpp    \
preference_dialogs.cpp preferences.cpp preferences_widgets_sdl.cpp Scenario.cpp  \
sdl_dialogs.cpp sdl_widgets.cpp shared_widgets.cpp Statistics.cpp                 \
thread_priority_sdl_dummy.cpp vbl.cpp

OBJ=$(SRC:.cpp=.o)

libmisc.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a