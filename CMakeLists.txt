cmake_minimum_required(VERSION 3.0)
project(qimq)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}  -pthread -std=c++17")

include_directories(${Boost_INCLUDE_DIRS} ${OPENSSL_INCLUDE_DIR}
        "rest_rpc/include"
        "rest_rpc/third/msgpack/include"
        )

add_executable(qimq main.cpp)