# FastFinder
_Find things. Fast._

**FastFinder** is command line tool to help navigate through large codebases (think 10GB+). It works by first storing all file names found within a directory into a cache. **FastFinder** executes case-insensitive `grep` on this cache and displays the results to the user. Selection is done by entering the number next to the result, which will prepend the path by any command passed by the user.

![Example usage](https://github.com/Martiul/FastFinder/raw/master/ff_sample.png "UML Diagram" "Example usage")

This makes finding and opening a file in your favourite text editor an easy two-step process. The flexibility of **FastFinder** also makes it really easy to use commands like `p4 edit` and `git diff` on specific files. The default command for **FastFinder** is `vim`.

**FastFinder** primarily serves as an alternative to running multiple `find` commands or text editor search features.
This tools also works well with `ctags` and `cscope` which work in a similar manner.

## Sample Usage
```
# Quick start
ff -init
ff QUERY  # Searches for files matching QUERY
```

```
# Change the command for this query only
ff -cmd=emacs QUERY
```

```
# Change the default command for queries
ff -set-default="git diff"
ff -config      # View the current default command
```

## Installation Instructions
1. Download the `ff` file located here and place it in a directory of your choosing (I will use `~/.tools` in this example)
2. Add the directory with `ff` to your `PATH`. Remember to refresh your profile (e.g. `source ~/.bashrc`)
```
# Example: Add the following line to your ~/.bashrc
export PATH=$PATH:~/.tools          # Replace with your directory
```
3. Run `ff --help` to get started!

