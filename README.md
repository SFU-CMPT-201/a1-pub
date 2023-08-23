# Assignment 1: Neovim practice

From now on, we will assume that you know how to use the command-line interface. This means that we
will not spell out the commands that you need to use. For example, we will just state that you need
to be in a certain directory instead of telling you what to enter, or that you need to clone a repo
instead of telling you which Git commands to use. You may still feel that you are not comfortable
with the command-line interface. As mentioned previously, open a cheat sheet in your browser and
keep looking up the commands throughout the semester. You will be very comfortable with the
command-line interface by the end of the semester.

Now, one of the most important tools for programming is an editor. There are many editors out there
and developers have their particular preferences. As you know already, this course uses Neovim, one
of the modern implementations of vi. One reason for the choice of vi/Neovim is the course's goal of
providing an immersive terminal-based Linux environment. Vi is available on pretty much all
terminal-based, Unix-like systems and if you know how to use it, along with the command-line
interface, you will have no trouble using any Unix-like systems out there. Another reason for the
choice of vi/Neovim is that it shows a unique editor design based on modes (which you have
experienced already in the previous assignment). We believe that this is intellectually stimulating
since it shows that it is possible to design software from a very different angle. In fact, the
original creator of vi is Bill Joy, a legendary programmer who led the development of Berkeley Unix
(BSD), which has many modern descendants including Apple's OSs like macOS and iOS.

Although you had a chance to use Neovim in the previous assignment, you probably still feel that you
are not very good at it yet. It will take time to get really comfortable with Neovim. But you will
have a lot of opportunities to practice it in this course, including this assignment. We are
confident that you will be an expert in vi/Neovim by the end of this semester.

In this assignment, there are three simple tasks that you need to do.

## Task 0: Reading an article

Before you get started, spend a few minutes and read [this
article](http://www.viemu.com/a-why-vi-vim.html). There are many articles that talk about using vi
and I believe it is one of the better-written articles. Don't miss the first misconception about the
modal editing as it describes the correct way to use vi.

## Task 1: Swapping `<Caps Lock>` and `<Esc>`

We highly recommend you to swap your `<Caps Lock>` key with your `<Esc>` key. You need to use
`<Esc>` heavily on vi, and swapping `<Caps Lock>` with `<Esc>` makes it easier. In fact, this was
the original keyboard layout at the time of vi's development. You don't typically use `<Caps Lock>`
anyways, so this won't affect your keyboard usage much. For Windows, install
[PowerToys](https://github.com/microsoft/PowerToys) by Microsoft, go to the Keyboard Manager, and
remap the keys. For MacOS, go to System Settings --> Keyboard --> Keyboard Shortcuts --> Modifier
Keys, and change the mapping for `<Caps Lock>`. For a Linux distro using GNOME, install
`gnome-tweaks` with your package manager (e.g., `apt`, `dnf`, etc.), go to Keyboard & Mouse -->
Additional Layout Options --> Caps Lock behaviour, and choose the mapping. For a Linux distro using
KDE, go to System Settings --> Input Devices --> Keyboard --> Advanced --> Caps Lock behavior, and
choose the mapping.

## Task 2: Neovim tutorial

In this task, use Neovim to follow a tutorial.

* First, make sure you are in the correct directory for this assignment (`a1`).
* Start `nvim`. You do not need to open any file.
* Once `nvim` starts, enter `:Tutor`, which will start the built-in tutorial.
* The tutorial will ask you to modify the content, and so after finishing the tutorial, save the
  content of the tutorial (including your modifications) to a new file named `tutor` (if you finish
  the tutorial, you will know how to save the content you're editing to a new file). Remember, as
  the above linked article describes, your workflow is that "you are *always* in normal mode, and
  only enter insert mode for *short bursts* of typing text, after which you press `<Esc>` to go to
  normal mode." So develop a habit of hitting the `<Esc>` key.
* After you're done, use `git` to push your `tutor` file to your remote GitHub Classroom repo.

# Tips

There are many good online webpages that you can use to quickly look up vi commands. We highly
recommend you to open one of those in your browser and keep it in the background throughout the
semester, so you can easily find the commands that you want to use. For example,
[this](https://vim.rtorr.com) is a good one to use. Since vi has many more useful commands that the
tutorial does not mention, you can try out the commands that the above linked cheat sheet describes.
There is also an extensive list of resources available at [Vim Tips
Wiki](https://vim.fandom.com/wiki/Vim_documentation).

# Other features

Neovim is extremely customizable with a long list of built-in options. Not only that, it allows us
to install third-party plugins. Using these, we have configured Neovim with a few more features and
you are encouraged to try these out and use them.

* The status line at the bottom comes from a plugin called
  [lightline](https://github.com/itchyny/lightline.vim).
* `<Ctrl>-h` (the control key and h) in normal mode opens a file explorer called
  [nvim-tree](https://github.com/nvim-tree/nvim-tree.lua). Once you open it, type `g?` opens a help
  page. But basically, you can use vim's key navigation (e.g., `j` and `k`) to navigate and
  `<Enter>` to open the file you select. `q` exits nvim-tree.
* When you open a new file using nvim-tree, it opens the file in a new *buffer*, which is roughly
  similar to a new tab in a web browser. At the top of your terminal window/tab, you will see that
  Neovim shows your current buffers, which comes from a plugin called
  [lightline-bufferline](https://github.com/mengelbrecht/lightline-bufferline).
* You can type `:bn` (*b*uffer *n*ext) to go to the next buffer, `:bp` (*b*uffer *p*revious) or
  `:bN` to go to the previous buffer, and `:bd` (*b*uffer *d*elete) to delete the current buffer.
* Typing `:Files` in normal mode opens a file finder using
  [fzf.vim](https://github.com/junegunn/fzf.vim), which is a plugin that integrates Neovim and fzf,
  the fuzzy finder we have mentioned before in the previous assignment. Using this, you can quickly
  find a file that you want to open. fzf.vim has many more features, so you might want to explore it
  further.
* We have installed a plugin called [vim-sneak](https://github.com/justinmk/vim-sneak), which allows
  us to quickly jump to a different location on the screen. To use it, type `s` in normal mode
  followed by two characters of the word that you want to jump to. It will immediately jump to the
  first match and show other options highlighted with a different color and a shortcut key. Typing
  one of the shortcut keys allows you to jump to a different option. `s` is for jumping forward and
  `S` is for jumping backward.

For our VM, we do not allow you to install any more plugins. We have actually configured our VM in a
way that prevents you from installing other plugins. This is first for learning purposes but also
because installing too many plugins slows down the performance of Neovim. Many Vim/Neovim users
prefer installing a minimal number of plugins that they consider essential and use the native
features of Vim/Neovim for the most part.

# Important note

For all future assignments, you *must* use `nvim`. To enforce this, we have configured our `nvim` so
that, for a few file types that we care about (e.g., `.c`, `.h`, `.sh`, etc.), it occasionally takes
a snapshot of the file you are editing and saves the snapshot to a directory named `.nvim`. For all
future assignments, you need to push this directory as part of your submission. We will check this
directory, analyze the snapshots to make sure that you are using `nvim`, and use the analysis
results as part of grading.

# Next steps

You need to accept the invite for the next assignment (A2).

* Go to this URL: [https://classroom.github.com/a/PGPiPLGw](https://classroom.github.com/a/PGPiPLGw)
* Accept the invite for Assignment 2 (A2).
* If you are not in `units/02-tools` directory, go to that directory.
* Clone the assignment repo.
