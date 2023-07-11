project(cmock)
    
add_library(cmock ${CMAKE_CURRENT_SOURCE_DIR}/src/cmock.c)
    
#todo move to mocks lib
target_include_directories(cmock PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src/)
set_target_properties(cmock PROPERTIES LINKER_LANGUAGE CXX)
target_link_libraries(cmock PRIVATE unity)
