#
# Copyright (c) 2015-present, Facebook, Inc.
# All rights reserved.
#
# This source code is licensed under the BSD-style license found in the
# LICENSE file in the root directory of this source tree.
#

set(OLD_DEFAULT_COMPONENT ${CMAKE_INSTALL_DEFAULT_COMPONENT_NAME})
set(CMAKE_INSTALL_DEFAULT_COMPONENT_NAME libraries)

add_subdirectory(ext)
add_subdirectory(libutil)
add_subdirectory(plist)
add_subdirectory(process)

set(CMAKE_INSTALL_DEFAULT_COMPONENT_NAME ${OLD_DEFAULT_COMPONENT})

