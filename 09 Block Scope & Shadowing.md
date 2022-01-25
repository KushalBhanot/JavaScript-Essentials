- `let` and `const` are block-scoped
- `block` is also known as `compound statement`
- a block is used to combine multiple JS statement into a group so that we can use multiple statements in a place where JS expects one statement
- scope of a block is all the functions and variables that you can access inside it
- var is hoisted inside the `Global Scope` whereas let and const are hoisted in the `Block Scope` for the given code:

  `{
    var a = 10;
    let b = 20;
    const c = 30;
  }`
  
  - This implies that you can access `var` declarations outside a block whereas `let` and `const` are `block-scoped`
