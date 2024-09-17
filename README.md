# Katex note taking in VSCode

## VSCode Snippets

[Snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets) are a powerful tool which allow to quickly insert extensive code blocks inside VSCode.
This is perfect for math note taking with Katex in markdown files where creating objects can be unefficient without the right utilities.

**Example** : Paranthesis matrix of size 2,2 <br>
```latex
$$
\begin{pmatrix}
   a & b \\
   c & d
\end{pmatrix}
$$
```

<br>

You will find a `katex.code-snippets` file in this repository which contains some Katex functions. I plan to expand this list over time to support most of the supported functions described at https://katex.org/docs/supported.html.

You can of course complete the snippet file according to your needs by hand or with an LLM like ChatGPT when adding in bulk.

## Requirements and recommendations

For the snippets to be suggested in markdown files, you will need to edit your VSCode `settings.json` file by adding the following block :
```json
"[markdown]": {
    "editor.quickSuggestions": {
        "other": true,
        "comments": false,
        "strings": false,
    },
}
```

I also recommend adding the following settings for a better experience : 
```json
"editor.suggest.showWords": false,
"editor.suggest.showKeywords": false,
"editor.suggest.showSnippets": true
```

