# polynomial-class
# Overview
This is a class I made for polynomials in Python, my main motivation in creating it was just as a way to learn OOP. It's built from scratch, only using base python imports. It's structured such that it behaves as a base Python type class, i.e. operator overloading/dunder methods. 

# Noteable Features: 
 * Operator Overloading: Standard mathematical operations such as addition, division, multiplication are all implemented with dunder methods such that those operations can be performed on objects of the class with natural syntax. Polynomials can also be multipled by integers or floats, and this multiplication is reflective, i.e. 5 * p1 and p1 * 5, where p1 is a polynomial object, both work.
 * Standard Polynomial Features: The string representation of a polynomial object is inline with mathematical standards. Polynomials can be evaluated at a specific float or integer, and this is in an optimal way with Horner's Method.
 * Calculus: Polynomials can be integrated or differentiated
 * Type Hinting throughout the class.
## Usage Example
```python
from polynomial import Polynomial

# Create P(x) = 3x^2 + 2x + 1
# Coefficients are passed as [x^0, x^1, x^2]
p1 = Polynomial([1, 2, 3])

# Readable string representation

# Evaluate the polynomial at x = 2
print(p1(2)) 
# Output: 17

# Take the derivative
dp = p1.derivative()
print(dp) 
# Output: 6x + 2

# Add two polynomials together
p2 = Polynomial([5, 0, -1]) # -1x^2 + 5
print(p1 + p2)
# Output: 2x^2 + 2x + 6
