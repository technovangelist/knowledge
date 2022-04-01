**git**-aware cat with syntax highlighting

Source: https://github.com/sharkdp/bat

![image](https://camo.githubusercontent.com/7b7c397acc5b91b4c4cf7756015185fe3c5f700f70d256a212de51294a0cf673/68747470733a2f2f696d6775722e636f6d2f724773646e44652e706e67)

```
bat 0.15.4
A cat(1) clone with syntax highlighting and Git integration.

USAGE:
    bat [OPTIONS] [FILE]...
    bat <SUBCOMMAND>

OPTIONS:
    -A, --show-all                       Show non-printable characters (space, tab, newline, ..).
    -p, --plain                          Show plain style (alias for '--style=plain').
    -l, --language <language>            Set the language for syntax highlighting.
    -H, --highlight-line <N:M>...        Highlight lines N through M.
        --file-name <name>...            Specify the name to display for a file.
    -d, --diff                           Only show lines that have been added/removed/modified.
        --tabs <T>                       Set the tab width to T spaces.
        --wrap <mode>                    Specify the text-wrapping mode (*auto*, never, character).
    -n, --number                         Show line numbers (alias for '--style=numbers').
        --color <when>                   When to use colors (*auto*, never, always).
        --italic-text <when>             Use italics in output (always, *never*)
        --decorations <when>             When to show the decorations (*auto*, never, always).
        --paging <when>                  Specify when to use the pager (*auto*, never, always).
    -m, --map-syntax <glob:syntax>...
            Use the specified syntax for files matching the glob pattern ('*.cpp:C++').

        --theme <theme>                  Set the color theme for syntax highlighting.
        --list-themes                    Display all supported highlighting themes.
        --style <components>
            Comma-separated list of style elements to display (*auto*, full, plain, changes, header,
            grid, numbers, snip).
    -r, --line-range <N:M>...            Only print the lines from N to M.
    -L, --list-languages                 Display all supported languages.
    -h, --help                           Print this help message.
    -V, --version                        Show version information.

ARGS:
    <FILE>...    File(s) to print / concatenate. Use '-' for standard input.

SUBCOMMANDS:
    cache    Modify the syntax-definition and theme cache
```
