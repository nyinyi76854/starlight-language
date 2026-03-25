This guide explains how to install and set up the Starlight CLI.

---

# Requirements

Before installing, make sure you have:

- Node.js (version 16 or higher recommended)
- npm (comes with Node.js)

Check versions:

```

node -v
npm -v

```id="c1x7lm"

---

# Install Starlight CLI

Install globally using npm:

```

npm install -g starlight-cli

```id="q9n3vb"

This command installs Starlight CLI globally so you can run `starlight` from anywhere.

---

# Verify Installation

After installing, run:

```

starlight -v

```id="t5y8hk"

You should see the CLI version printed in the terminal.

---

# Basic Usage

Run a Starlight file:

```

starlight app.sl

```id="z6r2dp"

---

# Create Your First File

Create a file named `hello.sl`:

```

define name = "World"
sldeploy("Hello " + name)

```id="p4w8nx"

Run it:

```

starlight hello.sl

```id="h7m1qa"

---

# Interactive Mode

Start the interactive editor:

```

starlight --writedirectly

```id="n3c8ut"

Type code line by line, then run:

```

:run

```id="x8d2sa"

---

# Open Learning Guide

```

starlight --learn

```id="v2p9kd"

This opens the official learning guide in your browser.

---

# Updating

Update to the latest version:

```

npm update -g starlight-cli

```id="j5u4rw"

---

# Uninstall

Remove globally:

```

npm uninstall -g starlight-cli

```id="m1s7qe"

---

# Troubleshooting

## Command Not Found

If `starlight` is not recognized:

- Make sure npm global bin is in your PATH
- Restart your terminal

Check npm global path:

```

npm config get prefix

```id="f3b6zn"

---

## Permission Errors (Linux / macOS)

Try:

```

sudo npm install -g starlight-cli

```id="r9k2vp"

---

# Notes

- `.sl` files are executable via the CLI
- `.md` files open in a rendered HTML viewer
- The CLI works cross-platform (Windows, macOS, Linux)


# End of Installation Guide
```
