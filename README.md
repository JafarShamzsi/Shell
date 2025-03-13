# Shell Implementation in Python

This project is a simple shell implementation in Python. It supports basic shell commands, command completion, and output/error redirection.

## Features

- **Builtin Commands**: Supports `echo`, `exit`, `type`, `pwd`, and `cd`.
- **Command Completion**: Provides tab completion for built-in commands and executables in the system's PATH.
- **Output Redirection**: Supports `>`, `>>`, `2>`, and `2>>` for redirecting stdout and stderr.
- **Error Handling**: Handles errors gracefully and provides appropriate error messages.

## Usage

1. **Running the Shell**:
   ```sh
   python main.py
   ```

2. **Builtin Commands**:
   - `echo [args]`: Prints the arguments to stdout.
   - `exit [code]`: Exits the shell with the specified exit code (default is 0).
   - `type [command]`: Displays whether the command is a builtin or an executable in PATH.
   - `pwd`: Prints the current working directory.
   - `cd [directory]`: Changes the current directory to the specified directory.

3. **Command Completion**:
   - Press `Tab` to complete commands and executables.
   - If multiple matches are found, pressing `Tab` again will display all matches.

4. **Output Redirection**:
   - `command > file`: Redirects stdout to the file (overwrites).
   - `command >> file`: Redirects stdout to the file (appends).
   - `command 2> file`: Redirects stderr to the file (overwrites).
   - `command 2>> file`: Redirects stderr to the file (appends).

## Example

```sh
$ echo Hello, World!
Hello, World!

$ pwd
/path/to/current/directory

$ cd /path/to/another/directory

$ type echo
echo is a shell builtin

$ ls > output.txt

$ ls non_existent_file 2> error.txt
```

## Dependencies

- Python 3.x
- `readline` module (for command completion)
- `shlex` module (for parsing commands)
- `subprocess` module (for executing external commands)
- `os` module (for file and directory operations)
- `re` module (for regular expressions)

## License

This project is licensed under the MIT License.
