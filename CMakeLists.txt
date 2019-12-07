# Json cpp shared library

cmake_minimum_required (VERSION 3.8)

set(LIB_NAME "JsonCppLib")

file(GLOB_RECURSE LIB_SOURCES "src/*.cpp")
file(GLOB_RECURSE LIB_HEADERS "src/*.h" "include/*.h")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

# Add source to this project's executable.
add_library(${LIB_NAME} STATIC ${LIB_SOURCES} ${LIB_HEADERS})

target_include_directories(${LIB_NAME} PUBLIC src PUBLIC include)

