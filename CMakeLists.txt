project(imgui)

set(IMGUI_SRCS)
file(GLOB IMGUI_SRCS	#GLOB_RECURSE
	*.h
	*.cpp
	backends/imgui_impl_glfw.h
	backends/imgui_impl_glfw.cpp
	backends/imgui_impl_opengl3.h
	backends/imgui_impl_opengl3.cpp
	backends/imgui_impl_opengl3_loader.h
    misc/cpp/imgui_stdlib.cpp
)

add_library(imgui STATIC
    ${IMGUI_SRCS}
)

target_include_directories(imgui PRIVATE
	./
	../deps
	backends
	../glfw/include
)
