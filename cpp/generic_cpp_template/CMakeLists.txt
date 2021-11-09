set(CMAKE_BUILD_TYPE Debug)
cmake_minimum_required(VERSION 3.17)
project("test_proj")
add_definitions(-std=c++17)
if (MSVC)
	# warning level 4 and all warnings as errors
	add_compile_options(/W4 /WX)
else()
	# lots of warnings and all warnings as errors
	add_compile_options(-Wall -Wextra -pedantic )
endif()



add_executable(main main.cpp functions.cpp)
