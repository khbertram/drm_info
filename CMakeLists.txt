cmake_minimum_required(VERSION 3.0)

project(drm_info)

add_executable(drm_info 
 json.c
 main.c
 modifiers.c
 pretty.c
)

target_link_libraries(drm_info -llibdrm -ljson-c)
install(TARGETS drm_info DESTINATION usr/bin)
