cmake_minimum_required(VERSION 4.1)
project(Eukariot)

set(CMAKE_CXX_STANDARD 26)

add_subdirectory(vendor)
add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE vendor)




#add_custom_target(copy_assets
#        COMMAND ${CMAKE_COMMAND} -E copy_directory ${CMAKE_CURRENT_LIST_DIR}/assets ${CMAKE_CURRENT_BINARY_DIR}/assets
#)
#add_dependencies(${PROJECT_NAME} copy_assets)

#include(InstallRequiredSystemLibraries)
#set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_CURRENT_SOURCE_DIR}/Liscense.txt")
#include(CPack)