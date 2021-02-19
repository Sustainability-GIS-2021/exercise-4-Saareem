# Exercise 4 - Written assignment

In the "Economic inequalities, growth and green economy" and the "Spatial regression" lessons + tutorial 
this week, we went through different indicators that can be used to understand economic inequalities and how 
(spatial) regression models can be used e.g. to understand which factors influence pricing of Airbnb listings. 

For this exercise, we recommend that you first write your text into Google Docs (or some other text editor), and once you are ready, paste the text into this Markdown document located at **your personal copy of the exercise** (e.g. `exercise-1-htenkanen`). You can add your text here using the editing functionalities of GitHub: click the pencil icon on the top-right side of this document (it will start an editor), then modify this document, and commit (i.e. save) your changes (to be able to do that, you need to add a commit message like `Update docs`). 

**Note for those doing the exercise in pairs**:

Only the `code ninja` should be cloning the Exercise repository as she/he/they will the **lead** on this exercise. The `philosopher`, i.e. you who will be leading the work for this written assignment should ask the `code ninja` to provide you [collaboration access](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository) to their copy of the Exercise. See more information from the [course page](https://sustainability-gis.readthedocs.io/en/latest/course-info/pair-programming.html).  

## Indicators and spatial regression (10 points)

Write 1-2 pages of text in English where you explain:
 
 - What are the key characteristics of different indicators that aim to measure economic inequality in the world?
 - Why growth/progress indicators that focus purely on economic performance are problematic? 
 - Why is it important to take spatial effects into account when doing regression analysis? 
 - What two approaches did we use to consider spatial effects in the tutorial? How do they differ? 
 
 
Use the lesson materials and the recommended readings (optional) as a source of information for answering to these.

----------------

### My answer

Ending the poverty is one of the main sustainability goals of United Nations Development Programme (UNDP). The mission sounds very ambitious and respectable, but its progress is difficult to measure. First, there should be clear and widely accepted definition for poverty. People who are poor in Finland, are not necessarily poor in Mozambique. Should people’s poverty be measured individually, nationally or globally? 

Maybe the most common global indicator of poverty is to calculate the amount of people who live on less than 2 dollars a day. Although the amount has decreased in the past years, the indicator contains lot of contradictions. Two dollars is not as valuable everywhere in the world and everything can’t be measured in dollars. If you live in the city, you have to buy everything you need, but in the countryside, you can utilize nature and agriculture. Money doesn’t matter so much in circular or self-sufficiency economy.

In fact, poverty is only a second half of economic inequality. Measuring just only poor or rich people doesn’t tell much about differences within the region. Inequality is always a relative to something, like other people. 

For that problem, there are developed also relative measurements. Maybe the most well-known is Gini-index that aims to measure degree of inequality in distribution in a specific region.  If region has Gini-value 1, everyone earns same amount of money, and if Gini-value is close to zero, situation is the opposite.

Second option is Palma-ratio that tells the ratio of the richest 10 % of the populations share of gross national income (GNI) divided by the poorest 40 %’s share. This ratio describes inequality well, but it has built-in presumption that population is already divided to the poor and the rich, as the portion of the poor is four times bigger.

A quite similar, but maybe better indicator is called 20:20 ratio, where the portions are the same size. As you can see from the name, that indicator compares how much richer the top 20 % of populations are to the bottom of 20 % of a given population. That reduces the effect of outliers, but still contains some presumptions. For example, 60 % of people are ignored. 

Globally the most used measurement is Gross Domestic Product (GDP) that sums up all monetary values of productions of goods and services in a country during a certain period. GDP doesn’t indicate well-being or inequality of country because everything can increase the total value of GDP, no matter how goods are distributed. Also, even terrorism or deforestation increases GDP, if they incurs costs.

There are many common problems of all indicators. Measurements are usually limited on a specific and arbitrary geographical boundaries and can consider only a things that can be thought as a money. It is hard to describe complicated phenomena with single number, which is always generalization of calculable units in certain region.

Geography is an important aspect of any measurement. Like Tobler’s law declares, spatially neighbouring observation affect one another. Values tend to cluster and have spatial autocorrelation which is called spatial lag. It can violate many statistical analysis, like regression, because there shouldn’t be any kind of correlation in regression analysis. Luckily, there are ways to reduce this effect and get more reliable results. In this lessons tutorial, that process have been done in two different ways of regression analysis. 

First is called spatially lagged exogenous regressors, where it is supposed to spatially lag or set spatial weights to explanatory variables that may affect the response variable. Observation where explanatory variable is high, will most probably affect or reflect to its neighbours. The closer the remarkable variable is, the more it affects to its neighbourhood spatially. Weights can be set for example with K-nearest neighbour – method.

Second method sounds more intuitive and is called spatially lagged endogenous regressors. The main point of this method is to set spatial weight to response variable itself. For example, house price is usually higher if neighbouring houses are also expensive and in opposite way. 

The main difference between spatially lagged exogenous and endogenous regressors is the variable to which spatial weight are set for. Exogenous method set weights to explanatory variable and endogenous set weights for response variable itself. Both are based on geography and proximity of observations.

## Hints

- If you need help in Markdown formatting (e.g. how to add headings, bold, italics, links etc.), please take a look at this excellent [guide / cheatsheet](https://www.markdownguide.org/cheat-sheet/) 
