# Find and Replace

To perform a find-and-replace operation on a file using Vex, follow this syntax:

```shell
vex replace "foo:bar=input.txt"
```

**Explanation:**

- `foo`: The text you want to find.
- `bar`: The text you want to replace it with.
- `input.txt`: The file where the operation will be performed.

This command follows the general format:

```shell
[find:replace=<textinput>]
```

## Case Sensitivity

By default, the `replace` command is case sensitive. To make it case insensitive, add the `-i` flag:

```shell
vex replace "foo:bar=input.txt" -i
```

- `-i`: Enables case-insensitive matching for the find-and-replace operation.