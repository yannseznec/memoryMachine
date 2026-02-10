## memoryMachine aka All of Your Sounds (AoYS)

A system design for taking a very large library of sounds and creating an endlessly changing "soundscape" (for lack of a better phrase?). 

I use it with a library of 1100 sounds representing the audio tracks of every video in my cloud library. 

Currently designed to run either on a desktop computer or a Bela. I've been testing it mainly on a Bela Gem board. 

# To use: 
- download all the patches in this repo
- make a folder in the same directory called "sounds" or something (see buglist below!)
- put a lot of sound files in there. I'd recommend doing over 1000! Must be WAV or AIFF, and probably 44.1k though I am not certain of that
- open "_main.pd" in Pure Data
- the sounds should automatically be mixed and edited together endlessly


These patches run well on a Bela, more details about that soon

if you need these links:
Pure Data https://puredata.info
Bela https://bela.io

# current bug:
running the patch on macOS, you actually currently need to have *two* subfolders in the directory, and the sounds need to be in the *second* folder (alphabetically). This is apparently because of a difference in how folders are counted in macOS vs Linux (for the Bela). I don't know what the deal is on windows, should probably test that at some point but I'd like to just fix it more broadly. Future "fix" will probably be to just hardcode the name of the folder.

# to-do:
- Consider how the parameter change happens on the length of sound...currently the value only changes when a new sound is triggered, which results in potentially very long perceived latency when going from high value to low value. Maybe that's fine? Probably not. A better version would change the playback system so that it triggers the next sound once the elapsed playtime has reached a threshold, and the knob changes that threshold. That way if a sound has been playing for longer than the threshold it will move to the next sound, even if that threshold has changed. That should solve it without any adverse effects (famous last words), but requires a more in-depth change than I have had the time for just yet. 
- fix the folder bug described above
- Possibly revisit the random number assignment system a bit
- new hardware enclosure/setup for the Bela version, PCB etc
- Currently I think it will always restart the random path from the beginning. Would be good to store the current state in a text file so that it restarts from where it left off