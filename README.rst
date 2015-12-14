===================
IS360 Final Project
===================

Maurice Cox - Modesto Cabrera
=============================


How nutritious are our Fast Food Restaurants?
---------------------------------------------

The goal of this project is to present you with the healthier choices between famous (well known) fast food restaurant meals. We will explore the common meals in proportions that are made available by these particular restaurants. In our exploration and analysis, we predict that we will not find many favorable conditions in our analysis. This is partly due to varying health conditions in individuals, all the conclusions in the process should be taken with a grain of salt in this regard. Fast food is not a healthy choice. But what we will hope to have determined by the end of the analysis is the difference between the foods that can cause more 
detrimental effects on an individual’s health, than others, which may be less harmful and therefore safer 
to consume.


Process 1:
----------

Querying Site: (Collective Fast Food Restaurants and Nutritions for meals served)

During this process we have acquired some data from the following link:

Link: http://www.acaloriecounter.com/fast-food.php

The above link consists of a site, which has majority of Fast Food restaurants. This site contains 
10 tables which we will use in various forms, each particular and joined in a series of analysis.


Process 2:
----------

Parsing Table:

While parsing through the tables a few issues came to light, such as the Onion Rings table which would contain a missing column, we’ve handled the issue using some coding in a python for loop. We’ve resulted to returning the text in the tables, and further returning the text into another for loop. In order to process the DataFrames for each table in an automated manner. This resulted in a special function jus to parse the onion rings table. This process resulted in more use of memory, but given that we’ve only have one onion ring table, refactoring the code at that point seemed a bit too much for the results that were desired. 

After this issue was handled, we've also created an automated format to do the following extra columns for each
table in the DataFrame:

With a few calcualtions, we've managed to attain some more information from the pre-existing tables, which will
aid in analysis.

We've also proceded to create a sql database using pythons sqlite3, using sql.write_frame, it provides a light
use of code, and creates a relational database.

Conclusion:
===========


Figuring which food fits our macro beakdown

25% Protien, 35% Fat, 50% Carbs
-------------------------------

The resulting food are healthy and can be eaten on the go. Depending on your health, you might want to check the sodium levels.
