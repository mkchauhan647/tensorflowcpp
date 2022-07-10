cmake_minimum_required(VERSION 3.0.0)
project(check VERSION 0.1.0)

include(CTest)
enable_testing()
#set(HEADERS_FILE  

 set(HEADERS_FILE

 /home/mroot/Desktop/tensorflow/include
 /home/mroot/Desktop/tensorflow/incude/src/

 )
 include_directories(check PUBLIC /home/mroot/Desktop/tensorflow/include)
 include_directories(check PUBLIC /home/mroot/Desktop/tensorflow/include/src)

#  add_library(externalLibA SHARED IMPORTED)
# set_target_properties(externalLibA 
#     PROPERTIES IMPORTED_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/libtensorflow_cc.so.2.10.0)
# target_include_directories(externalLibA
#     INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})


add_executable(check main.cpp)
target_compile_features(check PRIVATE cxx_std_17)
target_link_libraries(check PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/libtensorflow_cc.so.2.10.0 ${CMAKE_CURRENT_SOURCE_DIR}/libtensorflow_framework.so.2.10.0)
#target_link_libraries(${PROJECT_NAME} PUBLIC externalLibA)
#target_include_directories(check PUBLIC ${HEADERS_FILE})
set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
