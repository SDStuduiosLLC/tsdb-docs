---
description: >-
  How to install the required dependencies and configure your instance before
  deployment.
---

# 📥 Installing TSAB

### Cloning & Installing

To get started, clone the main branch from GitHub.

```bash
git clone https://github.com/sd-studios-official/the-somewhat-awesome-bot.git
```

After the repository has been successfully cloned, first make sure you have the required **global** dependencies installed. The command for installing them is:&#x20;

```bash
npm install --global typescript ts-node @types/node nodemon
```

Once all of these have been successfully installed, just run the NPM install command and wait for it to complete installing packages.

### Checkpoint 1

Now, before continuing - it's best just to check that everything installed correctly. Before running, we need to compile everything back into JavaScript. Run the build command shown below:

```bash
npm run build
```

If all is correctly installed, you should get the following output in the console.

```
if (!key) throw new Error('"key" is missing or undefined');
                        ^
Error: "key" is missing or undefined
```

or

```
No server specified, exit to prevent further errors...
```

If you get this, it worked! Everything has successfully installed.
