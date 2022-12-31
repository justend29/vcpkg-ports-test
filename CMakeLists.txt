cmake_minimum_required(VERSION 3.2)
project(vcpkg-ports-test)

find_package(imgui CONFIG REQUIRED)

if(TARGET imgui::from_custom_port)
  message(NOTICE "Successfully pulled imgui from custom port in custom registry")
else()
  message(FATAL_ERROR "'imgui::from_custom_port' is not a target! Failure.")
endif()
