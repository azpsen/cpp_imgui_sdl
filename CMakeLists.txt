cmake_minimum_required(VERSION 3.23)
project(slimulation)

set(CMAKE_CXX_STANDARD 17)

set (sources
        main.cpp
        imgui/imconfig.h
        imgui/imgui.cpp
        imgui/imgui.h
        imgui/imgui_demo.cpp
        imgui/imgui_draw.cpp
        imgui/imgui_internal.h
        imgui/imgui_widgets.cpp
        imgui/imstb_rectpack.h
        imgui/imstb_textedit.h
        imgui/imstb_truetype.h
        imgui/imgui_impl_opengl3.cpp
        imgui/imgui_impl_opengl3.h
        imgui/imgui_impl_sdl.cpp
        imgui/imgui_impl_sdl.h
        )

find_package(OpenGL REQUIRED)
find_package(SDL2 REQUIRED)

add_library("glad" "glad/src/glad.c")

include_directories("glad/include")
include_directories(${SDL2_INCLUDE_DIRS})

add_executable(slimulation main.cpp)

target_link_libraries(${CMAKE_PROJECT_NAME} ${OPENGL_gl_LIBRARY} "glad")
