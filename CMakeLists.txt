# Copyright 2017, AppDynamics LLC. and its affiliates
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

cmake_minimum_required(VERSION 3.7)

if(NOT DEFINED ETCDIR)
    if(${CMAKE_INSTALL_PREFIX} EQUAL "/")
        set(ETCDIR /etc)
    else()
        set(ETCDIR ${CMAKE_INSTALL_PREFIX}/etc)
    endif()
endif()

if(NOT DEFINED SYSCONFDIR)
    set(SYSCONFDIR ${ETCDIR}/pdns)
endif()

if(NOT DEFINED UNPRIV_UID)
    set(UNPRIV_UID pdns)
endif()

if(NOT DEFINED UNPRIV_GID)
    set(UPRIV_GID pdns)
endif()

add_subdirectory(etc/pdns)