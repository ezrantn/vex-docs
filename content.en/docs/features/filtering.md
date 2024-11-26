# Filtering

Vex makes it easy to filter specific words in your files. Use the following command to search for a word:

```shell
vex filter "Hello=world.js"
```

## Command Format 

The general format for the `filter` command is:

```shell
[word=<textinput>]
```

## Example Output

Here's what you might see when running the command:

```shell
Pattern: "Hello"
File: world.js
Total Matches: 3

Match 1: Line 5: console.log("Hello")
Match 2: Line 6: console.log("Hello")
Match 3: Line 7: console.log("Hello")
```

This output shows the word you're searching for, the file name, and a detailed list of all matches, including their line numbers and content.