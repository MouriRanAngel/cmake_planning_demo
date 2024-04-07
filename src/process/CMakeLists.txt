project(process)

add_library(${PROJECT_NAME} SHARED process.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${src_dir}/pnc_map)

target_link_libraries(${PROJECT_NAME} PUBLIC pnc_map)