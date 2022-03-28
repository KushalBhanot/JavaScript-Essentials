- "let" and "const" declarations are hoisted
- "let" declarations are hoisted in JS, but you can't access such variables since they are not present in the Global object, instead they are inside a "Script" object
- You can only access "let" variables are you have declared them, otherwise you'll get a "ReferenceError"
- Temporal Dead Zone is the time between the hoisting of a "let" variable and its assignment(initialisation) in the code execution
- You cannot initialise two variables with the same name using "let". It will throw a "SyntaxError". But in the case of "var", it won't throw any error and it will move to code execution phase
- Level of Strictness: const > let > var
- You cannnot re-initialise a "const" variable. It will throw a "SyntaxError"
- You need to initialise a "const" variable when you declare it. You cannot do it later.
- If you try to re-initialise a "const" variable after you have initialised it at the declaration, then the JS engine will throw a "TypeError"
- Best practice 1: use "const" and "let" instead of "var"
- Best practice 2: always declare varibles at the top of your scope to shrink temporal dead zone

//

-> let and const are hoisted. we cant use them before initialization is result of "temporal dead zone".
-> js use diff memory than global execution context to store let and cost. which is reason behind "temporal dead zone"
-> level of strictness ... var<<let<<const.
-> var //no temporal dead zone, can redeclare and re-initialize, stored in GES
    let //use TDZ, can't re-declare, can re-initialize, stored in separate memory
    const //use TDZ, can't re-declare, can't re-initialize, stored in separate memory
-> syntax error is similar to compile error. while type and reference error falls under run time error.
-> syntax error ... violation of JS syntax
    type error ...  while trying to re-initialize const variable
    reference error ... while trying to access variable which is not there in global memory.
