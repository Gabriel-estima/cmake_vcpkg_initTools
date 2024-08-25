cmake_minimum_required(VERSION 3.8)

	project(pn)

	find_package(fmt CONFIG REQUIRED)

	add_executable(en a.cpp)

	target_link_libraries(en PRIVATE fmt::fmt)