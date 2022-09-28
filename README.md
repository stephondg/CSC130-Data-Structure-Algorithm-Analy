# CSC130-Data-Structure-Algorithm-Analy
# Project 1 Sound Blaster
General Strategy
The general strategy for using sox is as follows.
1. Take a .wav sound file of your choosing (e.g. secret.wav). This
sound shouldn't be longer than a few seconds, or your program will
run out of memory.
2. Convert it to a .dat file: sox secret.wav secret.dat
3. Manipulate it with the program you will write: java Reverse
list double secret.dat secret-revealed.dat

Convert it back to a .wav file: sox secret-revealed.dat secret-
revealed.wav

4. Listen to it with your favorite sound player.

Project Assignment 
You need to provide two stack implementations, one using an array
and one using a linked list. They should be called ArrayStack and
ListStack, respectively. They should implement the DStack interface
given to you. Once you provide these implementations, Reverse

should work and create backwards sound files. It should take no
more than a page or two of code to provide the implementations.
Notes:
Your array implementation should start with an array of size 10
elements and resize to use an array twice as large whenever the
array becomes full, copying over the elements in the smaller array.
When growing your array, do your copying "by hand" with a loop, do
not use Arrays.copyOf or other similar methods. It is good to know
that these methods exist, but for now we want to focus on
understanding everything that is going on "under the covers" as
we talk about efficiency. If you write the copy method yourself
- then you really can see this. (You can either write a separate
private helper method, or just put the code in directly.) Using
the length property of an array is perfectly fine to do.
For your linked list implementation, you should implement your own
linked list nodes and build a stack out of those, similar to the
slides from lecture 1 that do the same thing for a queue. You
should NOT be using any classes from Java collections. You may
include your node class as a separate file (Don't forget to submit
this file!) or as a nested/inner class. Either will be fine.
Both ArrayStack and ListStack should throw an
EmptyStackException if pop() or peek() is called when the stack
is empty. To use EmptyStackException, add the following line to
your file:
import java.util.EmptyStackException;
Note that your solution does not require making changes to
Reverse.java.
