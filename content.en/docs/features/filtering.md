# Filtering

To filter a word in your file, you can run the following command:

```shell
vex filter "Hello=world.js"
```

This command is equivalent to the format:

```shell
[word=<textinput>]
```

Example Output:

```shell
Pattern: "Hello"
File: world.js
Total Matches: 3

Match 1: Line 5: console.log("Hello")
Match 2: Line 6: console.log("Hello")
Match 3: Line 7: console.log("Hello")
```