# Copyright 2024 Multiproject DevOps Team
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

cmake_minimum_required(VERSION 3.14)

project(hello_world_library VERSION "1.0.0" LANGUAGES CXX)
include(cmake/get_cmaize.cmake)

cmaize_add_library(
    hello_world_library
    SOURCE_DIR "${CMAKE_CURRENT_LIST_DIR}/src"  
    INCLUDE_DIRS "${CMAKE_CURRENT_LIST_DIR}/include/hello_world_library"
    
)
cmaize_add_package(hello_world_library NAMESPACE hello_world_library::)