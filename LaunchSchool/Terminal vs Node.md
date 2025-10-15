In this assignment, we're going to learn the difference between running shell commands and running JavaScript code. In particular, we'll discuss:

- how to issue shell commands in the terminal
- how to run JavaScript code from a file
- how to run JavaScript code from the `node` REPL

Be sure that you're clear on the differences between these three items before moving on to the next lesson.

## The Terminal and the Shell

You've already met the terminal and shell in our [Introduction to the Command Line](https://launchschool.com/books/command_line) book so we won't go into much detail in this section. To review, though, the **terminal** is an application on your computer that allows you to run commands by typing them at a command line. The **shell** is a program that runs in the terminal; it handles the details of interpreting the commands you enter, sends those commands to the operating system for execution, and displays the result. We may use the terms "terminal" and "shell" somewhat interchangeably, but it's worth keeping in mind that they are different things, albeit closely related. [^1]

Go ahead and open your terminal now. The resulting window should look something like this:

```terminal
Last login: Sun Nov 24 22:16:44 on ttys001
$
```

What you see on your system may differ from the above display in some ways, so don't panic. As long as you don't see anything that looks like an error message, you should be fine.

If you are using the bash shell, the `$` on the second line is the shell's way of telling us that it's waiting for us to do something. Note that your shell may not display a `$`, and that's probably okay; you may have a different prompt configuration. However, if you see a `#` instead of a `$`, you may be logged in as `root`; that's usually not wise. If you are logged in as `root`, you should logout and log back in as a regular user.

If you see a `%` prompt, you may be using the zsh shell. Recent versions of macOS now use the zsh shell as the default shell for Terminal sessions. For the most part, the zsh and bash shells are very similar -- most everything you can do in one you can do in the other.

If you aren't sure which shell you're using, run the following command:

Copy Code

```terminal
echo $SHELL
```

In the above command, the `$` at the beginning of the line represents the shell prompt. We'll almost always show the shell prompt in this manner. If you're not using bash or have a customized prompt, you'll see something else. Regardless of what your terminal displays, just remember that the `$` shown before shell commands is not part of the command that you should enter.

Okay, the shell is waiting for us to enter a command. We'll start with something simple and take a look at what's in the current directory:

```terminal
$ ls
Applications  Documents  Library  Music     Public  TT-RX  func
Desktop       Downloads  Movies   Pictures  Sites   bin    x.js
```

The command we entered, in this case, is the `ls` command. As you may recall, `ls` is the "list files" command. It lists all of the files and subdirectories of the current directory, which, in this case, is probably your **home directory**. In the output, we can see 14 files and subdirectories.

If you are using GitHub Codespaces, your initial directory may be something like `/workspaces/codespaces-blank`. This is **not** your home directory, but is where you should place any code you write. For the most part, you can treat this directory as your home directory. However, your home directory is really `/home/codespaces`.

If you are using AWS Cloud9, your initial directory is a subdirectory of your home directory called `environment`. For the most part, you can treat `environment` as your home directory. However, your home directory is really the parent directory of `environment`.

