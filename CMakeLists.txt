cmake_minimum_required(VERSION 3.15...3.26)

project(VMA VERSION 3.1.0 LANGUAGES CXX)

add_library(VulkanMemoryAllocator "src/vk_mem_alloc.cpp")
add_library(GPUOpen::VulkanMemoryAllocator ALIAS VulkanMemoryAllocator)

target_include_directories(VulkanMemoryAllocator PUBLIC include)
target_compile_options (VulkanMemoryAllocator PRIVATE -Wno-error -Wno-pedantive -w)
