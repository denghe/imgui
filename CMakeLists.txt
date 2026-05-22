set(IMGUI_SRCS)
file(GLOB IMGUI_SRCS	#GLOB_RECURSE
	../imgui/*.h
	../imgui/*.cpp
	../imgui/backends/imgui_impl_glfw.h
	../imgui/backends/imgui_impl_glfw.cpp
	../imgui/backends/imgui_impl_opengl3.h
	../imgui/backends/imgui_impl_opengl3.cpp
	../imgui/backends/imgui_impl_opengl3_loader.h
)

add_library(imgui STATIC
    ${IMGUI_SRCS}
)

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
