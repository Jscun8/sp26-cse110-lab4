**Question 1:** Line 12 will print 3. This is due to the variable i being declared by `var` so even if some line of code outside of the for loop tries to access the variable i (which was both declared and assigned inside the for loop), no error will occur. i takes the last value that it was assigned which was i = prices.length from the for loop. prices is [100, 200, 300] so prices.length is 3.

**Question 2:** Line 13 prints 150. This value is printed because similar to the previous question, declaring a variable with `var` makes it function-scoped rather than block-scoped. So any other thing as long as its in the function can still access it and doesn't have to be inside the for-loop that the variable was declared/defined in. Line 13 prints the last value that discountedPrice was assigned once the for loop terminated. this is 300 * (1-discount) = 300 * (1-0.5) = 150.

**Question 3:** At line 14, the code prints 150. This is the last assigned value for finalPrice which is essentially just discountedPrice but rounded as well. This still results in 150 being printed.

**Question 4:** This function returns the array called discounted which contains [50, 100, 150]. This is after all elements are parsed (discounted,rounded, and pushed into the array) from the for-loop. The final result is returning [50, 100, 150]. Although not explicitly visible in the console/terminal, you can just use console.log to explicitly see what was printed. 

**Question 5:** At line 12, the code causes an error because i is not defined, so a ReferenceError is thrown. This is because `let` is block-scoped and not function-scoped. Thus, since we attempt to reference i outside the for-loop, this causes an error.

**Question 6:** At line 13, we get the same error as in question 5. ReferenceError since discountedPrice is not defined outside the for-loop block.

**Question 7:** At line 14, the value 150 is printed. So printing finalPrice outside of the for-loop still works despite changing all variable declarations from `var` to `let` becuse finalPrice is also declared outside the for-loop block, and not only inside the for-loop. So it exists outside of the for-loop block, and we keep the last assigned value for finalPrice from inside the for-loop which is 150. 

**Question 8:** The function still returns the array called discounted which contains [50, 100, 150]. There is no error since discounted is declared outside of the for-loop block so it exists outside of that block-scope allowing the function to still be able to return it. The contents are then pushed in by the for-loop, and the function returns the array, discounted.

**Question 9:** A ReferenceError occurs since the reference attempt on i from line 11 is outside of the scope of the for-loop block. Similar to `let`, `const` is also a block-scoped declaration. So we will get a ReferenceError since i is not defined outside of the for-loop block.

**Question 10:** Line 12 prints 3. This is because prices is declared as a function argument, and thus can be used function-wide, not just limited to a closed block like an if-block or a for-loop inside the function. length is a constant variable, and since it is never reassigned after it has already been assigned to prices.length, there is no issue and no error occurs.

**Question 11:** The function still returns discounted with no issues which contains [50, 100, 150]. This is because const only prevents the variable that it was declared with from being reassigned to another value. discounted was never reassigned. It was initialized to an empty array, and then the for-loop block just pushed items into the array to fill the array with values. No reassigning, only mutating or modifying the contents of the discounted array. const only prevents reassignment but doesn't make the data itself immutable. There are also no block-scope issues like only being declared inside a for-loop. Thus, we can safely return the array discounted.

**Question 12:** Answer questions A,B,C,D,E.
A. student.name; OR student["name"];
B. student["Grad Year"];
C. student.greeting();
D. student['Favorite Teacher'].name;
E. student.courseLoad[0];

**Question 13:** Arithmetic
A. '3' + 2 outputs '32' because integers map to their exact string representation. Due to string concatenation and the `+` operator, 2 gets converted into its string representation and the result is 32. 

B. '3' - 2 outputs 1. This is because the `-` operator performs stricly mathematical subtraction causing the string 3 to be converted into 3 as a number. Then 3-2 is computed which results in 1 as the output.

C. 3 + null outputs 3. This is because of numeric conversion rules. The value null becomes 0. Then normal addition is computed, 3 + 0 = 3.

