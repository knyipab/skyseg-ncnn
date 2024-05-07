cmake_minimum_required(VERSION 3.10)

project(skyseg-ncnn)

configure_file(skyseg-ncnn.cpp.in skyseg-ncnn.cpp)

add_executable(skyseg-ncnn ${PROJECT_BINARY_DIR}/skyseg-ncnn.cpp)

find_package( OpenCV REQUIRED )
find_package( ncnn REQUIRED )


target_include_directories(skyseg-ncnn PUBLIC ${OpenCV_INCLUDE_DIRS}/opencv4 )

target_link_libraries(skyseg-ncnn opencv_core opencv_imgcodecs opencv_imgproc ncnn)

install(TARGETS skyseg-ncnn DESTINATION bin)
install(FILES skysegsmall_sim-opt-fp16.bin DESTINATION etc/skyseg-ncnn)
install(FILES skysegsmall_sim-opt-fp16.param DESTINATION etc/skyseg-ncnn)
