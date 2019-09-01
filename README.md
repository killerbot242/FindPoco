# FindPoco
cmake find module to find an installed poco


This file is heavily inspired by : 
- https://github.com/astahl/poco-cmake/blob/master/cmake/FindPoco.cmake
- FindBoost.cmake which ships with cmake

It is being build from scratch, with limited scope, which will be extended, hopefully on a steady pace.

First limits : 
- only linux
- from a poco installed on the system by building it manually (the old make syntax, as well as the cmake build syntax of poco)
- no distinction yet between debug/release
- limited inner library dependency tracking
- if possible only support IMPORTED taargets and no variable approach (moderncmake)


Current feature list : 
- detects poco within the above described limits
- provides IMPORTED targets for all the poco llibraries
- provides for a limited set of those "dependencies" between those libraries (example : Util depends on Foundation"
- provide use examples


Future lists : 
- installed poco versions that come from linux distriution repositories (ubuntu might have it ...)
- fully support/distinction between debug and release built types
- extend inner dependencies to cover all poco libraries
- support finding poco by finding the cmake generated files from a cmake build poco
- support cross compiling
- one day support windows ??