D. '3' + null outputs '3null'. This is because of string concatenation. When we use the `+` operator on the string 3 and null, then null gets converted into a string. So null becomes 'null' and we get '3null' as the result.

E. true + 3. This outputs 4. This is in normal mathematical addition between two numbers, the boolean true becomes a value of 1. So we have 1+3 = 4.

F. false + null. This outputs 0. This is because for numerical addition operation, false gets converted into the numerical value of 0 and null also gets converted into its numerical value which is 0 as well. So we get 0 as the output.

G. '3' + undefined. This outputs '3undefined'. This is because of string concatenation. Using the `+` operator on the string 3 and undefined would convert undefined to a string. This results in the output '3undefined'.

H. '3' - undefined. This outputs NaN. This is because when we use the `-` operator, we are strictly performing a mathematical subtraction operation. So '3' gets converted into the numerical number 3, and undefined gets converted to its numerical value which is NaN by conversion rules. This gives 3 - NaN which results in the output being NaN.

**Question 14:** Comparison
A. '2' > 1. This outputs true. Note that all comparison operators return a boolean value. The string '2' becomes a number 2, which is indeed greater than 1.

B. '2' < 12. This outputs true. The string '2' gets converted into a number 2, which is less than 12, so true is the output.

C. 2 == '2'. This outputs true. This is because the string '2' gets converted into a number 2 which is indeed equal to 2. So true is the output.

D. 2 === '2' outputs false. This is because the `===` operator is a strict equality check. Unlike the `==` regular equality check, the `===` would return false here because the two sides are of different types. 2 is a number whereas '2' is a string.

E. true == 2 outputs false. This is because after numerical conversion, true is equivalent to 1. However, 1 does not equal 2. Thus, false is the output.

F. true === Boolean(2) outputs true. This is because Boolean(any number other than 0) would be converted to the boolean true. If we have Boolean(0) then this is the one case where the boolean false is returned. However, here, we have Boolean(2) which would be converted to the boolean value of true. So we have true === true which is true even with the strict equality check since both sides are of the same type and have equal values.

**Question 15:** Explain the difference between the == and === operators.
The difference between the `==` and the `===` operators is that `==` is a loose or regular equality checker. This operator can involve type conversion such that both sides have the same common type and can then be compared. This involves conversion rules. For instance true/false become 1 and 0 respectively, and 5=='5' returns true due to the string '5' getting converted to a numerical 5. On the other hand, the `===` is the strict equality operator. Here, no type conversions are allowed, and it would only return true if both the values and the data type is the same. So if we have 5==='5', this would return false since the two sides are of different data types. 5 is a number, while '5' is a string.

**Question 17:** Calling the function modifyArray([1,2,3], doSomething) would result in the output of [2,4,6]. Firstly, inside the function modifyArray, we create an empty const array newArr. Inside the for-loop block the loop would terminate when i is the length of array which is the first argument passed to the function modifyArray, i.e. [1,2,3]. So the first iteration i=0 would look something like this: we call callback(array[i]), and callback is the second argument in the modifyArray function. calling callback on array[0] is essentially just calling it for the first element in the array passed as the first argument, so we have callback(1). Our second argument we pass when calling modifyArray([1,2,3], doSomething) would be doSomething. The function doSomething takes in num as its argument. So we have doSomething(1). This results in 1*2 = 2 as the first element to be pushed into the empty const array newArr. The other two elements 2, and 3 follow similarly. So we have the output [1*2, 2*2, 3*2] which is [2,4,6].

**Question 19:** The output of the code is: 1 4 3 2.
First of all, 1 is printed immediately, next we have a setTimeout of 1000 ms (1 second) delay for 2, and a setTimeout of 0 ms delay for 3, and then 4 is immediately printed. The numbers in the setTimeout are set aside in a task or callback queue to be executed after the current main call stack. Next javascript then looks at the callback queue and executes it. Since 3 has a 0 ms delay, it is ready immediately and printed first. Finally, 2 is printed last due to having a 1000 ms or 1 second delay.
