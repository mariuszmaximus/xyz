cmake_minimum_required(VERSION 3.0.0)
project(xyz VERSION 0.1.0)

include(CTest)
enable_testing()



if(XYZ_NAME)
else()
    set(XYZ_NAME "xyz")
endif()

message(STATUS "PPPPPPPPPPPPPPP")
message(STATUS "XYZ_NAME=${XYZ_NAME}")
message(STATUS "PPPPPPPPPPPPPPP")


add_library(${XYZ_NAME} xyz.cpp)

target_include_directories(${XYZ_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}) 

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack) 
