cmake_minimum_required(VERSION 3.7)

project(vulkan_test)

add_executable(${PROJECT_NAME} main.cpp)

target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_17)

target_link_libraries(${PROJECT_NAME}
        #glm
        glfw
        /home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64/lib/libvulkan.so)

target_include_directories( ${PROJECT_NAME} PUBLIC
        /home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64/include)
