===================
IS360 Final Project
===================

Maurice Cox - Modesto Cabrera
=============================


.. image:: https://github.com/mauricecox/Final-Project/blob/master/static/fastfoods_logos.png?raw=true
   :height: 100px
   :width: 200 px
   :scale: 50 %
   :alt: alternate text
   :align: center

How nutritious are our Fast Food Restaurants?
---------------------------------------------

Super Size Me produced in 2004 gave us a bad impression about eating fast food. It made it seem as though if you eat fast food you would become fat. This is horribly wrong. What happened in that documentary, and is not stated, is that the host Morgan Spurlock would eat way more calories than what is required for his daily caloric need. The host who needed 2500 calories worth of food, would eat more than 5000 calories per day. 3500 calories = 1lb of fat, so eating 1500 calories extra per day is 10500 calories which work out to be 3lbs of fat gain per week!

On the other hand, a science teacher, John Cisna, a high school science teacher lost 60lbs eating fast food for breakfast, lunch and dinner, McDonalds (breakfast menu) in particular. He understood caloric need and ate less calories than his daily caloric requirement, which allowed him to lose weight.

The goal of this project is to present you with the healthier choices between famous (well known) fast food restaurant meals. We will explore the common meals in proportions that are made available by these particular restaurants. In our exploration and analysis, we predict that we will not find many favorable conditions in our analysis. This is partly due to varying health conditions in individuals, all the conclusions in the process should be taken with a grain of salt in this regard. Fast food is not a healthy choice. But what we will hope to have determined by the end of the analysis is the difference between the foods that can cause more negative effects on health than others.

What we are doing here is pretty much going to educate you on what healthier fast food choices are. We will also analyze health food and give a recommended macro nutritional ratio of Protein, Fat and Carbs of 25/35/50 that will promote a healthy life style.



Process 1:
----------

Querying Site: (Collective Fast Food Restaurants and Nutrition’s for meals served)

During this process we have acquired some data from the following link:

Link: http://www.acaloriecounter.com/fast-food.php

The above link consists of a site, which has majority of Fast Food restaurants. This site contains 
10 tables which we will use in various forms, each particular and joined in a series of analysis.


Process 2:
----------

Parsing Table:

While parsing through the tables a few issues came to light, such as the Onion Rings table which would contain a missing column, we’ve handled the issue using some coding in a python for loop. We’ve resulted to returning the text in the tables, and further returning the text into another for loop. In order to process the Data Frames for each table in an automated manner. This resulted in a special function jus to parse the onion rings table. This process resulted in more use of memory, but given that we’ve only have one onion ring table, refactoring the code at that point seemed a bit too much for the results that were desired. 

After this issue was handled, we've also created an automated format to do the following extra columns for each
table in the Data Frame:

We also noticed while performing the tidying of data that the protein information was missing, with a few calculations, we've managed to attain some more information from the pre-existing tables, which aided in our analysis.

We then find the ratio of the fat, protein and carb of each meal. With this information we were able to analyze and select the rows in which matched our caloric recommendation.

We've also proceeded to create a SQL database using pythons sqlite3, using sql.write_frame, it provides a light
use of code, and creates a relational database.

Conclusion:
===========


Figuring which food fits our macro breakdown

25% Protein, 35% Fat, 50% Carbs
-------------------------------

The resulting food are healthy and can be eaten on the go. Depending on your health, you might want to check the sodium levels.
