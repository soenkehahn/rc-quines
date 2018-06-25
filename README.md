# Recurse Center Quine Game

This is a github-based game for people at the [Recurse
Center](https://github.com/soenkehahn/rc-quines).


# What are quines?

Quines are programs that -- if you run them -- output a string that is equal to
their source code. It's a fun puzzle to figure out how to write a quine, so
I won't give any hints in this README. Also, beware of spoilers when browsing
this repo, which will contain lots of quines, or when googling quines.

# The game

If you want to play this game, just submit a PR to this repo that contains a
quine, in a language of your choice.
[CI](https://circleci.com/gh/soenkehahn/rc-quines) will check whether the
program you've submitted is actually a quine. If CI passes, you have won the
game. (Yay!)

Also, you can ping me in a github comment
[@soenkehahn](https://github.com/soenkehahn) and I will merge the PR. This way,
I hope that this repo will become a fun collection of interesting and creative
quines.

# How to submit a PR?

Create a PR that adds a new directory to this repo that contains one file called
`quine`. That file has to be executable (`chmod +x ./quine`) and it'll be
executed without specifying an interpreter, so it should probably contain a
[shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)).
[Here](https://github.com/soenkehahn/rc-quines/pull/1)'s an
example of such a PR (that is not a quine, to avoid spoilers.)

# The quine-checker

The quine-checker is implemented
[here](https://github.com/soenkehahn/quine-checker). You can install it to check
your quines locally.

# Cheating

When it comes to quines some people consider some techniques cheating. For
example reading from the file system. Personally we think it's a lot of fun to
figure out how to cheat in creative ways, so if you can fool the automated `quine-checker` on CI, we'll consider your program a quine and merge the PR.

(Unless you do something nefarious, like messing with other people's quines or
with the quine-checker.)

# Supported languages

Currently the only supported languages are:

- python
- javascript (through `node`)
- haskell (through ghc's `runhaskell`)

But it should be easy to add more languages, please ping us if you want another
language. (Or submit a PR [here](https://github.com/soenkehahn/quine-checker).)
