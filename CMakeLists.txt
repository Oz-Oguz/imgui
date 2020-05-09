cmake_minimum_required(VERSION 3.0)

project(imgui VERSION 4.6 LANGUAGES C)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

#--------------------------------------------------------------------
# Add subdirectories
#--------------------------------------------------------------------
# add_subdirectory(src)
message("imgui::CURRENT_SOURCE_DIR: ${CMAKE_CURRENT_SOURCE_DIR}")

add_library(imgui STATIC
"imconfig.h"
"imgui.h"
"imgui.cpp"
"imgui_draw.cpp"
"imgui_internal.h"
"imgui_widgets.cpp"
"imstb_rectpack.h"
"imstb_textedit.h"
"imstb_truetype.h"
"imgui_demo.cpp" 
)

target_compile_options(imgui PRIVATE -fPIC)

target_include_directories(imgui PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")