cmake_minimum_required( VERSION 3.16 )

project( imgui )

add_library( ${PROJECT_NAME} )
target_sources( ${PROJECT_NAME} PRIVATE
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_opengl3.cpp
)

target_include_directories( ${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} )

target_link_libraries( ${PROJECT_NAME} PUBLIC glfw glad )
