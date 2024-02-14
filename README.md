# JavaScript-Q19
Write a JavaScript program to get the first n Fibonacci numbers.  Note: The Fibonacci Sequence is the series of numbers: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, . . . 

Each subsequent number is the sum of the previous two.

// Recursive JavaScript function to generate a Fibonacci series up to the nth term.
var fibonacci_series = function (n) {
  // Base case: if n is less than or equal to 1, return the base series [0, 1].
  if (n <= 1) {
    return [0, 1];
  } else {
    // Recursive case: generate the Fibonacci series up to (n - 1).
    var s = fibonacci_series(n - 1);
    // Calculate the next term in the series and push it to the array.
    s.push(s[s.length - 1] + s[s.length - 2]);
    // Return the updated Fibonacci series up to the specified length.
    return s.slice(0, n);
  }
};
// Example usage: Calculate and print the Fibonacci series up to the 8th term.
console.log(fibonacci_series(8));

** Output:**

[0,1,1,2,3,5,8,13]
