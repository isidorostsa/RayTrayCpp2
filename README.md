
RayTrayCpp2
---

RayTrayCpp2 is a Ray Tracing application written entirely using the experimental C++ alternative syntnax: [Cpp2](https://hsutter.github.io/cppfront/).

The goal of this personal project is to showcase and experiment with Cpp2. I am trying to make it as Cpp2-idiomatic as possible, though I think we are still discovering what that means.

Usage
---
To build this project you will need [Modern CMake's cppfront Wrapper](https://github.com/modern-cmake/cppfront). You will need to provide the `cppfront_DIR` to CMake. I am currently using cppfront with the following flags:
- `-in` to avoid modules for the time being
- `-no-s` because disabling bounds-checking yielded a 20x speedup. Also currently it is not possible to index arrays in a consteval context, even when both the size of the array and the index are known constants.
- Currently definitely lacks proper namespacing

Credits
---
- This implementation follows the [Ray Tracing In One Weekend](https://raytracing.github.io/) tutorial.

- This project is inspired by [mraylib](https://github.com/RishabhRD/mraylib).

- A fresh take on C++ evolution: [Cpp2](https://github.com/hsutter/cppfront)

- [Syntax highlighting](https://github.com/elazarcoh/cpp2-syntax) for Cpp2, massively helpful!