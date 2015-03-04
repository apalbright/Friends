# tld-friends
Raw data, tex code, and R scripts for "The One With All The Quantifiable Friendships" (found at: http://thelittledataset.com/2015/01/20/the-one-with-all-the-quantifiable-friendships/)

#Tikz viz
In order to make the multi-colored tikz visualization from this post, run the "tikznetwork" latex code.

#R viz
In order to make the R visualization found in the visualization update, run the "Rnetwork" R script. 

#R Packages Needed
You'll need to install the network package to run this the R script.

#Data fun
If you'd just like to play around with the data yourself, download the csv file from the raw_data folder.
Quick explanatory stuff: 
There are columns for episode season, episode number (within the season), episode name, and dynamics (which is the same thing as a character grouping in a plotline). There are a few rows for each episode of the show since each episode has a few different plotlines.

The episode dynamics are just numbers. The six friends are defined as follows:
Chandler=1
Joey=2
Monica=3
Phoebe=4
Rachel=5
Ross=6

So, 236 is a plotline made up of Joey, Monica, and Ross while 56 is a Rachel-Ross plotline. Pretty easy to interpret!
