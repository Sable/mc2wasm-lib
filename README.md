# MatMachJS Libray

[![Build Status](https://travis-ci.org/Sable/matmachjs.svg?branch=master)](https://travis-ci.org/Sable/matmachjs)

- [Matlab library for WebAssembly](#matlab-library-for-webassembly)
  * [Memory Allocation](#memory-allocation)
  * [Memory representation](#memory-representation)
  * [Author](#author)

The purpose of this repository is to create all the built-in functions necessary to support a McLab backend in WebAssembly. At the moment wasm does not support reference types and only allows one memory segment per module, this means before we have Matlab built-ins we must build a library for memory allocation, higher-level constructs among other things.

## Memory Allocation

This will be a simple malloc implementation in WebAssembly, where we use the memory segment as the array of bytes.
- Spec: [spec](./spec/memory_allocation.md)
## Memory representation

It is necessary to manage that memory segment and implement higher level constructs such as arrays, structs, cell-arrays, and strings. 
- Spec: [spec](./spec/memory_representation.md)


## Author
David Herrera
E-mail: davidfherrerar@gmail.com
