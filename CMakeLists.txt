cmake_minimum_required (VERSION 3.5)

project (yocto-gl)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED on)

# compile flags
if(APPLE)
    add_definitions(-Wno-missing-braces)
endif(APPLE)
if(WIN32)
    add_definitions(/D_CRT_SECURE_NO_WARNINGS /wd4018 /wd4244 /wd4305 /wd4800 /wd4267)
endif(WIN32)

file(GLOB yocto_sources yocto/yocto_*.cpp)
file(GLOB yocto_headers yocto/yocto_*.h)
set(yocto_include_dir ${PROJECT_SOURCE_DIR})

add_library(yocto STATIC ${yocto_sources} ${yocto_headers})
target_include_directories(yocto PUBLIC ${yocto_include_dir})