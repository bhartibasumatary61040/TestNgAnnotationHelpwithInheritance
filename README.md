
overview:
  description: >
    This project demonstrates how Java Inheritance works together with
    TestNG annotations. It explains constructor chaining using the
    super keyword, method execution flow, and TestNG lifecycle
    annotations like @BeforeMethod, @Test, and @AfterMethod.

technology:
  language: Java
  framework: TestNG
  java_version: 17

objective:
  - Understand Inheritance in Java
  - Understand constructor chaining using super()
  - Learn TestNG lifecycle annotations
  - Understand execution order of methods
  - Practice OOP concepts with arithmetic operations

project_structure:

  PS.java:
    role: Base Parent Class
    explanation: >
      This class contains common reusable methods and TestNG lifecycle
      annotations. It acts as the main parent class.

    contains:
      - doThis(): Prints a message from PS class
      - @BeforeMethod beforeRun(): Runs before each test method
      - @AfterMethod afterRun(): Runs after each test method

  PS1.java:
    role: Test Class (Child of PS)
    explanation: >
      This class extends PS and contains the actual @Test method.
      It creates an object of PS2 and executes arithmetic operations.
      It also inherits BeforeMethod and AfterMethod from PS.

    contains:
      - @Test testRun(): Executes increment, decrement,
                         multiplyTwo and multiplyThree methods

  PS2.java:
    role: Child Class (Extends PS3)
    explanation: >
      This class demonstrates constructor chaining.
      It uses super(a) to call the constructor of PS3.
      It contains increment and decrement logic.

    contains:
      - increment(): Increases value by 1
      - decrement(): Decreases value by 1

  PS3.java:
    role: Parent Class of PS2
    explanation: >
      This class contains multiplication logic.
      It provides reusable arithmetic methods
      that are inherited by PS2.

    contains:
      - multiplyTwo(): Multiplies value by 2
      - multiplyThree(): Multiplies value by 3

execution_flow:
  step_1: @BeforeMethod runs first (from PS class)
  step_2: @Test method runs (from PS1 class)
  step_3: increment() executes
  step_4: decrement() executes
  step_5: multiplyTwo() executes
  step_6: multiplyThree() executes
  step_7: @AfterMethod runs last (from PS class)

key_concepts:
  - Inheritance
  - Constructor chaining
  - super keyword
  - Method reuse
  - TestNG lifecycle management
  - Object-Oriented Programming (OOP)

how_to_run:
  - Install Java 17
  - Add TestNG dependency
  - Right click on PS1.java
  - Run as TestNG Test
