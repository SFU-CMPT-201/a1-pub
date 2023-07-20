# Assignment 1: Neovim practice

In this assignment, you will practice Neovim, a text editor that we use for this course. There are three simple tasks that you need to do.

## Task 0

Before you get started, spend a few minutes and read [this article](http://www.viemu.com/a-why-vi-vim.html). There are many articles that talk about using vi and I believe it is one of the better-written articles. Don't miss the first misconception about the modal editing as it describes the correct way to use vi.

## Task 1

In this task, use `nvim` to write a `main()` function inside a file named `main.c`. The `main()` function should invoke every single function in the `lib.c` file and exit with a success exit code (`0`). To compile the code, you can enter `clang -o main main.c lib.c` which will generate an executable named `main`. There is an executable named `grader` that you can run and check your score (`./grader`). As the above linked article describes, your workflow is that "you are *always* in normal mode, and only enter insert mode for *short bursts* of typing text, after which you press <Esc> to go to normal mode."

After you're done, use `git` to push your `main.c` to your remote GitHub Classroom repo.

## Task 2
