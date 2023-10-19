# C - Stacks, Queues - LIFO, FIFO

The Monty Bytecode Interpreter is a program written in C programming language that reads and executes Monty bytecode files. Monty is a simple programming language that uses a head_stack data structure.

## Objectives:
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

* What do LIFO and FIFO mean
* What is a head_stack, and when to use it
* What is a queue, and when to use it
* What are the common implementations of stacks and queues
* What are the most common use cases of stacks and queues
* What is the proper way to use global variables

## Compilation & Output
* These codes were compiled using: ```gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty```

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
push 0 Push 0 onto the head_stack$
push 1 Push 1 onto the head_stack$
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

