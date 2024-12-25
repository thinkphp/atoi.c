# Custom Integer Parser

A simple C program that implements a custom string-to-integer conversion function, similar to the standard `atoi()` function. The program validates input strings and converts them to integers, handling positive and negative numbers.

## Features

- Input validation for integer strings
- Handles positive and negative numbers
- Supports leading '+' and '-' signs
- Custom implementation without using standard `atoi()`

## Implementation Details

The program consists of two main functions:

### 1. `correct(char str[50])`

Validates if the input string represents a valid integer:
- Checks if the first character is a digit, '+', or '-'
- Verifies that all subsequent characters are digits
- Returns 1 if valid, 0 if invalid

### 2. `atoi2(char str[50])`

Converts the validated string to an integer:
- Handles leading '+' and '-' signs
- Performs digit-by-digit conversion
- Returns the final integer value with appropriate sign

## Usage

1. Compile the program:
   ```bash
   gcc integer_parser.c -o integer_parser
   ```

2. Run the program:
   ```bash
   ./integer_parser
   ```

3. Enter a string when prompted:
   ```
   string = -123
   -123 = -123
   ```

## Input Examples

Valid inputs:
- "123" → 123
- "-456" → -456
- "+789" → 789

Invalid inputs:
- "12a34" (contains letters)
- "1.23" (contains decimal point)
- "abc" (no digits)

## Error Handling

The program will display "Number is not integer!" for any invalid input that doesn't match the expected integer format.

## Limitations

- Maximum input length is 49 characters (plus null terminator)
- Does not handle integer overflow
- Does not support floating-point numbers

## Contributing

Feel free to submit issues and enhancement requests!

## License

MIT
