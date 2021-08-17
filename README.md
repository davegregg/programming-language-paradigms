# Programming Language Paradigms
*In other words, how do we organize our code?*
*How do we manage complexity and change?*

+ What was it like to code before programming paradigms?
  - Machine languages: binary code specific to a unique combination of circuitry.
  - Not flexible. Not easy to write. Not easy to read.

+ **The Imperative Programming Paradigm**
  - "Wouldn't it be nice to be able to say that this particular combination of binary code means 'add', so that we don't have to type all those zeroes and ones?"
  - Approach? *Organize code into named commands and variables.*
  - Introduced by assembly languages (1947).
  - You wouldn't recognize much in assembly code, but you may recognize commands like `ADD`, `PUSH`, and `POP`.
  - The command "MOV" was used to move raw data manually between different locations in memory. Different memory locations served different purposes.

+ **Procedural Programming**
  - "Wouldn't it be nice if we could create our own custom commands?"
  - Approach? *Organize code into procedures/functions.*
  - Introduced by FORTRAN (1957), ALGOL 58 (1958), and COBOL (1959).
  
+ **Structured Programming**
  - "Wouldn't it be nice if we could organize the flow of our logic into groups, instead of telling the interpreter to jump to specific lines of code all over the place?"
  - Approach? *Organize code into blocks* instead of `GOTO` statements jumping to line numbers in a file.
  - Introduced by ALGOL 60 (1960)
  - This was a direct response to the famous open letter [Go To Statements Considered Harmful](https://en.wikipedia.org/wiki/Go_To_Statement_Considered_Harmful):
    > The unbridled use of the go to statement has as an immediate consequence that it becomes terribly hard to find a meaningful set of coordinates in which to describe the process progress. ...

    > The go to statement as it stands is just too primitive, it is too much an invitation to make a mess of one's program.
  - This paradigm is the first approach which really attempts to reduce the problem of "spaghetti code."
  
+ **Modular Programming**
  - Introduced by Modula (1975).
  - Approach? *Organize code into self-contained modules/files which cannot leak data accidentally.*
  - This can be seen as a natural evolution of the concept of "scope" which was prominently involved in the use of blocks in Structured Programming.
  - JavaScript in the browser historically defied this paradigm by default. Every JS file works in the same global scope. But modern browsers now support modules ([https://mdn.io/modules](https://mdn.io/modules)).

+ **Object-Oriented Programming**
  - Introduced by C++ (when it was still called "C with Classes")
  - Notably championed by Java, Ruby, and Python
  - Approach: Organizing code/behavior around data?
  - Decreasing in popularity
  
+ **Functional Programming**
  - Introduced by Lisp, inspired by Lambda Calculus (Alonzo Church, colleague of Alan Turing)
  - Approach: Organize code by controlling side-effects in a conservative way
  - Change management
  - Increasing in popularity gradually since the late 50s and especially recently.

+ An Aside on the **Declarative Programming Paradigm**
  - Examples: HTML, CSS, SQL, JSX, RegEx
  - Approach: Organize code by telling the computer what you want to be done, instead of HOW to do it.
  - The logic is expressed without explicitly describing flow control.
  - This is almost exactly the opposite approach of Imperative Programming. This isn't a bad thing. It isn't the absence of an approach: it is the reverse approach. 
  - In a way, the language provides the algorithms. We describe which algorithms we want. This is obviously much easier when the problem set is quantifiable and small; that is, in domain-specific languages.
  - This paradigm often describes a different set of languages than the general-purpose programming languages we all think of as "real" programming languages.
  - However, functional programming languages often follow the Declarative Paradigm. `map`, `filter`, `reduce`, etc., are examples of functional programming's declarative approach.

# HOW do we write in a particular paradigm for organizing our code?

- The programming language itself must prevent you from writing your code in any other way; or,
- You must be disciplined to use the features available to you to follow the paradigm.
