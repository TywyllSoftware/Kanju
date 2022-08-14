cmake_minimum_required(VERSION 3.21)
set(CMAKE_CXX_STANDARD 17)
project(Kanju)

add_subdirectory(metal-cmake)  # Library definition

FILE(GLOB SRC_FILES 
	${PROJECT_SOURCE_DIR}/src/*.cpp
	${PROJECT_SOURCE_DIR}/src/*.h
)

# Create executable and link target
add_executable(${PROJECT_NAME} ${SRC_FILES})
target_link_libraries(${PROJECT_NAME} METAL_CPP)