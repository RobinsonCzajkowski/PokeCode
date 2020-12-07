
PokeBot v2.3

Creator: Robinson Czajkowski 2020
robbyczajkowski@gmail.com



How to use:

Run Main.py to start scanning. Exit code by Ctr-C or exiting the cmd line. Battle data will be saved under the folder recordedData.
Run Analysis.py to analyze data and make it into readable stats. Stats will be saved under Analysis directory.
Run clearData.py to clear all files under recordedData directory. The data cleared will be saved under the backup folder.


Errors:

If an error occurs it will beep and print out the error message. The scanning should still run hopefully.
Losing internet connection will cause an error.


Settings:

Change settings in config.ini file

loadTime -> wait time for startup of program. If program has errors starting up due to bad
internet, try increasing this value.

maxGames -> greatest number of games that will be analyzed at once

minimumElo -> only games with both players above this ranking will be scanned

demoMode -> Set this to true to unhide the browsers used to view battles. Use for showing 
off this program.

debugMode -> If true, will only analyze one game and not save it to file

analysisLength -> The analysis function will only view battles that were recorded this many
days ago. Having a smaller number will give a more accurate picture of the current metagame

giveMargin -> Option to disable margin of error to make it look more readable

problemPokemon, problemPlayers -> names that throws off the indentation of text files


Installation:

Might need to install pip.

Then run pip install selenium in cmd

If any of the .py files open and close intantly without running, navigate to the PokemonBot directory in cmd with the files and type
the file (for example Main.py) in the command line. The error should then be printed. If it says module not found, type 
pip install moduleName

Also, you may need to allow permission for the script to run


Notes on Analysis:

Win percentages calculated with confidence interval of 95%. In other words, the actual ratio of win percentages has a 95% chance
of falling within the range of percantages given. More data will decrease the range further.

The brought percentages are skewed slightly to be lower than 50% due to lack of information. More losing pokemon are recorded as
brought to the battle, so the avarage win percentage of known pokemon are probably more like 45%. So a pokemon with a win percentage
when brought of 50% is possibly more favorable to use than average.

Items are determined only by the Frisk ability. This gives a decent sample size and is mostly unbiased.

Abilities are recorded only when they activate in a battle. Thus, the data on abilities are extreemely biased. This data has little 
statistical significance. It can be interesting to see how many people use certain useless abilities such as pressure on Dusclops, but
thats about it. I would need access to the code of pokemon showdown to do a more significant analysis.












