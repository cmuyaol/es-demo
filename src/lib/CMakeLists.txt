cmake_minimum_required(VERSION 3.10)

project(mylib VERSION 1.0.0)

add_library(mylib SHARED lib/mylib.cpp)
target_include_directories(mylib PUBLIC lib)

set_target_properties(mylib PROPERTIES VERSION ${PROJECT_VERSION})
set_target_properties(mylib PROPERTIES SOVERSION 1)

install(TARGETS mylib DESTINATION lib)
install(FILES lib/mylib.h DESTINATION include)
