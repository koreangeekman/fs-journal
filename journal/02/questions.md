# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > | var let const |

02. What is the definition of a function?

    > | a set of instructions intended for a specific purpose; reusable block of code for processing instructions  |

03. What are the `SOLID` principles?

    > | 
    "SOLID Principles:
        Single Responsibility Principle (SRP)
        Open-Close Principle (OCP)
        Liskov Substitution Principle (LSP)
        Interface Segregation Principle (ISP)
        Dependency Inversion Principle (DIP) 
    aka
    S - Singular purpose
    O - fixed but interoperable design
    L - Make parent classes representable of child elements ie. Fruits:Apples Fruits:Oranges  
    I - reduce the breadth of client facing interfaces - they don't need access to all aspects of the program if they only need to turn it on/off and reset for maintenance
    D - complete Division of the high/low level modules, interact only via abstractions - removes dependency ties between high/low levels
    |

04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    ```

    > | 
    ```js
    fruit.splice(fruit.indexOf('pineapple'),1)
    ```
     |

05. Given these two objects: How could you add each to the others friends arrays?

    ```js
    let you = {
        name: "You",
        hair: true,
        friends: []
    }
    let them = {
        name: "Them",
        hair: false,
        friends: []
    }
    ```

    > | ANSWER HERE |

06. Give an example of a JavaScript `Conditional`:

    > |
    ```js
    let sky = 'blue' 
    if ( sky == 'blue' ) {
        return true
    } else {
        return 'the sky is falling!'
    }
    ```
    |

07. What is the main difference between `parameters` and `arguments`?

    > | parameters are the variables for a function, arguments are passed to the function to be used in those variables |

08. Instead of writing everything to the console, what is a better way to debug your code?

    > | ANSWER HERE |

09. What is the difference between a `primitive` value and a `reference` value?

    > | 
    primitive values = numbers, boolean, null, undefined, string (basic types data)
    reference values = objects, arrays, functions (referential types of data)
     |

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > | 
    ```js
    let i = -100;
    while (i <= 100){
        console.log(i);
    }
    ```
     |
