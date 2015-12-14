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


Conclusions
=============

Not Many Fast Foods are healthy





General Code in Notebook: 
-------------------------

(Used to Parse and Create DataFrames in automated Format)


Tables Code:
^^^^^^^^^^^^

[ Tables ]
``````````

.. code-block:: python

Table_Names = ['Fries',
               'Hamburgers',
               'Sandwiches_Hamburger',
               'Chicken_Pieces',
               'Chicken_Sandwiches',
               'Onion_Rings',
               'Bkfst_Sandwiches',
               'Mozzarella_Sticks',
               'BreadSticks_CheesyBread',
               'Pizza_Large14'
              ]

    def parse_table(table):
    results = []
    counter = 0
    table_row = []
    for row in table:
        try:
            table_row.append(float(row))
        except Exception as e:
            table_row.append(row)
        counter += 1
        if counter % 9 == 0:
            results.append(table_row)
            table_row = []
    return results
    
    

[ DataFrame ]
`````````````
.. code-block:: python

def easy_dataframe(table_list, table_catg):
    df_object = pd.DataFrame(table_list, columns = table_catg)
    return df_object.replace('Unknown', 0)

counter = 0
for item in Table_Names:
    exec('{} = easy_dataframe({},{})'.format(item.strip(),
                                             parse_table(TABLES_DATA[counter]),
                                             TABLE_CATEGORIES))
    counter += 1
    
