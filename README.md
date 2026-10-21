# C-Lite Language Support for VS Code

Syntax highlighting and basic editor support for **C-Lite**, a lightweight, C-like scripting language.

## Features

- Syntax highlighting for C-Lite keywords and operators
- Highlighting for strings, character literals, numbers, and boolean values
- Support for line comments (`//`) and block comments (`/* ... */`)
- Function name highlighting
- Automatic bracket and quote pairing
- Comment toggling support
- `.clite` file association

## Supported Syntax

The grammar currently recognizes constructs such as:

```c
int count = 10;
bool active = true;
string welcome = "Welcome to C-Lite!";

echo welcome endl;

if count >= 10 {
    echo "Count reached!" endl;
}

greet() {
    echo "Hello from C-Lite!" endl;
}
```

The example illustrates the language's syntax; actual runtime support depends on the C-Lite interpreter.

## Installation

### Run from source

1. Clone this repository.
2. Open the project folder in Visual Studio Code.
3. Press `F5` to launch the Extension Development Host.
4. Open a `.clite` file to test syntax highlighting.

### Install a packaged extension

If a `.vsix` package is available, install it through the VS Code command line:

```bash
code --install-extension clite-language-support-0.0.1.vsix
```

Alternatively, use **Extensions: Install from VSIX...** from the VS Code Command Palette.

## Project Structure

```text
clite-vscode/
├── package.json
├── language-configuration.json
├── syntaxes/
│   └── clite.tmLanguage.json
├── README.md
├── LICENSE
└── .gitignore
```

## Related Project

This extension provides editor support for the C-Lite scripting language. It is maintained separately from the language implementation.

**C-Lite interpreter:** [Add your interpreter repository URL here]

## Scope and Limitations

This project currently provides declarative syntax highlighting and basic editor configuration.

It does not currently provide:

- Autocomplete or IntelliSense
- Syntax or type checking
- Diagnostics from the interpreter
- Go-to-definition or symbol navigation
- Debugging integration

Some highlighting rules use lexical patterns rather than the interpreter's parser, so highlighting may not always reflect semantic context.

## Contributing

Contributions, bug reports, and suggestions are welcome. Please ensure that changes to the grammar remain consistent with the actual C-Lite syntax.

## License

See the [LICENSE](LICENSE) file for licensing terms.
