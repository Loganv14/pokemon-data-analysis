# Pokemon Data Exploration
## by Logan Vega


## Dataset

The data consists of information regarding all 807 Pokemon from the first 7 generations, including Pokemon type, battle statistics,
evolution information, and if a Pokemon is a rare and special "legendary" or "mythical" Pokemon. The data was gathered from 
[here](https://github.com/veekun/pokedex/tree/master/pokedex/data/csv). Light wrangling was needed to obtain the features I 
wanted to investigate, and was done through inner merges of the dataframes on Pokemon id numbers. I then saved a csv of the wrangled 
data as pokemon_data.csv, which is included as a file.


## Summary of Findings

Water is the most common Pokemon type and Ice the least common type. When looking at only single type pokemon, normal is the most 
common and flying the least common. Among dual types, flying is by far the most common and electric the least common. No 
transformations were needed. Also, water is by far the most common pokemon type overall, and has about equal distribution between 
single- and dual-type Pokemon.

The flying type is the most common among dual types but among single types there was only 1 flying-type pokemon. Overall, it is the 3rd 
most common type. This suggests flying is a type that is almost exclusively paired with another type, but is quite common when doing so.
The flying type is most often paired with the normal or bug type. Also, the distribution of total battle stats was bimodal but had a 
small group of pokemon that had stats high above the rest. No adjustments were needed to the data as it was not a result of data error 
and are facts important to the analysis.

Total stats and capture rate have a fairly strong negative correlation. Dragon and steel Pokemon types had slightly higher total stats 
than other types of Pokemon. Total stats are higher to legendary and mythical Pokemon, while capture rate was lower for these Pokemon. 
Total stats are typically higher among Pokemon that evolved from a different species, except in the cases of legendary and mythical 
Pokemon, which do not evolve but have higher total stats than other Pokemon. Most generation introduced a similar spread of Pokemon 
with different total stat amounts, but generation 7 (the newest in this dataset) had a higher proportion of stronger Pokemon than the 
previous generations.

There appeared to be fairly weak positive correlations between attack and special attack and between defense and special defense. 
This suggests that a Pokemon is usually stronger or weaker in both types of attack or both types of defense rather than just a single 
type.

The poison, electric, and ice types had the strongest negative correlation between total stats and catch rate, while the dragon type 
had the weakest correlation. Also, the normal Pokemon type had nearly the lowest total stats on average for Pokemon that are not 
legendary or mythical, yet had nearly the highest total stats for Pokemon that are legendary or mythical. This suggests that the 
strength of normal Pokemon of a certain type is not a predictor of the strength of that type's legendary/mythical Pokemon.

Generation 1 Pokemon having the largest total stat gap between nonevolved and evolved Pokemon and generation 7 having the smallest gap 
was interesting. This suggests that for generation 1, picking Pokemon that evolve to use in your team is likely more important for 
battle strength than it is in generation 7. 


## Key Insights for Presentation

For the presentation, I focus on Pokemon types and total stats. I added background information that describes the features that are 
being investigated. I first show Pokemon type and total stats distributions in a countplot and histogram, respecitively. I added 
titles and axis labels to these plots. I then examine total stats and capture rate by Pokemon type through a PairGrid of Box Plots, 
adding axis labels and a title for clarity.

I then discuss total stats by Pokemon type and legendary/mythical status via a triple bar graph. I added better axis labels and a 
title to this plot as well. Finally, I discuss total stats versus generation and evolution and show a double bar graph. This plot 
was already cleaned up in the exploration. 