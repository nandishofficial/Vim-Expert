# Vim-Expert
Notes for VimTutor that will help make you Vim Expert ;)


Note: You can best leverage this guide alongside opening the "vimtutor" :)
![image](https://github.com/nandishofficial/Vim-Expert/assets/70503042/ae457645-5998-449f-83de-b9c173dce074)


1.1

Okay so J looks like a down arrow

L is at rightmost, so goes right

Rest you can figure it out, as the total keys are "hjkl"
![image](https://github.com/nandishofficial/Vim-Expert/assets/70503042/1b920208-67e6-4865-9331-8a5ad1a6175c)


1.2

Know the difference between :q!<ENTER> and :wq
![image](https://github.com/nandishofficial/Vim-Expert/assets/70503042/43f633c0-a4ca-41c2-8387-328a5190fb3d)


1.3 Text Editing - Deletion, Insertion

Deletion - move the cursor straight on top of the character which is to be removed
Insertion - move the cursor on top of the character BEFORE which the text is to be inserted

Eg - swiggy
![image](https://github.com/nandishofficial/Vim-Expert/assets/70503042/9628517f-9001-4450-b183-f3ba84a6579c)


2.1 deletion words

Dw - delete word
Important - Only if cursor is at the beginning of the word that needs to be deleted.

2.2 More deletion commands
d$ - delete the end of the line, so place the cursor at the end of the line and the rest of the line will be deleted.

2.3 On operators and motions
w - until start of next word
e - end of current word, including the last character
$ - end of the line

2.4 Using a count for a motion
0 - move to the end of the line
n(w, e, $, 0, … {all known shortcuts}), where n is an integer
10 (n0) - move ten places from the current position

2.5 Using a count to delete more
Yeah same as 2.4 but about delete

2.6 Operating on Lines
dd - delete a whole line (from anywhere)
Ndd - ", where n > 1 is an integer

2.7 The Undo command

u, U, CTRL+R

3.1 The put command
Use p ABOVE where the deleted line should go.

3.2 The Replace command
Type rk to replace some x with k

3.3 The Change Operator (places you in the insert mode)
ce - change until the end of the word
cc -- change the whole line

Note - the difference between dd and cc is that in cc you get to change the whole line, so you enter into the insert mode after writing cc, and in dd it literally deletes that whole line. Note in cc it does not delete the blank line, but clears the whole line and allow you to write something on that line itself.

3.4 More changes using c
c acts as d (delete), but delete in an insert mode (c). It also follows the "operator [number] motion"

4.1 Cursor Location and File Status
CTRL+G, here G is lowecase, gives you filename and line number
G (upper-case, i.e., SHIFT+G) move you to the bottom of the file
gg move you to the start of the file

4.2 The Search Command
Type / for search and hit ENTER. Now, type n for next and type N for reverse next, i.e., in the opposite direction. To straight away search for the text in the backward/opposite direction, use ? Instead of /
Jump back - CTRL+O
Jump forward - CTRL+I

4.3 Matching Parentheses Search
Type % to find a matching ), ], or }

4.4 The Substitute Command
:s/old/new/g
s mean substitute
g mean globally
:#,#s/old/new/g - #,# is the range of lie numbers where the substitution is done
:%s/old/new/g - change every occurrence in the whole file
:%s/old/new/gc - whole file, but will prompt whether to substitute or not

5.1: How to execute an external command
:! Followed by an external command to execute that command

5.2: More on Writing Files
Acts as "save as"
type :w FILENAME
w - write/save as

5.3: Selecting Text to Write
Type v and move the cursor to select the text. Save by :'<,'>w FILENAME

5.4: Retrieving and Merging Files
:r FILENAME, retrieves FILENAME and puts it below the cursor position
r- retrieve

:r !ls - retrieves ls command and place it below the cursor


6.1: The Open Command
Type o to open a line below the cursor and O for above the cursor.
Typing o or O will take you in an insert mode.

6.2: The Append Command
a - append
a - inserts text AFTER the cursor ; A - inserts text at the END of line
e - pressing continuously will jump continuously to the END of the words, so the cursor is on the last letter of the word where jump happened

6.3: Another Way to Replace
Replace the text with CTRL+R. Note R is uppercase.

6.4: Copy and Paste Text
Select with v, copy with y (yank), paste with p.
Move to end of the line by $

6.5: Set Option
:set ic where ic mean ignore case. Inverse is :set noic
:set hls is where hls mean highlightsearch and is mean incremental search (real-time search). Inverses are :nohlsearch for hls and for is it is :set noincsearch

For inverses, you could also add no in front of the name, like :set noic, :set nohls, :set nois

NOTE: If you want to ignore case just for a single search command, use \c while searching. For example
/anywordtosearch\c


7.1: Getting Help
Type Ctrl+W Ctrl+W (2 times) to jump from one window to another

![image](https://github.com/nandishofficial/Vim-Expert/assets/70503042/a4f12f4c-d403-4e93-8439-afcce68ae9ac)



