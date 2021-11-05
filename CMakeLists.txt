cmake_minimum_required(VERSION 3.0.0)
project(Focal VERSION 0.1.0)

include(CTest)
enable_testing()

file(GLOB SRCFILES src/*.cpp)
link_directories({PROJECT_DIR}/include)

add_executable(Focal ${SRCFILES})
target_link_libraries(Focal libSDL2-2.0.so.0)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
