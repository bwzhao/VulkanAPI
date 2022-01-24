cmake_minimum_required(VERSION 3.16)
project(Renderer)

set(CMAKE_CXX_STANDARD 20)

include_directories(/Users/bowen/VulkanSDK/1.2.198.0/macOS/include/ /usr/local/include/)
link_directories(/Users/bowen/VulkanSDK/1.2.198.0/macOS/lib/ /usr/local/lib/)

set(ENV{VK_ICD_FILENAMES} /Users/bowen/VulkanSDK/1.2.198.0/macOS/share/vulkan/icd.d/MoltenVK_icd.json)
set(ENV{VK_LAYER_PATH} /Users/bowen/VulkanSDK/1.2.198.0/macOS/share/vulkan/explicit_layer.d)

add_executable(Renderer main.cpp)
target_link_libraries(Renderer glfw vulkan)
