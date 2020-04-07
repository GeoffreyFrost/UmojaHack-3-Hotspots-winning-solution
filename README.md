# UmojaHack-3-Hotspots-winning-solution
The winning solution for the Zindi UmojaHack#3 hotspots 2020 hackathon

[Link: UmojaHack #3: Hotspots](https://zindi.africa/hackathons/umojahack-3-hotspots)

## Competition Context
_"Each year, thousands of fires blaze across the African continent. Some are natural occurrences, part of a ‘fire cycle’ that can actually benefit some dryland ecosystems. Many are started intentionally, used to clear land or to prepare fields for planting. And some are wildfires, which can rage over large areas and cause huge amounts of damage. Whatever the cause, fires pour vast amounts of CO2 into the atmosphere, along with smoke that degrades air quality for those living downwind._

_Figuring out the dynamics that influence where and when these fires will occur can help us to better understand their effects. And predicting how these dynamics will play out in the future, under different climatic conditions, could prove extremely useful. For this challenge, the goal is to do exactly that. We’ve aggregated data on burned areas across the whole of the DRC for each month since 1 April 2000. You’ll be given the burn area data up to the end of 2013, along with some additional information (such as rainfall, temperature, population density etc) that extends into the test period. The challenge is to build a model capable of predicting the burned area in different locations over the 2014 to 2016 test period based on only this information."_

## Solution
Quite some time was spent researching all the variables so that I could better understand what I was working with. This involved a lot of wikipedia as the provided variable descriptions were not enough to grasp the effect of each feature. 

I used fast.ai’s tabular learner, which is a feed forward neural network. I didn’t use any fancy model selection tools, I just picked it because it’s really easy to work with and I’ve used it in the past. Before doing any feature engineering, I wanted to get a baseline. I trained on just the provided data, which resulted in a root mean squared loss (rmsl) of about 0.03136 which was already pretty good for the early stages of the competition.

I beagain adding features one by one, evaluating my model each time. This allowed me to add a few really good features, and not add any features that would hurt the model. After I was happy with the features I was adding, I tuned my hyper parameters,  and managed to get a rmsl of 0.02505 after ensembling.


## Remarks
I am by no means an expert in data science and I am sure there are things that I could have improved upon so please feel free to share any suggestions! Lastly, I had a blast competing in this hackathon, thanks to everyone involved!
