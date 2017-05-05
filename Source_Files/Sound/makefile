# Makefile for AmigaOS 4

SRC=BasicIFFDecoder.cpp Decoder.cpp FFmpegDecoder.cpp MADDecoder.cpp Mixer.cpp Music.cpp \
ReplacementSounds.cpp SndfileDecoder.cpp SoundFile.cpp SoundManager.cpp VorbisDecoder.cpp

OBJ=$(SRC:.cpp=.o)

libsound.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a