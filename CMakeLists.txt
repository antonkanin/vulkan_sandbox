cmake_minimum_required(VERSION 3.7)

project(vulkan_test)

add_executable(${PROJECT_NAME} main.cpp)

target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_17)

#set(ENV{VULKAN_SDK} "/home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64")
#set(ENV{VK_LAYER_PATH} "/home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64/etc/explicit_layer.d")
#set(ENV{LD_LIBRARY_PATH} "/home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64/lib")

# lifehack to manually copy vulkan layer files
# https://community.khronos.org/t/why-does-my-vulkan-instance-have-no-any-validation-layers/7007/10

target_link_libraries(${PROJECT_NAME}
        #glm
        glfw
        /home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64/lib/libvulkan.so)

target_include_directories(${PROJECT_NAME} PUBLIC
        /home/anton/fun/vulkansdk-linux-x86_64-1.1.101.0/1.1.101.0/x86_64/include)
