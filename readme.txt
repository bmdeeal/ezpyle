ezpyle -- a simple and friendly line editor written in Python
(C) 2021, 2022 B.M.Deeal

Distributed under the ISC license.
See isc-license.txt for details.
Alternatively, visit <https://opensource.org/licenses/ISC>.

ezpyle was written mainly under Python 3.7, and is known to work under
Python 3.6.
Other versions may work, but have not been tested significantly.

This file was partially edited in ezpyle itself.

---
ABOUT:

ezpyle was written as a "friendly" editor for use under somewhat
"unfriendly" conditions. Namely, as an easy editor for use on systems that
cannot use a fullscreen editor for one reason or another.
Contrast ed, ex, and edlin for similar, less-friendly examples.
ezpyle is verbose and tries to provide all the information needed to edit
a file through interactive use, even if you've never used it before.

ezpyle is not meant to be a primary text editor, especially not in 2022.
My main use-case for it was using a Windows CE device over serial. The
VT100 emulation of the built-in terminal program is terrible.
Editors like vi, let alone nano or mcedit, broke miserably, but I didn't 
want to have to muck about and struggle with ed.

In general, ezpyle was made for changing a few config settings here and
there, or doing some basic text editing on a more powerful system from some
odd-ball device. It was never designed to replace your regular console text
editor.

However, ezpyle is friendly, highly interactive, and dead simple above all
else. Maybe too simple, too friendly, and too highly interactive, but
ultimately, most other editors in this category swung too hard in the
opposite direction.

The impetus for writing this program came from back when I had a Blackberry
with a fairly low-quality SSH client on it, around eleven years ago.
I couldn't (reliably) use vi or nano on that thing, due to some odd issues
with the terminal emulation compounding with the spotty EDGE connection.
Many of the terminal updates would end up being dropped, and I'd have to
try and refresh the display constantly.

Now, all these years later, I sat down and spent an evening to write this.
Since that evening, I've made it more usable through off-and-on work, and
it's now a reasonably useful bit of software.

I hope that ideally, if you use ezpyle, it's for a fun project like using
an old "dumb" terminal with a modern system.
Even something like an old WinCE system can be "useful" like this.

---
USAGE:

Usage is fairly simple: input a command, provide input, repeat.
All commands work on the current line.
ezpyle is mainly driven by giving a command, inputting lines of data and 
answering yes/no questions.
Commands take no parameters, and ask for information interactively.
All prompts for input are indicated by the '>' character. 

An example session is as follows:

Welcome to ezpyle v2.0-beta 5.
(C) 2022 B.M.Deeal.
Type ? for help.
(1|.) Command? > i
Inserting at line 1:
 > Hi there! I'm Brenden, the developer of ezpyle.
(2|!) Command? > i
Inserting at line 2:
 > I hope you find this program useful in some waay.
(3|!) Command? > l
1: Hi there! I'm Brenden, the developer of ezpyle.
2: I hope you find this program useful in some waay.
(3|!) Command? > repl
Replacing in line:
2* I hope you find this program useful in some waay.
String to be replaced? (case-sensitive) > waay
String to replace with? > way
The resulting line is as follows:
2* I hope you find this program useful in some way.
Is this okay?
y/[n] > y
Replaced 'waay' with 'way'.
(3|!) Command? > l
1: Hi there! I'm Brenden, the developer of ezpyle.
2: I hope you find this program useful in some way.
(3|!) Command? > wf
Filename to save as? Leave blank to cancel.
 > example.txt
Saved 2 lines to disk.
(3|.) Command? > quit
Exiting.

---
COMMANDS:

The full list of commands is as follows:
	?, help - show help
	a, app, append - append line after current
	i, ins, insert - insert line before current
	p, [, prev, previous - go back a line
	n, ], next - go forward a line
	r, replace - replace a string in this line with another
	j, jmp, jump - jump to line
	dd, delete - delete current line
	wf, write, save - write file to disk
	lf, load, open - load file from disk
	l, ls, list - list lines
	sl, showline, ll - show the current line
	la, al, als, listall - list all lines in file
	sp, split - split a line at a given string
	jn, join, cat - join the current line iwth the next
	mv, move - move the current line to another
	qq, quit, exit - quit program
	
---

This isn't a super-serious project, but it's been fun to work on.
It's been fairly fun to use too, even if there's no reason to not just use
nano or vim or anything else under normal circumstances. 
Editing this file in ezpyle has been actually pretty comfortable.

I hope you find this program useful.
Take care, and happy editing!
--B.M.Deeal
