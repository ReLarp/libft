# Libft — 42 School Project

> *C library containing custom re-implementations of standard C library functions.*

---

## 📌 About The Project

`libft` is the foundational C library project at 42 School. The objective is to re-code a set of standard C library functions from scratch, as well as additional utility functions, without using standard non-allowed C functions. This library serves as a primary dependency for future 42 C projects such as `ft_printf`, `get_next_line`, and `minishell`.

---

## 🛠️ Project Rules & Constraints

* **Language:** C (compiled with `cc`)
* **Compilation Flags:** `-Wall -Wextra -Werror`
* **Code Style:** Strictly compliant with **Norminette 3.x** rules.
* **Memory Management:** Zero memory leaks allowed (`malloc`/`free` monitored).
* **Forbidden:** No `global` variables; standard library functions restricted except those explicitly authorized per project scope.

---

## 📚 Function Overview

| Function | Category | Description |
| :--- | :--- | :--- |
| `ft_strlen` | String Processing | Calculates the length of a string. |
| `ft_memcpy` | Memory Operations | Copies a memory area from source to destination. |
| `ft_strdup` | Allocation | Allocates memory and duplicates a given string. |
| `ft_split` | Parsing | Splits a string into an array of substrings based on a delimiter. |

---

## ⚙️ Compilation & Usage

### 1. Build the Library
Run `make` in the root directory to generate the static library file `libft.a`:

```bash
make
```

Available Makefile rules:
* `make`: Compiles all `.c` files into `.o` and creates `libft.a`.
* `make clean`: Removes all `.o` object files.
* `make fclean`: Removes `.o` object files and the output library `libft.a`.
* `make re`: Performs `fclean` followed by `make`.

### 2. Linking in Your Own Projects
Include the header file in your `.c` files and compile with the static library path:

```c
#include "libft.h"
```

```bash
cc -Wall -Wextra -Werror main.c -L. -lft -o my_program
```

---

## 🧪 Testing

This project has been thoroughly tested using official school testers and memory analyzers:

* **Norminette:** `norminette -CheckDefine libft.h` `norminette -CheckForbiddenSourceHeader *.c`
* **Valgrind Memory Leak Test:**
  ```bash
  valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./my_program
  ```
* **Third-Party Testers:** 42 Network Moulinette

---

## 👤 Author

* **Login:** `islakoua`
* **Campus:** 1337 Rabat / 42 Network
