# Find and Replace

## Single Find and Replace

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

## Batch Find and Replace

You can now perform multiple find-and-replace operations in a single command. The syntax for batch operations is as follows:

```shell
vex replace "foo1,foo2,foo3:bar1,bar2,bar3=input.txt"
```

Explanation:

- `foo1, foo2, foo3`: The words you want to find.
- `bar1, bar2, bar3`: The corresponding words to replace them with.
- `input.txt`: The file where the batch operation will be performed.

**Example:**

Input command:

```shell
vex replace "foo1,foo2,foo3:bar1,bar2,bar3=input.txt"
```

Operation:

- foo1 → bar1
- foo2 → bar2
- foo3 → bar3

## Case Sensitivity

The replace command is case-sensitive by default. To enable case-insensitive find-and-replace, use the `-i` flag:

```shell
vex replace "foo:bar=input.txt" -i
```

Key Points:

- `-i` allows matching text regardless of case (e.g., foo, Foo, and FOO are treated as the same).
  
**Batch Example (Case Insensitive):**

```shell
vex replace "foo1,FOO2,foo3:bar1,bar2,bar3=input.txt" -i
```

Matches:

- `foo1, FOO2, foo3` → `bar1, bar2, bar3`