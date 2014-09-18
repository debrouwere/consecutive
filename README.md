# Consecutive

You're writing a novel, a technical manual, a thesis, and it's organized like so:

    1-introduction.md
    2-literature.md
    3-research.md
    4-conclusion.md

But then you decide you need a "methods" chapter in between the literature and the 
research, and unlike a word processor, your filesystem doesn't automatically 
update your chapter numbers. So you delete a file here and want to squeeze in another 
chapter there, and it's terribly annoying to have to rename all of those files to keep 
them in order.

This little `consecutive` executable will rename all files you hand it so they have 
a consecutive numbering. And when you need room for a new chapter, pass on any gaps
`consecutive` should leave in the numbering, and gaps there will be.

## Usage

```shell
# after you've deleted a chapter, you can redo the entire numbering like this
ls *.md | consecutive

# the same thing works marvelously when you've reached chapter ten
# and need to pad all previous chapter numbers with a zero
ls *.md | consecutive

# to create a new chapter 3 and 4 and bump up all subsequent chapters
ls *.md | consecutive 3 4
```

## Installation

```shell
sudo wget https://raw.githubusercontent.com/stdbrouw/consecutive/master/consecutive -O /usr/local/bin/consecutive;
sudo chmod +x /usr/local/bin/consecutive;
```
