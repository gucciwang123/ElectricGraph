add_executable(graph "")
include(${CMAKE_CURRENT_SOURCE_DIR}/sources.cmake)

if(WIN32)
else()
	find_library(LIB_GLEW NAMES libglew glew REQUIRED)
	find_library(LIB_SDL2 NAMES libsdl2 SDL2 REQUIRED)

	target_link_libraries(graph PRIVATE ${LIB_SDL2} PRIVATE ${LIB_GLEW})
endif()


