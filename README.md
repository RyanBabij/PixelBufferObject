PixelBufferObject
=================

Project forked from Juan Navarro's repo (https://github.com/j1elo/PixelBufferObject). Original credit to Song Ho Ahn (http://www.songho.ca/opengl/gl_pbo.html).

I modified the code to work with FreeGLUT instead of GLUT, and GLEW instead of GLEXT. I also added some RNG to the texture pixel update to increase the load a bit. It seems that on my laptop there is no measurable performance increase using PBO. However it might work on other hardware. I am also using this to test performance increase of glTexSubImage2D instead of binding whole textures.

OpenGL Pixel Buffer Object (PBO) streaming.
