# c++ imgui sdl base project
a simple working sdl/imgui c++ project useful as a base for further graphics projects\
adapted from [this tutorial](https://decovar.dev/blog/2019/05/26/sdl-imgui/)

## setup
### requirements
- SDL2
- OpenGL3
- GLAD
- Dear ImGUI

### pre-build
the following files should be moved from imgui/backends to imgui/:
- imgui_impl_opengl3.cpp
- imgui_impl_opengl3.h
- imgui_impl_opengl3_loader.h
- imgui_impl_sdl.cpp
- imgui_impl_sdl.h
