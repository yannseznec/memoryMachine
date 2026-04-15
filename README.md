## memoryMachine aka All of Your Sounds (AoYS)

A system design for taking a very large library of sounds and creating an endlessly changing "soundscape" (for lack of a better phrase?). 

I use it with a library of 1100 sounds representing the audio tracks of every video in my cloud library. 

Currently designed to run either on a desktop computer or a Bela. I've been testing it mainly on a Bela Gem board. 

# To use: 
- download all the patches in this repo
- make a folder in the same directory called "sounds" or something
- put a lot of sound files in there. I'd recommend doing over 1000! Must be WAV or AIFF, and probably 44.1k though I am not certain of that
- open "_main.pd" in Pure Data
- the sounds should automatically be mixed and edited together endlessly

This system is working rather well on a Bela Gem now. Should work on older Belas now, but I'm not sure if the older Bela boards have the version of Pure Data with the [file] object, which enables the easier file loading. 

if you need these links:
Pure Data https://puredata.info
Bela https://bela.io

# selecting the sounds folder:
There's a subpatch in the main patch called "ys.soundloader". Use the "select folder" number to find the folder that actually has the sounds in it you want to use. 

# to-do:

- Currently it will always restart the random path from the beginning. Would be good to store the current state in a text file so that it restarts from where it left off
- new hardware enclosure/setup for the Bela version, PCB etc