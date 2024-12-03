# Go (Golang) Cheat Sheet for C# Developers

## Basics
| Concept             | C#                               | Go                                   |
|---------------------|----------------------------------|--------------------------------------|
| Entry Point         | `static void Main()`            | `func main()`                       |
| Namespace           | `namespace`                    | No namespaces; use packages.        |
| Package Import      | `using System;`                | `import "fmt"`                      |
| Comments            | `// Single line` <br> `/* Multi-line */` | Same syntax as C#.                  |
| String Interpolation| `$"Hello, {name}"`             | `fmt.Sprintf("Hello, %s", name)`    |

## Data Types
| Category            | C#                               | Go                                   |
|---------------------|----------------------------------|--------------------------------------|
| Integer             | `int`, `long`                   | `int`, `int32`, `int64`             |
| Floating Point      | `float`, `double`               | `float32`, `float64`                |
| Boolean             | `bool`                          | `bool`                              |
| String              | `string`                        | `string`                            |
| Byte/Char           | `byte`, `char`                  | `byte`, `rune`                      |
| Arrays              | `int[] nums = new int[5];`      | `nums := [5]int{}`                  |
| Slices (Dynamic)    | `List<int>`                     | `nums := []int{1, 2, 3}`            |
| Dictionaries        | `Dictionary<string, int>`       | `map[string]int`                    |

## Control Flow
| Feature             | C#                               | Go                                   |
|---------------------|----------------------------------|--------------------------------------|
| If-Else            | `if (x > 5) { } else { }`       | `if x > 5 { } else { }`             |
| Switch             | `switch (x) { case 1: break; }` | `switch x { case 1: break }`        |
| Loops              | `for`, `foreach`, `while`       | `for` (acts like all three)         |
| Infinite Loop      | `while(true)`                   | `for {}`                            |
| Break/Continue     | `break; continue;`              | Same syntax.                        |

## Functions
| Feature              | C#                               | Go                                   |
|----------------------|----------------------------------|--------------------------------------|
| Define Function      | `void DoSomething() {}`         | `func DoSomething() {}`             |
| Return Value         | `int Add(int a, int b) { ... }` | `func Add(a, b int) int { ... }`    |
| Multiple Return Values| Not supported                  | `func Divide(a, b int) (int, error)`|
| Named Return Values  | Not supported                  | `func Sum() (result int) { ... }`   |
| Variadic Parameters  | `void Log(params int[] args)`   | `func Log(args ...int)`             |
| Anonymous Functions  | `x => x * x`                   | `func(x int) int { return x * x }`  |

## Key Differences
1. **Go does not have classes**: Use structs and methods on structs instead.
2. **No exceptions**: Go uses error values (`error` type).
3. **Concurrency**: Built-in lightweight goroutines and channels make concurrency simpler than threading in C#.
4. **Simpler syntax**: Go avoids keywords like `public`, `private`, etc. Exported fields and methods are capitalized.
5. **Package system**: Go heavily relies on modular packages and `go mod` for dependency management.
