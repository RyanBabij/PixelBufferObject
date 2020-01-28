# Pixel Buffer Object

Project forked from Juan Navarro's repo (https://github.com/j1elo/PixelBufferObject). Original credit to Song Ho Ahn (http://www.songho.ca/opengl/gl_pbo.html).

This is some sample code which demonstrates OpenGL's Pixel Buffer Object (PBO) streaming. It is very useful for updating texture data at runtime. One obvious application of this is postprocessing, for example if you want to invert the colours on the screen or something like that. Another application is if you want to render per-pixel output, for example making an emulator where you want to render each pixel exactly as it would appear on the hardware.

I modified the code to work with FreeGLUT instead of GLUT, and GLEW instead of GLEXT. I also added some RNG to the texture pixel update to increase the load a bit. It seems that on my laptop there is no measurable performance increase using PBO. However on my desktop the performance increase is massive, dropping the render update time for a 5012x5012 texture from 50ms to around 0.1ms. There seems to be no measurable performance increase using multiple PBOs. PBO therefore appears to be very useful, but only on modern hardware.

I am also using this to test performance increase of glTexSubImage2D instead of binding whole textures. This seems to work well even on old hardware but I still need to test it properly.

## Issues

For some reason I'm unable to static link GLEW, so I'll bundle the dll in the release.

I've only tested this code on Windows, it will likely require some work to get working on other OSs.

The code throws a lot of warnings which I am not interested in fixing atm.
