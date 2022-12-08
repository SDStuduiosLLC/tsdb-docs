---
description: How to build your TSAB instance.
---

# 🏗 Building Your Instance

So, now you have your instance configured, it needs to be built and tested before fully deploying it. It probably won't work first time if your anything like us...

To build the bot, simply run:

```bash
npm run build
```

After this, to make sure your build worked, run either:

```bash
node build/src/theHeart.js
```

or

```bash
npm run start-prod
```

If all is working properly, you should get a whole bunch of stuff being spewed out, basically, the rule is - if its _not_ spitting errors out, but there is lots of text, it's probably working. Make sure you have the bot added to your server, and check that it has actually come online. From the last time we changed it, the bot status should be _"Watching the suffering of humanity"_ if I were you, might be worth changing that if you want to have a good impression on your communities members.\
\
(I mean, you don't _need_ to. It's not, like, required.)
