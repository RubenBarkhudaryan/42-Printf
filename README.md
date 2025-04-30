## 42 ft_printf README.md

# 42 ft_printf

ft_printf is a reimplementation of the standard C library `printf` function. The challenge is to master variadic functions, format specifiers, and produce a robust, error-safe implementation that handles numerous conversion options.

## Features

- **Conversion Specifiers:** `%c`, `%s`, `%p`, `%d`, `%i`, `%u`, `%x`, `%X`, and `%%`.  
- **Flags & Formatting:** Handles flags (`-`, `0`, etc.), field widths, and precision.  
- **Robust Error Management:** Ensures safe handling of edge cases and erroneous input.

## Installation

Clone the repository:

## Bash
```
git clone https://github.com/RubBarkhudaryan/42-Printf.git
```

## Compile the library:

```
make
```

## Usage
Include the header file in your project:

```
#include "ft_printf.h"
```

## Example usage
```
ft_printf("Hello %s, your score is %d%%\n", "User", 100);
```

## Project Structure
libft/ – utilities for correct functionality of ft_printf

**Makefile** - automated compilation of program by using command ```make```
**ft_printf.c** - the main part of ft_printf implementation
**ft_printf.h** - header file where were defined all the neccessary functions and macros

**Author
Rub Barkhudaryan**
