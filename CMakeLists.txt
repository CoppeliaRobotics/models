cmake_minimum_required(VERSION 3.12)
project(models)

if(NOT COPPELIASIM_INCLUDE_DIR)
    if(DEFINED ENV{COPPELIASIM_ROOT_DIR})
        set(COPPELIASIM_INCLUDE_DIR $ENV{COPPELIASIM_ROOT_DIR}/programming/include)
    else()
        set(COPPELIASIM_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/../include)
    endif()
endif()
list(APPEND CMAKE_MODULE_PATH ${COPPELIASIM_INCLUDE_DIR}/cmake)
find_package(CoppeliaSim 4.5.0.7 REQUIRED)

coppeliasim_add_model_directory("components")
coppeliasim_add_model_directory("equipment")
coppeliasim_add_model_directory("examples")
coppeliasim_add_model_directory("furniture")
coppeliasim_add_model_directory("household")
coppeliasim_add_model_directory("infrastructure")
coppeliasim_add_model_directory("nature")
coppeliasim_add_model_directory("office items")
coppeliasim_add_model_directory("other")
coppeliasim_add_model_directory("people")
coppeliasim_add_model_directory("robots")
coppeliasim_add_model_directory("tools")
coppeliasim_add_model_directory("vehicles")
