# Find and Replace

Vex makes finding and replacing text in files simple and efficient. Here's how you can use it:

## Single Find and Replace

To perform a single find-and-replace operation, use the following syntax:

```shell
vex replace "foo:bar=input.txt"
```

**Explanation:**

- `foo`: The text you want to find.
- `bar`: The text you want to replace it with.
- `input.txt`: The file where the operation will be performed.

## Command Format

```shell
[find:replace=<textinput>]
```

## Batch Find and Replace

Vex also supports multiple find-and-replace operations in a single command. Here's the syntax:

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

By default, the replace command is **case-sensitive**. To make it **case-insensitive**, use the `-i` flag:

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