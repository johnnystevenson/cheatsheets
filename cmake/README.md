| Usage  | Description |
| ------------- | ------------- |
| `set(list file1.cpp file2.cpp)`  | Creates a variable, in this case a list of filenames  |
| `include_directories( $(includes) )` | Adds directories to the include path for building subsequent targets |
| `add_executable( a.out $(list)`  | Adds an executable target built from a list of source files |
| `add_library( libname STATIC|SHARED $(libname_srcs) ) `  | Adds a library target built from a list of source files |
| `target_link_libraries( a.out $(libnames) ) `  | Links libraries to a target, in this case a list of libraries to the target executable |