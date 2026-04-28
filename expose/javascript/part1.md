**Question 1:** Line 9 in the given code snippet prints, values added: 20. 

**Question 2:** Line 13 prints, final result: 20. 

**Question 3:** We should not use var due to it being function-scoped rather than block-scoped. It has a property that when declaring some variable using var, the declaration gets hoisted upwards and can be accessed anywhere inside the function, while the assignment still remains to be parsed on the line it was written on. This can lead to a more difficult time debugging, as variables can be accessed outside of their intended scope in the curly braces. When accessing the var before it is assigned, no crashing occurs, only an undefined value is assigned.

**Question 4:** Line 9 prints, values added: 20

**Question 5:** Line 13 returns an error. Specifically, due to result not being defined. This error is returned because the console.log print statement at line 13 tries to reference the variable result that was declared by `let`. But in doing so this error is caused because the statement on line 13 is outside of the scope where result was declared and defined. Due to the properties of declaring a variable with `let`, an error would occur for any attempt to reference that variable outside of the scope of the `let` variable definition. Thus, `let` is block-scoped, and the defined variable can only be accessed inside the enclosed block on which it is defined (i.e. inside the if statement block enclosed in the curly braces). 

**Question 6:** Line 9 returns an error. This is a TypeError and it occurs because we cannot reassign another value to a `const` variable that has already been assigned a value. So since result couldn't be assigned to the new value num1+num2. This error happens before the code is even able to reach and execute the console.log statement on line 9. 

**Question 7:** Line 13 also returns an error for a similar reason to in Question 6. A TypeError occurs before the code reaches the console.log line. Execution is halted due to the line where we attempt to assign result = num1 + num2 when result is a const variable that has already been assigned to 0. Additionally, declaring a variable with `const` is also block-scoped like `let` so line 13's reference to result would also have a ReferenceError. But this line isn't even reached due to the error in the line where we attempt to reassign const result.