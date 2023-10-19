# C - Stacks, Queues - LIFO, FIFO

The Monty Bytecode Interpreter is a program written in C programming language that reads and executes Monty bytecode files. Monty is a simple programming language that uses a stack data structure.

## Objectives:
* To know what LIFO and FIFO mean
* To know what a stack is, and when to use it
* To know what a queue is, and when to use it
* To know the common implementations of stacks and queues
* To know the most common use cases of stacks and queues
* To know the proper way to use global variables

## Compilation & Output
* These codes were compiled using: ```gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty```
* Any output must be printed on ```stdout```
* Any error message must be printed on ```stderr```

## Examples
```
julien@ubuntu:~/monty$ cat -e bytecodes/000.m
push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$
julien@ubuntu:~/monty$
```
Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:
```
julien@ubuntu:~/monty$ cat -e bytecodes/001.m
push 0 Push 0 onto the stack$
push 1 Push 1 onto the stack$
$
push 2$
  push 3$
                   pall    $
$
$
                           $
push 4$
$
    push 5    $
      push    6        $
$
pall This is the end of our program. Monty is awesome!$
julien@ubuntu:~/monty$
```
# Examples

Here's an example Monty bytecode file that adds two numbers:
```
push 5
push 10
add
pall
```
When executed, the above bytecode will output: `15`

