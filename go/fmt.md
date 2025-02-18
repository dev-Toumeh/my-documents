# FMT

## Introduction
The fmt package in Go is primarily used for formatting strings and printing output to the standard output, 
which is typically the terminal/console when developing command-line applications or services.

### characters and formatting 
- In Go's fmt package, the characters used to correspond to specific types:
    %s: Used for formatting strings.
    %d: Used for formatting integers (decimal).
    %f: Used for formatting floating-point numbers.

### Printing to the Console:
- The fmt.Println() function is used to print a newline-terminated string to the console:

    func main() {
        fmt.Println("Hello, world!")
    }

### Formatting Strings:
- You can format strings using fmt.Sprintf() to create a formatted string without printing it immediately:

    func main() {
      name := "John"
      age := 30
      formattedString := fmt.Sprintf("Name: %s, Age: %d", name, age)
      fmt.Println(formattedString)
    }

### Formatted Printing:
- The fmt.Printf() function is used for formatted printing, similar to printf in C. You specify format specifiers like %s, %d, %f, etc., followed by the values to be substituted:

    func main() {
        name := "Alice"
        age := 25
        fmt.Printf("Name: %s, Age: %d\n", name, age)
    }

### Error Formatting:

    func main() {
        err := fmt.Errorf("An error occurred: %s", "file not found")
        fmt.Println(err)
    }


