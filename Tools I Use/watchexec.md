automatically run a command when a file is changed
source: https://github.com/watchexec/watchexec

```
watchexec 1.14.1
Execute commands when watched files change

USAGE:
    watchexec [FLAGS] [OPTIONS] <command>...

FLAGS:
    -c, --clear                Clear screen before executing command
    -h, --help                 Prints help information
    -k, --kill                 Send SIGKILL to child processes (deprecated, use -s SIGKILL instead)
        --no-default-ignore    Skip auto-ignoring of commonly ignored globs
        --no-environment       Do not set WATCHEXEC_*_PATH environment variables for child process
        --no-ignore            Skip auto-loading of ignore files (.gitignore, .ignore, etc.) for filtering
        --no-meta              Ignore metadata changes
    -n, --no-shell             Do not wrap command in 'sh -c' resp. 'cmd.exe /C'
        --no-vcs-ignore        Skip auto-loading of .gitignore files for filtering
    -p, --postpone             Wait until first change to execute command
    -r, --restart              Restart the process if it's still running
    -V, --version              Prints version information
    -v, --verbose              Print debugging messages to stderr
    -W, --watch-when-idle      Ignore events while the process is still running

OPTIONS:
    -d, --debounce <milliseconds>    Set the timeout between detected change and command execution, defaults to 500ms
    -e, --exts <extensions>          Comma-separated list of file extensions to watch (js,css,html)
    -f, --filter <pattern>...        Ignore all modifications except those matching the pattern
    -i, --ignore <pattern>...        Ignore modifications to paths matching the pattern
    -w, --watch <path>...            Watch a specific file or directory
        --force-poll <interval>      Force polling mode (interval in milliseconds)
    -s, --signal <signal>            Send signal to process upon changes, e.g. SIGHUP

ARGS:
    <command>...    Command to execute
```

**CLI Tools** 