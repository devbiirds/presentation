# presentation-Q3-2019  
My name is Minakov Vadim.  
###### (Slide - TypeScript)
TypeScript is an open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing to the language.
TypeScript is designed for development of large applications and transcompiles to JavaScript As TypeScript is a superset of JavaScript, existing JavaScript programs are also valid TypeScript programs. TypeScript may be used to develop JavaScript applications for both client-side and server-side (Node.js, Deno) execution.
TypeScript supports definition files that can contain type information of existing JavaScript libraries, much like C++ header files can describe the structure of existing object files. This enables other programs to use the values defined in the files as if they were statically typed TypeScript entities. There are third-party header files for popular libraries such as jQuery, MongoDB, and D3.js. TypeScript headers for the Node.js basic modules are also available, allowing development of Node.js programs within TypeScript.[8]
The TypeScript compiler is itself written in TypeScript and compiled to JavaScript. It is licensed under the Apache License 2.0. 
###### (Slide - History)
TypeScript was first made public in October 2012 (at version 0.8), after two years of internal development at Microsoft.Soon after the announcement, Miguel de Icaza praised the language itself, but criticized the lack of mature IDE support apart from Microsoft Visual Studio, which was not available on Linux and OS X at that time Today there is support in other IDEs, particularly in Eclipse, via a plug-in contributed by Palantir Technologies.Various text editors, including Emacs, Vim, Sublime, Webstorm, Atom] and Microsoft's own Visual Studio Code also support TypeScript
TypeScript 0.9, released in 2013, added support for generics, TypeScript 1.0 was released at Microsoft's Build developer conference in 2014.] Visual Studio 2013 Update 2 provides built-in support for TypeScript
In July 2014, the development team announced a new TypeScript compiler, claiming 5× performance gains. Simultaneously, the source code, which was initially hosted on CodePlex, was moved to GitHub.
On 22 September 2016, TypeScript 2.0 was released; it introduced several features, including the ability for programmers to optionally prevent variables from being assigned null values, sometimes referred to as the billion-dollar mistake.
###### (Slide - Design)
TypeScript originated from the shortcomings of JavaScript for the development of large-scale applications both at Microsoft and among their external customers. Challenges with dealing with complex JavaScript code led to demand for custom tooling to ease developing of components in the language.[29]
TypeScript developers sought a solution that would not break compatibility with the standard and its cross-platform support. Knowing that the current ECMAScript standard proposal promised future support for class-based programming, TypeScript was based on that proposal. That led to a JavaScript compiler with a set of syntactical language extensions, a superset based on the proposal, that transforms the extensions into regular JavaScript. In this sense TypeScript was a preview of what to expect of ECMAScript 2015. A unique aspect not in the proposal, but added to TypeScript, is optional static typing that enables static language analysis, which facilitates tooling and IDE support.
###### (Slide - Additional features)
-	Type annotations and compile-time type checking
-	Type inference
-	Type erasure
-	Interfaces
-	Enumerated types
-	Generics
-	Namespaces
-	Tuples
-	Async/await  
###### (Slide - The following features are backported from ECMAScript 2015)
-	Classes
-	Modules
-	Abbreviated "arrow" syntax for anonymous functions
-	Optional parameters and default parameters
Syntactically, TypeScript is very similar to JScript .NET, another Microsoft implementation of the ECMA-262 language standard that added support for static typing and classical object-oriented language features such as classes, inheritance, interfaces, and namespaces.
  
###### (Slide - Type annotations)
TypeScript provides static typing through type annotations to enable type checking at compile time. This is optional and can be ignored to use the regular dynamic typing of JavaScript.

`function add(left: number, right: number): number {`
	`return left + right;	`
`}`

The annotations for the primitive types are number, boolean and string. Weakly- or dynamically-typed structures are of type any.
Type annotations can be exported to a separate declarations file to make type information available for TypeScript scripts using types already compiled into JavaScript. Annotations can be declared for an existing JavaScript library, as has been done for Node.js and jQuery.
The TypeScript compiler makes use of type inference to infer types when types are not given. For example, the add method in the code above would be inferred as returning a number even if no return type annotation had been provided. This is based on the static types of left and right being numbers, and the compiler's knowledge that the result of adding two numbers is always a number. However, explicitly declaring the return type allows the compiler to verify correctness.
If no type can be inferred because of lack of declarations, then it defaults to the dynamic any type. A value of the any type supports the same operations as a value in JavaScript and minimal static type checking is performed for operations on any values.
###### (Slide - Declaration files) 
When a TypeScript script gets compiled there is an option to generate a declaration file (with the extension .d.ts) that functions as an interface to the components in the compiled JavaScript. In the process the compiler strips away all function and method bodies and preserves only the signatures of the types that are exported. The resulting declaration file can then be used to describe the exported virtual TypeScript types of a JavaScript library or module when a third-party developer consumes it from TypeScript.
The concept of declaration files is analogous to the concept of header file found in C/C++.
`declare namespace arithmetics {
    add(left: number, right: number): number;
    subtract(left: number, right: number): number;
    multiply(left: number, right: number): number;
    divide(left: number, right: number): number;
}`
Type declaration files can be written by hand for existing JavaScript libraries, as has been done for jQuery and Node.js.
Large collections of declaration files for popular JavaScript libraries are hosted on GitHub in DefinitelyTyped.
###### (Slide - Classes)
TypeScript supports ECMAScript 2015 classes that integrate the optional type annotations support.
###### (Slide - Generics) 
TypeScript supports generic programming.
`function doSomething<T>(arg: T): T {`
    `return arg;`
`}`
Modules and namespaces
TypeScript distinguishes between modules and namespaces. Both features in TypeScript support encapsulation of classes, interfaces, functions and variables into containers. Namespaces (formerly internal modules) utilize immediately-invoked function expression of JavaScript to encapsulate code, whereas modules (formerly external modules) leverage JavaScript library patterns to do so (AMD or CommonJS). 
###### (Slide - Compiler)  
The TypeScript compiler, named tsc, is written in TypeScript. As a result, it can be compiled into regular JavaScript and can then be executed in any JavaScript engine (e.g. a browser). The compiler package comes bundled with a script host that can execute the compiler. It is also available as a Node.js package that uses Node.js as a host.
There is also an alpha version of a client-side compiler in JavaScript, which executes TypeScript code on the fly, upon page load.[36]
The current version of the compiler supports ECMAScript 5 by default. An option is allowed to target ECMAScript 2015 to make use of language features exclusive to that version (e.g. generators). Classes, despite being part of the ECMAScript 2015 standard, are available in both modes.
