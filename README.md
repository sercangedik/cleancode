# Clean Code
![alt tag](https://www.butterfly.com.au/images/easyblog_images/27/2e1ax_butterfly_entry_ARASH-clean-code.jpg)

##Chapter 1 - Clean Code
### İzci Kuralı
 _Kamp kurduğunuz yeri kamp kurmadan önceki halinden daha temiz bırakın._ 

### **Üstadlar için Clean Code nedir ?**

* **Bjarne Stroustrup :** Elegant and efficient.
* **Grady Booch :** Simple and direct.
* **Michael Feathers :** It looks like it was written by someone who cares.
* **Ron Jeffries :** Small, expressive, simple and no duplication.

##Chapter 2 - Meaningful Names

* Avoid disinformation
* Use pronounceable names
* Use searchable names

### Pick One Word per Concept
* Controller
* Manager
* Driver

### Don't pun (kelime oyunu)

* Shorter names are generally better than longer ones, so long as they are clear. Add no
more context to a name than is necessary.


##Chapter 3 - Functions

### Small !

* The first rule of functions is that they should be small. The second rule of functions is that
they should be smaller than that.

### Do One Thing

* Functions should do one thing. They should do it well. They sould do it only.

### The Stepdown Rule

* image.

### Use Descriptive Names

* Don’t be afraid to make a name long. A long descriptive name is better than a short enigmatic name.

### Don't Repeat Yourself !

## Chapter 4 - Comments 

### Don’t comment bad code—rewrite it.

* Formatting
* Clarification
* TODO
* Journal
* Position Markers

## Chapter 5 - Formatting

* Vertical Formatting
* Horizontal Formatting

### Team Rules
* A team of developers should agree upon a single formatting style.

## Chapter 6 - Objects and Data Structures

### Law of Demeter 
* Talk to Friends Not to Strangers

### Data Transfer Objects
* A class with public variables and no functions

### Train Wrecks

## Chapter 7 - Error Handling

### Use Exceptions Rather Than Return Codes
* It is easy to forget
* Provide context with exceptions

## Avoid pass null && return null

## Chapter 8 - Boundaries
* Write test for the third-party code for understanding
* Abstraction

## Chapter 9 - Unit Tests

### The Three Laws of TDD
* You may not write production code until you have written a failing unit test.
* You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
* You may not write more production code than is sufficient to pass the currently failing test.
 
### Tests enable the -ilities
* Flexible
* Maintainable
* Reusable

### Why ?
* If you have tests, you do not fear making changes to the code.

### Keeping test clean
* Readability
* Readability
* Readability

### One Assert per Test
* Single conclusion that is quick and easy to understand.

### Single Concept per Test
* Test a single concept in each test function.

### F.I.R.S.T.
* Fast (Tests should be fast)
* Independent (Tests should not depend on each other)
* Repeatable (Tests should be repeatable in any environment)
* Self Validating (The tests should have a boolean output)
* Timely (The tests need to be written in a timely fashion)

## Chapter 10 - Classes

* Again stepdown rule
* Classes should be small 
* The single responsibility principle (One responsibility—one reason to change)

## Chapter 11 - Systems

