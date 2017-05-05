# Makefile for AmigaOS 4

SRC= Dim3_Loader.cpp Model3D.cpp ModelRenderer.cpp StudioLoader.cpp \
WavefrontLoader.cpp

OBJ=$(SRC:.cpp=.o)

libmodelview.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a