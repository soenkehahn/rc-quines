# Recurse Center Quine Game

This is a github-based game for people at the [Recurse
Center](https://github.com/soenkehahn/rc-quines).


# What are quines?

Quines are programs that -- if you run them -- output a string that is equal to
their source code. It's a fun puzzle to figure out how to write a quine, so
we won't give any hints in this README. Also, beware of spoilers when browsing
this repo, which will contain lots of quines, or when googling quines.

# The game

If you want to play this game, just submit a PR to this repo that contains a
quine, in a language of your choice.
[CI](https://circleci.com/gh/soenkehahn/rc-quines) will check whether the
program you've submitted is actually a quine. If CI passes, you have won the
game. (Yay!)

Also, you can ping us in a github comment
[@soenkehahn](https://github.com/soenkehahn) and we will merge the PR. This way,
we hope that this repo will become a fun collection of interesting and creative
quines.

# How to submit a PR?

Fork this repo. Then create a PR that adds a new directory to this repo that
contains one file called `quine`. That file has to be executable
(`chmod +x ./quine`) and it'll be
executed without specifying an interpreter, so it should probably include
a shebang. A shebang is a line at the beginning of your script that tells your shell
which interpreter to run. For example, to submit a python quine, add a shebang at
the beginning like so:

```
#!/usr/bin/env python
```

[More information about shebangs here.](https://en.wikipedia.org/wiki/Shebang_(Unix))

[Here](https://github.com/soenkehahn/rc-quines/pull/1)'s an
example of such a PR (that is not a quine, to avoid spoilers.)

After submitting
a PR, you can monitor CI to see the `quine-checker` checking your PR. Here's a link:
https://circleci.com/gh/soenkehahn/rc-quines

# The quine-checker

The quine-checker is implemented
[here](https://github.com/soenkehahn/quine-checker). You can install it to check
your quines locally.

# Cheating encouraged

People sometimes argue about what is a valid quine and what is not. For example,
reading from the file system is sometimes considered to be cheating.

We disagree and think it's a lot of fun to figure out how to cheat in creative ways.
If you can fool the automated `quine-checker` on CI, we'll consider your program a quine
and merge the PR. So, feel free to cheat.

We *won't* merge PRs that do 'extreme cheating' such as messing with other people's quines
or with the `quine-checker`, because that would break the game for others. However, we still
look forward to receiving PRs like that.

# Supported languages

Currently the only supported languages are:

- bash
- python
- javascript (through `node`)
- haskell (through ghc's `runhaskell`)

We will add more languages quickly depending on interest. If your favourite
language is not yet supported, feel free still to create a PR. We will try
to add support for that language. Alternatively, we very much welcome PRs for
the [`quine-checker` itself](https://github.com/soenkehahn/quine-checker)
adding support for more languages.
