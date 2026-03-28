# 42 ft_printf

## Overview
This project reimplements printf in C as ft_printf, with variadic argument handling and formatted output conversion.

It focuses on building a reliable formatting engine from scratch while preserving expected output and return-value behavior.

## Features
Supported conversions:
- c
- s
- p
- d
- i
- u
- x
- X
- percent literal

Additional formatting behaviors are implemented according to project scope and tests.

## Core Concepts

### Variadic Arguments
ft_printf reads unknown argument lists using stdarg macros. Correct type extraction per conversion is essential.

### Format Parsing Pipeline
Each conversion follows a pipeline:
1. detect `%`
2. parse conversion context (flags/width/precision if supported)
3. dispatch to conversion handler
4. write formatted output
5. accumulate printed character count

### Return Value Semantics
Like printf, ft_printf returns the number of characters printed. This makes output accounting part of core logic, not an optional extra.

### Base Conversions
Numeric conversions require custom integer-to-string formatting in decimal and hexadecimal bases, including unsigned and pointer representations.

## Build
- make

## Usage
Include header:
- ft_printf.h

Example:
- ft_printf("Score: %d percent\n", 100);

Additional examples:
- ft_printf("Hex: %x %X\n", 255, 255);
- ft_printf("Ptr: %p\n", ptr);
- ft_printf("String: %s Char: %c\n", "hello", 'A');

## Project Structure
- ft_printf.c: main dispatcher and formatting flow
- ft_printf.h: declarations
- libft: helper utility library
- Makefile: build rules

Typical internal split:
- parser/dispatcher
- conversion handlers
- write wrappers and counter updates

## Key Learnings
- Variadic functions with stdarg
- Number/string conversion pipelines
- Output accounting and return values

## Notes
ft_printf is a core 42 project and a practical foundation for future parser-driven implementations.
