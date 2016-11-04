# libGL error: failed to load driver: swrast

This happened during an update.

```
p230198@fwn-biol-132-102:~$ qtcreator
Starting process:  "/usr/bin/cmake" "--help" 
libGL error: failed to load driver: swrast
QOpenGLShader: could not create shader 
QOpenGLShaderProgram: could not create shader program 
QOpenGLShader: could not create shader 
QOpenGLShaderProgram::uniformLocation( imageTexture ): shader program is not linked 
QOpenGLShaderProgram::uniformLocation( imageTexture ): shader program is not linked 
QOpenGLShader: could not create shader 
QOpenGLShaderProgram: could not create shader program 
QOpenGLShader: could not create shader 
QOpenGLShaderProgram::uniformLocation( imageTexture ): shader program is not linked 
QOpenGLShaderProgram::uniformLocation( imageTexture ): shader program is not linked 
QOpenGLShader: could not create shader 
QOpenGLShaderProgram: could not create shader program 
QOpenGLShader: could not create shader 
QOpenGLShaderProgram::uniformLocation( imageTexture ): shader program is not linked 
QOpenGLShaderProgram: could not create shader program 
QOpenGLShader: could not create shader 
Renderer failed shader compilation: 
"" 
Segmentation fault (core dumped)
```


# Solution

Thanks to [this StackOverflow answer](http://stackoverflow.com/a/39604514), I found out the solution:

```
sudo apt-get install nvidia-340 --fix-missing
```
