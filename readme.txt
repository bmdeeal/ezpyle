ezpyle -- a simple and friendly line editor written in Python
(C) 2021 B.M.Deeal

Distributed under the ISC license.
See isc-license.txt for details.
Alternatively, visit <https://opensource.org/licenses/ISC>.

ezpyle was written under Python 3.7.
Other versions may work, but have not been tested.

This file was partially edited in ezpyle itself.

---
ABOUT:

ezpyle was written as a "friendly" editor for use under somewhat
"unfriendly" conditions.
Namely, an easy editor for use on systems that cannot use a fullscreen
editor.
Contrast ed, ex, edlin for similar, less-friendly examples.
ezpyle is verbose and tries to provide all the information needed to edit
a file through interactive use, even if you've never used it before.

ezpyle is not meant to be a primary text editor, especially not in 2022.
My main usecase was using a Windows CE device over serial.
The VT100 emulation of the built-in terminal program is terrible.
Editors like vi, let alone nano or mcedit, broke miserably.
In fact, I am currently typing this line from said device.

In general, this is for changing a few config settings here and there.
If you're using ezpyle, you're SSH-ing in from a potato.
Alternatively, things work enough for Python, but not vi for some reason.
If you need to do heavy text editing, you won't be using a line editor.
ezpyle is friendly, highly interactive, and dead simple above all else.
Often, too simple.

I probably should have written this 11 or so years ago. :P
I had a Blackberry at the time with a fairly poor SSH client on it.
I couldn't use vi or nano on that thing, as the terminal client I used
wasn't very good.
The spotty EDGE connection didn't help either, haha.

A simple editor like this would have been wonderful.
Now, ages later, I finally sat down and spent an evening to write this.
Since that evening, I've made it more usable through off-and-on work.
I hope if you use ezpyle, it's for a fun project, rather than because
things are totally broken, haha.
Something like being able to use a glass TTY or other ancient terminal.
Even something like an old WinCE system can be "useful" like this.

---
USAGE:

Usage is fairly simple: input a command, provide input, repeat.
All commands work on the current line.

The four main editing commands are
	* jumping to a line
	* deleting a line
	* inserting at a line
	* appending after a line

In general, editing is done by inserting and deleting whole lines.
Many operations also involve splitting and joining lines.
To edit an existing line, you would generally:
	1. jump to the line you want to fix (with 'j' or 'jump')
	2. retype the line with your edits (with 'i' or 'insert')
	3. delete the old line (with 'dd' or 'delete') 

---
COMMANDS:

The commands are:
	? - show help
	a - append line after current
	i - insert line before current
	j - jump to line
	dd - delete current line
	wf - write file to disk
	lf - load file from disk
	l - list lines
	sl - show the current line
	als - list all lines in file
	sp - split a line at a given string
	jn - join the current line iwth the next
	mv - move the current line to another
	qq - quit program
	
You don't need to memorize the commands.
Type ? at the ezpyle prompt for a full list of commands.
Each command has long-form aliases too, like 'save' or 'delete'.

---

This isn't a super-serious project, but it's been fun to work on.
It's been fairly fun to use too, even if there's no reason to not just use
nano or vim or anything else. Line editing is dead, but eh.
Editing this file in ezpyle has been actually pretty comfortable.

I hope you find this program useful.
Take care, and happy editing!
--B.M.Deeal