Cloud9 is no longer available to new customers. Please see [this post](https://launchschool.com/posts/431a3e9d) for more information.

After entering a command at the shell prompt, be sure to press your Return or Enter key. The only way the shell can tell that you're done typing is when it detects that the Return or Enter key was pressed. Without it, the shell will continue waiting for more input.

Let's create a new, empty subdirectory and make that our current directory:

```terminal
$ mkdir projects
$ ls
Applications  Downloads  Music     Sites  func
Desktop       Library    Pictures  TT-RX  projects
Documents     Movies     Public    bin    x.rb
$ cd projects
$ ls
```

The first command creates a new subdirectory named `projects` in our current directory. The fact that we don't see any error messages is our only hint that the command worked. To be sure, though, we run the `ls` command again; we can see the new `projects` subdirectory in the output.

The third command sets the current directory to the `projects` subdirectory. When we run the `ls` command this time, we can see that the directory is empty.

## Running a JavaScript Program File

Let's create an elementary JavaScript program. We'll call it `hello-world.js`. We'll start by using the `touch` command to create it.

Copy Code

```terminal
touch hello-world.js
```

Once again, the only indication that the command worked is that there are no error messages. You can confirm that it worked by running the `ls` command once more:

```terminal
$ ls
hello-world.js
```

Using `touch` to create isn't necessary; most editors can create new files themselves. However, when you use the editor, it's easy to make a mistake and put the new file in the wrong directory. If you do that, you may spend some time trying to find the file.

Next, use your editor to open the `hello-world.js` file. You may have to navigate the editor's open file dialog to the `projects` directory. Alternatively, you may be able to open the file directly from the command line. For instance, VS Code provides a `code` command that you can use at the command line:

Copy Code

```terminal
code hello-world.js
```

If you're not using VS Code, the command will be different. With some editors, you may need to install a set of command-line tools; with others, there may not be a command-line equivalent at all.

Once you've opened the file, place the following code in the file and save it:

hello-world.js

Copy Code

```js
console.log("Hello, World!");
```

Go back to the terminal window and run the program by using the `node hello-world.js` command:

```terminal
$ node hello-world.js
Hello, World!
```

This technique is how you'll run most JavaScript code in our curriculum; learn it well!

## Running JavaScript Code in a REPL

You can also run JavaScript code one line at a time in the Node **REPL** (short for **Read, Evaluate, Print, Loop**). In short, a REPL is a program that reads input from the user, evaluates the input, prints the results, and then loops back to wait for more input.

The shell is a REPL for system commands, but the `node` command is a REPL for JavaScript code. It lets us enter code one line at a time, evaluates the code, then displays the results before looping back to await more input:

```terminal
$ node
> console.log("Hello, World!")
Hello, World!
undefined
> 3 + 4
7
> Control-D # (press and hold the Control or Ctrl key
            # and the D key at the same time)
            # Control-C also works.
$
```

Here we see two JavaScript expressions being entered into the `node` REPL and then executed. The first expression, `console.log("Hello, World!")`, outputs `Hello, World!` and _returns_ `undefined` (we'll discuss that distinction later). The second expression, `3 + 4`, doesn't print anything, but it returns a value of `7`. Finally, we terminate the REPL and return to the shell by pressing `Control-D` or `Control-C`.

Note that we show the `node` REPL's prompt as `>`. You may see a different prompt.

It's important to realize that the shell REPL and the `node` REPL are **not** the same thing. The shell REPL executes system commands, while the `node` REPL executes JavaScript. You can't use the shell to execute JavaScript, and you can't use `node` to execute system commands:

```terminal
$ console.log("Hello, World!");
-bash: !": event not found
```

```terminal
$ node
> ls
Thrown:
ReferenceError: ls is not defined
```

The REPL is ideal for testing how a single line of JavaScript code works. Learn to use it as you learn to code whenever you're uncertain of what some code will do. You can avoid many program bugs if you first make sure that you're getting the results that you expect.

## Recap

Use the shell command-line to run system commands. Many (but not all) system commands concern themselves with files and directories, system configuration, and starting other programs (like editors and REPLs for programming languages like JavaScript). The shell doesn't know how to run JavaScript code, or that of any other programming language.

To execute JavaScript code that is in a file, use the `node` command with the file's name as an argument, e.g.:

Copy Code

```terminal
node do-something.js
```

It's important to remember that running JavaScript code like this **does not** display any return values; just the output of the code.

If you want to run JavaScript code a single line at a time, you can use the `node` REPL by executing the `node` command with no arguments:

```terminal
$ node
> console.log("Hello");
```

Unlike running JavaScript code from a file, using the REPL displays both the output of the code and the return values.
# Footnotes

[^1]: The difference between the terminal and shell - terminal is the application, shell is the program