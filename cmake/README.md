| Usage  | Description |
| ------------- | ------------- |
| `set(list file1.cpp file2.cpp)`  | Creates a variable, in this case a list of filenames  |
| `find_package(Name REQUIRED)` | Sets Name_INCLUDE_DIR and Name_LIBRARIES using local FindName.cmake script, a FindName.cmake built into cmake, or a NameConfig.cmake in the search path |
| `include_directories( $(includes) )` | Adds directories to the include path for building subsequent targets |
| `add_executable( a.out $(list)`  | Adds an executable target built from a list of source files |
| `add_library( libname STATIC\|SHARED $(libname_srcs) ) `  | Adds a library target built from a list of source files |
| `target_link_libraries( a.out $(libnames) ) `  | Links libraries to a target, in this case a list of libraries to the target executable |
