#   Starlight Programming Language

Starlight is a lightweight **server-side scripting language** with its own CLI runtime.
It allows you to execute `.sl` script files directly from the command line.

---

##   Usage

Run a Starlight script using:

```bash
starlight file.sl
```

This command will:

1. Read the `.sl` source file
2. Tokenize it using the lexer
3. Parse it into an AST
4. Execute it using the evaluator

---

## 📦 Project Structure

```plaintext
starlight/
├── lexer.js        # Tokenizes source code into tokens
├── parser.js       # Converts tokens into an AST
├── evaluator.js    # Executes the AST
├── starlight.js    # CLI entry point
└── README.md
```

---

##   Core Components

### `lexer.js`

Breaks raw `.sl` source code into tokens.

* Recognizes keywords, operators, identifiers, literals
* Outputs a structured token stream

  **Source Code → Tokens**

---

### `parser.js`

Transforms tokens into an Abstract Syntax Tree (AST).

* Ensures correct syntax
* Builds hierarchical program structure

  **Tokens → AST**

---

### `evaluator.js`

Executes the AST.

* Interprets expressions and statements
* Handles runtime behavior

  **AST → Output**

---

### `starlight.js`

The main CLI runtime.

* Handles command-line input (`starlight file.sl`)
* Reads file content
* Connects lexer → parser → evaluator

---

##   Execution Pipeline

```plaintext
file.sl
   ↓
lexer.js
   ↓
parser.js
   ↓
evaluator.js
   ↓
Output
```

---

##  Server-Side Language

Starlight is designed to run **on the server / command line**, not in the browser.

It can be used for:

* Backend scripting
* Automation
* Learning how interpreters work

---

##  Running the CLI

If installed globally:

```bash
starlight program.sl
```

Or using Node.js directly:

```bash
node starlight.js program.sl
```

---

##  Example

```plaintext
hello.sl
```

Run:

```bash
starlight hello.sl
```

---

##  Project Goals

* Build a simple but functional scripting language
* Demonstrate interpreter architecture
* Provide a foundation for future language features

---

##  Future Improvements

* Variables and functions
* Control flow (if, loops)
* Error handling
* Standard library
* Package system

---

##  Concepts Covered

* Lexical analysis (tokenization)
* Parsing (AST generation)
* Interpretation (execution)
* CLI tool design

---

##  Contribution

Contributions and ideas are welcome.
Feel free to fork and extend the language.

---

##  License

Open-source for educational and experimental use.
