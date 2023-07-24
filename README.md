# Assignment 1: Neovim practice

From now on, we will assume that you know how to use the command-line interface. This means that we will not spell out the commands that you need to use. For example, if you need to be in a certain directory, we will just say that you need to be in that directory instead of telling you what to enter. You may still feel that you are not comfortable with the command-line interface. As mentioned previously, open a cheat sheet in your browser and keep looking up the commands throughout the semester. You will be very comfortable with the command-line interface by the end of the semester.

Now, one of the most important tools for programming is an editor. There are so many editors out there and developers have their particular preferences. As you know already, this course uses Neovim, one of the modern implementations of vi. One reason for the choice of vi/Neovim is the course's goal of providing an immersive terminal-based Linux environment. Vi is available on pretty much all terminal-based, Unix-like systems and if you know how to use it, along with the command-line interface, you will have no trouble using any Unix-like system out there. Another reason for the choice of vi/Neovim is that it shows a unique editor design based on modes (which you have experienced already in the previous assignment). We believe that this is intellectually stimulating since it shows that it is possible to design software from a very different angle. In fact, the original creator of vi is Bill Joy, a legendary programmer who led the development of Berkeley Unix (BSD), which has many modern descendants including Apple's OSes like macOS and iOS.

Although you had a chance to use Neovim in the previous assignment, you probably still feel that you are not very good at it yet. It will take time to get really comfortable with Neovim. But you will have a lot of opportunities to practice it in this course, including this assignment. We are confident that you will be an expert in vi/Neovim by the end of this semester.

In this assignment, there are three simple tasks that you need to do.

## Task 0

Before you get started, spend a few minutes and read [this article](http://www.viemu.com/a-why-vi-vim.html). There are many articles that talk about using vi and I believe it is one of the better-written articles. Don't miss the first misconception about the modal editing as it describes the correct way to use vi.

## Task 1

We highly recommend you to swap your <Caps Lock> key with your <Esc> key. You need to use <Esc> heavily on vi, and swapping <Caps Lock> with <Esc> makes it easier. In fact, this was the original keyboard layout at the time of vi's development. You don't typically use <Caps Lock> anyways, so this won't affect your keyboard usage much. For Windows, install [PowerToys](https://github.com/microsoft/PowerToys) by Microsoft, go to the Keyboard Manager, and remap the keys. For MacOS, go to System Settings --> Keyboard --> Keyboard Shortcuts --> Modifier Keys, and change the mapping for <Caps Lock>. For a Linux distro using GNOME, install gnome-tweaks with your package manager (e.g., `apt`, `dnf`, etc.), go to Keyboard & Mouse --> Additional Layout Options --> Caps Lock behaviour, and choose the mapping. For a Linux distro using KDE, go to System Settings --> Input Devices --> Keyboard --> Advanced --> Caps Lock behavior, and choose the mapping.

## Task 2

In this task, use Neovim to follow a tutorial. First, make sure you are in the correct directory for this assignment (`a1`). Start `nvim`. You do not need to open any file. Once `nvim` starts, enter `:Tutor`, which will start the built-in tutorial. The tutorial will ask you to modify the content, and so after finishing the tutorial, save the content of the tutorial (including your modifications) to a new file named `tutor` (if you finish the tutorial, you will know how to save the content to a new file). Remember, as the above linked article describes, your workflow is that "you are *always* in normal mode, and only enter insert mode for *short bursts* of typing text, after which you press <Esc> to go to normal mode."

After you're done, use `git` to push your `tutor` file to your remote GitHub Classroom repo.

## Tips

There are many good online webpages that you can use to quickly look up vi commands. We highly recommend you to open one of those in your browser and keep it in the background throughout the semester, so you can easily find the commands that you want to use. For example, [this](https://vim.rtorr.com) is a good one to use. Since vi has many more useful commands that the tutorial does not mention, you can try out the commands that the above linked cheat sheet describes. There is also an extensive list of resources available at [Vim Tips Wiki](https://vim.fandom.com/wiki/Vim_documentation).
