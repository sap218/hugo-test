---
title: "Colours"
date: 2019-12-11
toc: true
categories: ['python','command line','nlp','sentiment']
---

# Rainbow project

All fun little `Python` projects via command line interface.


## `indigo`

Simple to-do list: indi-go-ing

`indigo` is a to-do list tracker ([GitHub repo](https://github.com/sap218/indigo "indigo git repository")).
During my PhD, I often had impromptu meetings which needed my laptop and I found myself unable to multi-task: reading results, listening to others, and trying to write down notes. 
I usually ended up rushing my notes, which then became unreadable. And so I made `indigo` to make my note-taking easier: I can `Alt+Tab` to switch between the window of results to the window of notes.

You can add tasks, complete tasks, and room for future features! I also then proceed to transfer notes to a more secure location after the meeting.

```
$ indigo

>> help
View list:	'view'
Add tasks:	'add'
Done task:	'done'
Need help:	'help'
Shut down:	'n'
```

**Current issues:**
+ if user doesn't use `n` correctly when closing the program, task list may disappear (`Python` returns a `keyboard interruption error`)...But `indigo` encourages users to exit and save by typing `n`.


## `cyannotator`

Simple highlighting annotator - in cyan.

`cyannotator` is a highlighting tool for a corpus ([GitHub repo](https://github.com/sap218/cyannotator "cyan annotator git repository")).
My PhD included NLP tasks to show frequency of terms in a corpus, and I was looking for a way to visualise this.
Futhermore, sometimes in a meeting it was asked if a particular term was present and I needed a quick easy way to show this.

I developed `cyannotator` for quick observation of plain text files (and a plain text file of `\n` separated list of key terms).

```
$ cyan --help

Usage: cyan.py [OPTIONS]

Options:
  --file TEXT   Text file.
  --lists TEXT  List of words.
  --help        Show this message and exit.
```

`$ cyan -file yourtextinput.txt -lists yourconcepts.txt`


## `mAIze`

Simple chatbot: a-mAIze-ng!

`mAIze` is a sentiment score "chatbot" ([GitHub repo](https://github.com/sap218/mAIze "maize git repository")). Essentially it'll ask how you are and remembers your previous disucssion.
During my PhD, I discovered the amazing world of sentiment analysis and although my PhD progressed onto the next chapter, I wanted to play around a little more with this.

```
$ maize
```

**Current issues:**
+ currently only remembers emotion score from last visit and not what was said.
