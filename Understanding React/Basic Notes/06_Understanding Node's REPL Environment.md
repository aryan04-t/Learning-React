# Node.js REPL Environment

## What is REPL?

**REPL** stands for Read-Eval-Print Loop. It is a simple, interactive programming environment that allows you to execute JavaScript code line by line and see the results immediately.

## How to Access REPL?

You can access the Node.js REPL environment by simply typing `node` in your terminal and pressing Enter. This will start the REPL, and you can begin executing JavaScript code.

## Basic Commands in Node.js REPL:

1. **Running JavaScript Code**:
   - Simply type JavaScript code and press Enter to execute it. For example:
     ```
     > 2 + 3
     5
     ```

2. **Getting Last Executed Output**:
   - You can use the underscore `_` to get the result of the last expression executed in the REPL. For example:
     ```
     > 10 * 5
     50
     > _
     50
     ```

3. **Multi-line Statements**:
   - You can write multi-line JavaScript statements in the REPL. To enter a multi-line statement, press Enter after the incomplete statement. For example:
     ```
     > function add(a, b) {
     ... return a + b;
     ... }
     ```

4. **Exiting REPL**:
   - To exit the Node.js REPL, you can type `.exit` or press `Ctrl + C` twice.

5. **Help Command**:
   - You can type `.help` in the REPL to get a list of all available commands and special keys.

## Summary

- **REPL**: Provides an interactive JavaScript environment for quickly testing code snippets.
- **Basic Commands**: Include running JavaScript code, getting last executed output, handling multi-line statements, and exiting the REPL. 