## Home made Shell, that does the following:
* accepts standard commands from user that are in OS binaries (ls, wc etc.)
* Implements home made function of cmd 'cd' which changes directory, goes to HOME path if no path specified
* handles background and foreground processes (&)
* implements binaries (ls, wc etc.) by creating child processes that use exec function
* handles stdin and stdout redirection (< , >)
* expands var $$ into parent process ID
* has signal handler for SIGINT--(ctrl C), to not stop parent process
* exit handler-- entering exit will exit shell, shell cleans up zombies and all background processes
* has signal handler for SIGSTP (ctrl Z), that instead of stopping processes, enters 'foreground mode'
* foreground mode ignores background job command (&), user SIGSTP to exit this mode
* cmd 'status' will print last ran process exit status
  
