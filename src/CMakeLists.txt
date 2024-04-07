project(planning_main)

add_subdirectory(pnc_map)
add_subdirectory(process)

add_executable(${PROJECT_NAME} main.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${src_dir}/process)
target_link_libraries(${PROJECT_NAME} PUBLIC process)

target_include_directories(${PROJECT_NAME} PUBLIC ${src_dir}/pnc_map)
target_link_libraries(${PROJECT_NAME} PUBLIC pnc_map)