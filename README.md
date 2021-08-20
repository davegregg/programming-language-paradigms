# Programming Language Paradigms
*In other words, how do we organize our code?*
*How do we manage complexity and change?*

+ What was it like to code before programming paradigms?
  - Machine languages: binary code specific to a unique combination of circuitry.
  - Negatives?
    - Not easy to write.
    - Not easy to read.
    - Time consuming to work with.
    - Zero versatility.
  - Benefits?
    - Maximum control.
    - Maximum access to hardware features.
    - Maximum performance when used well.

+ **The Imperative Programming Paradigm**
  - "Wouldn't it be nice to be able to say that this particular combination of binary code means 'add', so that we don't have to type all those zeroes and ones?"
  - Approach? *Organize code into named commands/operators and variables.*
  - Introduced by assembly languages (1947).
  - You wouldn't recognize much in assembly code, but you may recognize commands like `ADD`, `PUSH`, and `POP`.
  - The command "MOV" was used to move raw data manually between different locations in circuitry, serving different purposes.

+ **Procedural Programming**
  - "Wouldn't it be nice if we could create our own custom commands?" Brilliant!
  - Approach? *Organize code into procedures/functions.*
  - Introduced by FORTRAN (1957), ALGOL (1958), and COBOL (1959).
  
+ **Structured Programming**
  - "Wouldn't it be nice if we could organize the flow of our logic into groups, instead of telling the interpreter to jump around to specific lines of code?"
  - Approach? *Organize code into blocks.*
  - This paradigm is the first approach which really attempts to reduce the problem of "spaghetti code."
  - Introduced by ALGOL (1960)
  - This was a direct response to the famous open letter [Go To Statements Considered Harmful](https://en.wikipedia.org/wiki/Go_To_Statement_Considered_Harmful):
    > The unbridled use of the `go to` statement has as an immediate consequence that it becomes terribly hard to find a meaningful set of coordinates in which to describe the process progress. ... The `go to` statement as it stands is just too primitive, it is too much an invitation to make a mess of one's program.
  
+ **Modular Programming**
  - Introduced by Modula (1975).
  - Approach? *Organize code into self-contained modules/files, with explicit inputs and outputs, meaning that the programmer decides which data or behavior their program can access and expose.*
  - This can be seen as a natural expansion of the concepts of "functions" and "scope" from Procedural and Structured Programming, respectively.
  - JavaScript in the browser historically did not provide a first-class modules feature. Every JS file works in the same global scope, by default. In order to follow the Modular Programming Paradigm, we used [IIFEs](https://developer.mozilla.org/en-US/docs/Glossary/IIFE#the_module_pattern) (pronounced "if-fee", like "iffy"), which simply uses a function to accomplish the same task.
  - However, modern browsers now support first-class modules ([https://mdn.io/modules](https://mdn.io/modules)).
  - And backend implementations of JavaScript have had first-class modules since Node.js was released in 2009.

+ **Object-Oriented Programming**
  - Introduced by C++ (when it was still called "C with Classes")
  - Notably championed by Java, Ruby, and Python
  - Approach: *Organize code by coupling behavior to data*
  - There is growing frustration with Object-Oriented Programming as an approach to managing complexity, because the approach itself seems either to introduce its own complexity at larger scales or else does not sufficiently constrain programmers from making code organization decisions which are likely to cause significant architectural and semantic trouble later.
  - Gradually losing favor in the community
  
+ **Functional Programming**
  - Introduced by Lisp, inspired by Lambda Calculus (Alonzo Church, colleague of Alan Turing)
  - Approach: *Organize code by decoupling behavior from data* (controlling side-effects in a conservative way)
  - A way of managing IO differently: inputs and outputs occur at the "edges" of a system. Let's acknowledge this as an architectural philosophy. We isolate the code which does not need to interact with inputs and outputs in the middle of the system, pushing IO concerns explicitly to the edge of the system.
  - Steadily increasing in popularity gradually since the late 50s and especially in the last decade.

+ An Aside on the **Declarative Programming Paradigm**
  - Examples: HTML, CSS, SQL, JSX, RegEx
  - Approach: *Organize code by telling the computer what you want to be done, instead of HOW to do it.*
  - This means that the logic is expressed without explicitly describing flow control. The programmer does not usually control the order in which things occur, though they may specify *priorities.*
  - This is almost exactly the opposite approach of Imperative Programming. This isn't a bad thing. It isn't the absence of an approach: it is the reverse approach.
  - In a way, the language provides all of the algorithms. Then we describe which algorithms we want to use or configure. This is obviously much easier when the problem set is quantifiable and small; that is, in domain-specific languages.
  - For this reason, the Declarative paradigm often describes a different set of languages than the general-purpose programming languages we all think of as "real" programming languages.
  - However, the Functional Paradigm tends to work well together with the Declarative Paradigm, and has introduced Declarative features into many programming languages which would normally be considered Imperative languages. `map`, `filter`, and `reduce` are examples of this.

# HOW do we write in a particular paradigm for organizing our code?

- The programming language itself must prevent you from writing your code in any other way; or,
- You must be disciplined to use the features available to you to follow the paradigm.
