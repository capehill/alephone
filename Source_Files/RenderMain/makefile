# Makefile for AmigaOS 4

SRC= AnimatedTextures.cpp Crosshairs_SDL.cpp ImageLoader_SDL.cpp \
ImageLoader_Shared.cpp OGL_Faders.cpp OGL_FBO.cpp OGL_Model_Def.cpp \
OGL_Render.cpp OGL_Setup.cpp OGL_Shader.cpp OGL_Subst_Texture_Def.cpp \
OGL_Textures.cpp Rasterizer_Shader.cpp render.cpp RenderPlaceObjs.cpp  \
RenderRasterize.cpp RenderRasterize_Shader.cpp RenderSortPoly.cpp       \
RenderVisTree.cpp scottish_textures.cpp shapes.cpp SW_Texture_Extras.cpp \
textures.cpp

OBJ=$(SRC:.cpp=.o)

librendermain.a: $(OBJ)
	ar -ru $@ $(OBJ)
	ranlib $@

%.o:%.cpp
	g++ $(CFLAGS) -c $< -o $@

clean:
	delete #?.o
	delete #?.a