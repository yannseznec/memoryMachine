## memoryMachine aka All of Your Sounds (AoYS)

A system design for taking a very large library of sounds and creating an endlessly changing "soundscape" (for lack of a better phrase?). 

I use it with a library of 1100 sounds representing the audio tracks of every video in my cloud library. 

Currently designed to run either on a desktop computer or a Bela. I've been testing it mainly on a Bela Gem board. 

To use: 
- download all the patches in this repo
- make a folder in the same directory called "sounds" or something
- put a lot of sound files in there. I'd recommend doing over 1000!
- open "_main.pd" in Pure Data
- the sounds should automatically be mixed and edited together endlessly

These patches run well on a Bela, more details about that soon

if you need these links:
Pure Data https://puredata.info
Bela https://bela.io

to-do:
- More stress testing of the system, make sure it doesn't crash or go silent after a long time
- I think I need to revisit the random number assignment system a bit
- new hardware enclosure/setup for the Bela version, PCB etc
- Make some parameter customization? For adjusting how the random parameters get triggered, to enable better exploration of different types of sound libraries etc. Do this initially in the software and then eventually maybe in hardware too, to have knobs for adjusting how you want your memories presented