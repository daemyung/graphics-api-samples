# MIT License
#
# Copyright (c) 2018 DAEMYUNG, JANG
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in all
# copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.

#
# Add triangle executable.
#
add_executable(TriangleSample WIN32
	source/triangle-resources.h
	source/gl-triangle-sample.h
	source/gl-triangle-sample.cpp
	source/vk-triangle-sample.h
	source/vk-triangle-sample.cpp
	source/dx-triangle-sample.h
	source/dx-triangle-sample.cpp
	source/main.cpp)

#
# Link libraries
#
target_link_libraries(TriangleSample
	PRIVATE
		Common)

#
# Compile definitions
#   
target_compile_definitions(TriangleSample
	PRIVATE
		RESOURCE_DIR="${CMAKE_CURRENT_SOURCE_DIR}/resources")

#
# Set properties.
#
set_target_properties(TriangleSample
	PROPERTIES
		CXX_STANDARD          17
		CXX_STANDARD_REQUIRED ON)