# Shell Variables & Scripting Notes

## Key Takeaways
- **Variable Assignment**: `VARIABLE_NAME=value` (no spaces around the `=` sign).
- **Referencing**: Use `$VARIABLE_NAME` or `${VARIABLE_NAME}` to avoid ambiguity when appending text.
- **Quoting**:
  - Single quotes (`''`) preserve literal values (no variable expansion).
  - Double quotes (`""`) allow variable expansion while preserving spaces if quoted.
- **Command Substitution**: Wrap commands in `$()` or backticks `` ` `` to assign their output to a variable.
- **Arithmetic**: Use `$((expression))` for integer math, increments, and decrements.
- **Environment Variables**: Use `export VAR_NAME` to make variables available to child processes, and `unset` to remove them.
