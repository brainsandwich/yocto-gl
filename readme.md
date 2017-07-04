# Yocto/GL: C/C++ Single File Libraries for Physically-Based Graphics

_Yocto/GL is a collection of single-file libraries, or single .h/.cpp pairs, for building physically-based graphics applications. Yocto/GL is written in C++14 and compiles on OSX (clang), Linux (clang/gcc) and Windows (cl). You can use Yocto/GL as either header-only libraries, for simplicity, or .h/.cpp pairs, to rduce code bloat and compile time._

This is only the gltf part of Yocto GL. Check the `yocto_gl` if you need all the other libraries.

## Main Libraries

- **yocto_gltf (.h/.cpp)** - Khronos glTF loader and writer automatically generated by the spec. Supports all glTF format including Khronos extensions. Depends on `json.hpp` for json parsing. Optionally depends on `yocto_img.h/.cpp` for texture loading and   writing.

## Support Libraries

- **yocto_img (.h/.cpp)** - Quick and dirty image loading and saving baSed on `stb_image`.

## Documentation

All documentation is included in each library file in plain ASCII. If desired, runs `doxygen` in the root directory to get html formatted documentation.

## Examples

Oh yeah sorry no examples anymore

### Building

mkdir build/
cd build/
cmake .. -G "Whatever"
cmake .. --build

## License

Yocto/GL libraries are released under the permissive MIT license, while the example apps are released under the 2-clause BSD (to include warranty for binary distribution).
