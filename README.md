# C++ templates tutorial

## [under construction]

Ever wondered how C++ templates work or how to use/write them? Then this is the right place you came to.

I have created this repository to provide easy to understand explanation and examples. While cppreference.com has complete documentation, there aren't that many examples and the webpage intends to have very technical-like language which can be hard to understand.

Contents
- intro (please read)
- function templates
- template default arguments, templated funcions overloading
- class templates
- template full specialization, template partial specialization
- non-type templates, dependent names
- `<type_traits>`, `constexpr` and `static_assert`
- templates of templates (yes, they exist)
- (since C++11) variadic templates (`...`) and perfect forwarding (`Args&&...`)
- (since C++14) alias templates (aka templated `typedef`)
- (since C++14) variable templates
- (since C++17) fold expressions (`0 + ... + args`)
- (since C++20) concepts (constrained templates)
- CRTP (example of static polymorphism)
- expression templates
- SFINAE - what is it
- SFINAE with `std::enable_if`
- SFINAE with `std::void_t`
- examples
  - discrete mathematics using SFINAE and `constexpr`
  - lambda traits
  - containers
    - vector
	- single-linked list
	- simple smart pointer with unique ownership
  - bit pattern scanner
  - sample small ET library
  - lazy initialization


Intro

History // TODO: write more ot link to wikipedia
At the early stage of forming C++, templates were added as a very powerful tool to create generic code, they originated from Ada generics. Later, there have been multiple (often accidental) discoveries: C++ templates syntax is a standalone, turing-complete, purely functional language. As the time progressed, more features regarding templates where added.

The target - why do we need generic programming
Generic code offers high portability, extensibility and // TODO: as above

Important note
C++ templates are a way of expressing generalized instructions. Templates alone can not be compiled, since they are only "code drafts" - exact types/values are unknown or incomplete. This means you have to put both template declarations and definitions in header files.
