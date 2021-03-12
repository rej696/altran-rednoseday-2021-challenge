# altran-rednoseday-2021-challenge

One weekend deep in lockdown, your project manager has asked you to go into the office as a matter of urgency! (Those ATC2 system tests aren't going to run themselves after all) However, after almost a year of not going into the office, you have completely lost your pass! With no Kevin to let you in, you scan around for alternate methods of entry.

You sneak up the stairwell behind Cosy Club and make your way to the back door. However, the door is locked with a keypad expecting a passcode! In an effort to improve security, the code is changed every 10 minutes, and Claire has left a message on the wall with cryptic instructions for figuring out the code. (The idea being that it will take too long to figure out the code before it changes.)

The document goes on to explain that each button to be pressed can be found by starting on the previous button and moving to adjacent buttons on the keypad: U moves up, D moves down, L moves left, and R moves right. Each line of instructions corresponds to one button, starting at the previous button (or, for the first line, the "5" button); press whatever button you're on at the end of each line. If a move doesn't lead to a button, ignore it.

You are running out of time to complete your tests, so as the excellent software engineer that you are, you decide to figure out the code programmatically.

You picture a keypad like this:

1 2 3
4 5 6
7 8 9

Suppose your instructions are:

URR
DDLUUD
LLDLUU
RDLUR

- You start at "5" and move up (to "2"), right (to "3"), and right (you can't so stay on "3"), so the first button is 3.
- Starting from the previous button ("3"), you move down twice (to "9") and then left once (to "8"), followed by up twice (to "2") and down once, ending up at 5.
- Continuing from "5", you move left once (ignoring the second left), down once, ignore the 3rd left and up once (ignoring the 2nd up) to end up at 1.
- From 1, you move right, down, left, up, and right finally ending up at 2

So for this example, the code for the door is 3512

Your puzzle input is displayed on a screen by the keypad. What is the code?!
