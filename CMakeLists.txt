############### IMGUI ###############
set(IMGUI_NAME imgui)

include_directories(
        .
)

set(IMGUI_SOURCES
        ${CMAKE_CURRENT_SOURCE_DIR}/imgui.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/imgui_draw.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/imgui_tables.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/imgui_widgets.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_glfw.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_vulkan.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_opengl2.cpp
)

set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} -fPIC)
add_library(${IMGUI_NAME} STATIC ${IMGUI_SOURCES})
