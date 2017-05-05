# Makefile for AmigaOS 4

SRC= ConnectPool.cpp HTTP.cpp network_capabilities.cpp network.cpp \
network_data_formats.cpp network_dialog_widgets_sdl.cpp network_dialogs.cpp \
network_games.cpp network_lookup_sdl.cpp network_messages.cpp \
network_microphone_shared.cpp network_microphone_sdl_dummy.cpp \
network_speaker_sdl.cpp network_speaker_shared.cpp network_speex.cpp          \
network_star_hub.cpp network_star_spoke.cpp network_udp.cpp \
RingGameProtocol.cpp SDL_netx.cpp SSLP_limited.cpp StarGameProtocol.cpp Update.cpp

MS_SRC= \
Metaserver/metaserver_dialogs.cpp Metaserver/metaserver_messages.cpp \
Metaserver/network_metaserver.cpp Metaserver/SdlMetaserverClientUi.cpp

OBJ=$(SRC:.cpp=.o) $(MS_SRC:.cpp=.o)

libnetwork.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a
