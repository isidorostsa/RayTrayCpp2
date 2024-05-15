cmake_minimum_required(VERSION 3.23)
project(example)

set(CXX_COMPILER clang++)
set(CXX_STANDARD 23)

find_package(cppfront REQUIRED)

add_executable(main src/main.cpp2)

set(cpp2headers src/inc/sphere.h2 src/inc/color.h2 src/inc/vec3.h2 src/inc/ray.h2 src/inc/hittable.h2 src/inc/hittable_list.h2)

cppfront_generate_cpp(cpp1headers ${cpp2headers})

target_sources(main PUBLIC ${cpp1headers})