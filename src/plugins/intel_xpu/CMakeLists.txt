# Copyright (C) 2018-2024 Intel Corporation
# SPDX-License-Identifier: Apache-2.0
#

if (NOT ENABLE_INTEL_XPU)
    return()
endif()

set (TARGET_NAME "openvino_intel_xpu_plugin")

# build properties

set(XPU_DEVICE_NAME "XPU")

set(XPU_PLUGIN_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR})

set(CMAKE_CXX_STANDARD 11)

find_program(ICPX_COMPILER icpx)
message("##### find the icpx compiler: ${ICPX_COMPILER} #####")

set(CMAKE_CXX_COMPILER ${ICPX_COMPILER})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fsycl")