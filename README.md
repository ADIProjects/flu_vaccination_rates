# The Non Nocere Lobby
## Solving the problems of vaccination in a globalised society

In the course of this project, we represent a group of concerned lobbyists, who have created a data science model for the US 
Government. In the current climate of Coronavirus panic, along with the rising tide of anti-science denialism (a la the documentary 'Vaxxed'), more effort than ever is needed to ensure protection against disease. In our study, we began by identifying the states with the lowest flu vaccine uptake, before then identifying the factors most likely to impact it nationwide. The conclusion is focussed on those areas most actionable, and includes strategies for increasing immunisation of the popluation.

## Step One - Data Selection

Initially, we were provided with a dataset covering all of North America, with over 500 variables to choose from. We decided to, as mentioned above, target the flu vaccine. Flu, the common name for the respiratory virus Influenza, has been a feature of human disease since it was first recorded in the 4th Century BC. It has been responsible for high mortality rates since this time, the most severe of which was the Spanish Flu pandemic of 1918. Spreading worldwide in the wake of World War One, it infected some 500 million people, or 1/3 of the global popuation, and possessed a motality rate of around 15%. Although this strain was not the same as the modern flu virus, it shows the signifcant impact the disease can have. Many people appear to believe the flu is similar to the common cold, which it is decidedly not, being much more severe. As a result, we feel that a renewed effort to educate people to the risks of the diease is necessary at the current point in time. This is not also a purely social concern. Studies have shown that sick days from work cost the US economy 530 billion dollars in 2018 (https://www.globenewswire.com/news-release/2018/11/15/1652374/0/en/Poor-Health-Costs-US-Employers-530-Billion-and-1-4-Billion-Work-Days-of-Absence-and-Impaired-Performance-According-to-Integrated-Benefits-Institute.html)

Therefore, through our efforts, we seek to both lessen the impact of the diease on both people, and the economy at large. 

## Step Two - Data Cleaning

We chose the variables based on a correlation matrix to identify the most significant impacts on the uptake of the flu vaccine. This was in order to narrow our analysis to the most relevant areas, and reduce the overall computational load of our eventual model. The raw values were selected, as these represented an overall readout for each variable. We also sourced an alternative dataframe for religious populations in the US. This was to investigate the potential impact belief systems may have upon the acceptance of flu vaccines. Overall, we chose variables that would allow us to drive home a message based on where we feel the most impact could be made. We filled the NaN values in the dataset with the median for that state, as this would have the least impact on the overall mean of the group.

## Step Three - Modelling

We split the dataset into training and test sections, in order to train our model on the relevant data. We proceeded to then undertake four training models, in order to investigate which had the overall greatest R^2 value. This value would demonstrate to us which of the models produced the most secure link between the dependent and independent variables. The models chosen were polynomial regression, ridge, lasso and elastic. These models utilised polynomial, scaled values, as well as being cross validated. The model with the highest R^2 value ended up being the Ridge regression, but this left us with over a thousand variables. As this was too many, we opted to go with the Lasso model, the R^2 of which was not significantly lower than the Ridge. We then tested the testing data set on the Lasso model, to identify our co-efficients and render an overall R^2 of 0.29. We also included a visualiser to map the distribution of our test data and our train data, with the test data performing .01 better than the train. Finally, we mapped our co-efficients onto our original dataframe, too see the areas which are actionable regarding flu vaccines.

# Conclusions

We have successfully been able to identify, and infer from this, several factors which may lead to a reduced uptake in flu vaccines in North America. This will allow for further, specialised study, and a hopefully effective campaign against this potentially deadly virus. 
These conclusions are threefold:
  1) Access to education about the disease, and the vaccine, is essential. People respond much better when they are informed,      and can appreciate the dangers associated with an unchecked infection. This was inferred from the mammogram value, and        potentially the Catholic population rates
  2) Linked to this is the nature of targeting those individuals who are not cautious about these potential risk with the          above point. We have taken this from deaths through injury, which may suggest people who are not overtly risk averse. 
  3) Finally, we have targeted ability to afford healthcare as a factor, which also links with point 1. Flu vaccines are not        cheap for those in the bottom of the economic data, and a program of free, or discounted vaccines may go a long way to        ameliorating this.
  
 ## Further Research
 
 Although we have some interesting findings, we are not statistically confident in them to a great extent, which may mostly be due to a lack of specialised data available. Further reserach focussed on access to unbiased, objective information about both the disease, the vaccine, and the makeup of the vaccine would assist in proving that the cure is not worse than the infection. On top of this, we suggest focussing efforts on poorer populations, who may not have the capacity to avoid lower-risk employment, which may create an overall higher risk mindset. The overall cultural and mental data, however, would be harder to quantify, but eminently achieveable with a dedicated surveying team. 
