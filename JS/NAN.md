1. It is a special value that represents an unrepresentable or undefined numerical result. 
2. It indicates a value that is not a legal number, typeof of NaN will return a Number.
3. NaN is often returned as a result when a mathematical operation or function fails to produce a meaningful numeric value.
4. The NaN value is of the number data type, but it is not a "real" number. It is considered a numeric value that is not equivalent to any other number, including itself. Therefore, NaN is not equal to anything, including other NaN values.
5.  isNaN() function converts the given value to a Number type, and then equates to NaN.
```
isNaN("Hello")  // Returns true
isNaN(345)   // Returns false
isNaN('1')  // Returns false, since '1' is converted to Number type which results in 0 ( a number) 
isNaN(true) // Returns false, since true converted to Number type results in 1 ( a number)
isNaN(false) // Returns false
isNaN(undefined) // Returns true
