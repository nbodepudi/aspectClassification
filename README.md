# aspectClassification
This algorithm provides a basic approach to Aspect classification and Grouping of words in python.
All of the code are written in python2.7.

The algorithm which I used can be optmized.
This gives a basic idea of Natural Language Proccessing. 

First  code is about seperating required words which are used in analyzing the conext of the whole sentence for sensitivity analysis.
By seperating out required words mood of the sentence can be identified.

To solve this I took a dataset on which my algorithm trains to give the required data. 
Firstly the algorithm which I wrote learns from the training data. Here 3/4 data is used as training data and other 1/4 as testing data.
Here to train I used basic Naivebayes classification algorithm. In a word I considered its First letter case, last letter and last but one letter as its main features.
This can be modified based on the needs.
The accuracy of the algorithm depends on two things 1) technique used and features considered.
Here if the first letter is capital its most probably belongs to a class of nous which can be discarded. And other two criteria are two random creteria which I choose.

By running the algorithm on the training data our algorithm creates a classifier based on the training data with our given paramaters which can be used for prediction and other purposes.
Third part is the prediction part. Here the built classifier in the second step helps to predict outcomes on the given test_data or the new data.

Second task is clustering task. I used Kmeans algorithm to cluster the words. It measures distances between two data points and make them as a cluster. This is also a ML algorithm. The explanation of the steps followed are similar to the above task.


***********************************************************************
Results
************************************************************
Task-1
*********
To optimize further using the same algorithm we can add arguments in the function word_features.
By running the algorithm it prints the probability of correctness in test_data, precision, recall, f1-score and few data where the classifier is not agreeing with training_data

*Output*
stats:

probability of Correctness of the Test Data:
0.900579710145

number of true positive, false positive, flase negative are respectively:
(3107, 276, 67)

Precision:
0.918415607449

Recall:
0.978890989288

F1-score:
0.947689492146


Most Informative Features of the classifier:

                 suffix2 = 'z'               ASP : NASP   =     15.9 : 1.0
                 suffix2 = 'c'               ASP : NASP   =     11.2 : 1.0
             last_letter = 's'              NASP : ASP    =      9.7 : 1.0
             last_letter = 'o'              NASP : ASP    =      9.3 : 1.0
                 suffix2 = 'f'               ASP : NASP   =      8.6 : 1.0


****************************************************************
Task-2
******
Here for clustering the given data I used K-means algorithm as it is easy to use :P.

I used K-means algorithm. Here number of clusters are to be predefined. The number of clusters to which they were divided are for large data (n/20).

For small amounts of data this algorithm doesn't work.
I used tfid vectorization to vectorize the given tokens and use Kmeans on it.
Given data consists of 259 tokens so these data is divided into 12 clusters.
And those 12 clusters can be printed by running the algorithm.

We can change the number of cluster just by changing the value of n in the algorithm.

['moving', 'quarter', 'town', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'taste', 'kind', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'guest', 'noodle', 'bar', 'afternoon', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'First', 'party', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'chicken', 'area', 'owner', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'mozzarellum', 'oyster', 'post', 'Joya', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'Waitstaff', 'fat', 'feature', 'flair', 'menu-fare', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moule', 'model/waitress', 'mix', 'meeting', 'floor', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'food-quality', 'Statue', 'Guacamole', 'pad', 'Family', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'pasta', 'fries', 'kid', 'minute', 'rest', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'restraunt', 'ravioli', 'must', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'name', 'food']

['staff', 'quarter', 'waitress', 'guest', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'town', 'noodle', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'kind', 'party', 'chicken', 'bathroom', 'mozzarellum', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'afternoon', 'request', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'date', 'bar', 'post', 'area', 'drink', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'meal', 'waiter', 'fun', 'tuna', 'world', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'spot', 'lunch', 'neighborhood', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'owner', 'oyster', 'pad', 'Statue', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Waitstaff', 'Joya', 'pasta', 'Guacamole', 'fries', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'kid', 'minute', 'must', 'restraunt', 'Family', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'rest', 'name', 'ravioli', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'food']

['moule', 'mouth', 'quarter', 'town', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'special', 'taste', 'guest', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'group', 'noodle', 'kind', 'First', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'waitstaff', 'bar', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'party', 'chicken', 'area', 'owner', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'mozzarellum', 'oyster', 'post', 'Joya', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'Waitstaff', 'fat', 'feature', 'flair', 'menu-fare', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'model/waitress', 'mix', 'meeting', 'floor', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'food-quality', 'Statue', 'Guacamole', 'pad', 'Family', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'pasta', 'fries', 'kid', 'minute', 'rest', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'restraunt', 'ravioli', 'must', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'name', 'food']

['request', 'quarter', 'waitress', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'town', 'kind', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'guest', 'noodle', 'post', 'bathroom', 'mozzarellum', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'afternoon', 'party', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'chicken', 'bar', 'area', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'owner', 'oyster', 'pad', 'Statue', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Waitstaff', 'Joya', 'pasta', 'Guacamole', 'fries', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'kid', 'minute', 'must', 'restraunt', 'Family', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'rest', 'name', 'ravioli', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'food']

['salad', 'quarter', 'kind', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'town', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'guest', 'noodle', 'chicken', 'party', 'mozzarellum', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'date', 'bar', 'post', 'area', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'tuna', 'world', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'spot', 'fun', 'neighborhood', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'lunch', 'owner', 'oyster', 'pad', 'Statue', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Waitstaff', 'Joya', 'pasta', 'Guacamole', 'fries', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'kid', 'minute', 'must', 'restraunt', 'Family', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'rest', 'name', 'ravioli', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'food']

['dosa', 'quarter', 'guest', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'town', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'group', 'kind', 'bar', 'noodle', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'party', 'chicken', 'area', 'owner', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'mozzarellum', 'oyster', 'post', 'Joya', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'Waitstaff', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Statue', 'Guacamole', 'pad', 'Family', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'pasta', 'fries', 'kid', 'minute', 'rest', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'restraunt', 'ravioli', 'must', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'name', 'food']

['bar', 'kind', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'town', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'guest', 'noodle', 'post', 'party', 'mozzarellum', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'chicken', 'quarter', 'area', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'owner', 'oyster', 'pad', 'Statue', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Waitstaff', 'Joya', 'pasta', 'Guacamole', 'fries', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'kid', 'minute', 'must', 'restraunt', 'Family', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'rest', 'name', 'ravioli', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'food']

['atmoshere', 'quarter', 'town', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'taste', 'guest', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'group', 'kind', 'bar', 'noodle', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'party', 'chicken', 'area', 'owner', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'mozzarellum', 'oyster', 'post', 'Joya', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'Waitstaff', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Statue', 'Guacamole', 'pad', 'Family', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'pasta', 'fries', 'kid', 'minute', 'rest', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'restraunt', 'ravioli', 'must', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'name', 'food']

['kid', 'College', 'drink', 'money', 'hall', 'music', 'dumpling', 'crowd', 'crust', 'delivery', 'dining', 'quarter', 'conversation', 'glass', 'group', 'guest', 'cream', 'waitress', 'bottle', 'week', 'noodle', 'town', 'taste', 'special', 'size', 'flavor', 'deal', 'cuisine', 'course', 'room', 'kind', 'reviewer', 'party', 'location', 'pad', 'post', 'owner', 'mozzarellum', 'idea', 'hostess', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'part', 'date', 'planet', 'Service', 'meal', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'table', 'chicken', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'waiter', 'fun', 'lunch', 'decor', 'area', 'world', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'spot', 'neighborhood', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'pasta', 'oyster', 'plate', 'fat', 'factor', 'exprience', 'effect', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'salmon', 'Waitstaff', 'Statue', 'fallback', 'feature', 'Guacamole', 'flair', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'model/waitress', 'mix', 'menu-fare', 'meeting', 'mayo', 'maus', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'food-quality', 'floor', 'Joya', 'Winnie', 'Family', 'name', 'Chicken', 'fries', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'must', 'minute', 'noise', 'scallion', 'restraunt', 'rest', 'seating', 'tempura', 'ravioli', 'trouble', 'vibe', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'water', 'pastrami', 'occassion', 'occasion', 'weather', 'winter', 'notch', 'saturday', 'bathroom', 'rice', 'atmoshere', 'moule', 'moving', 'request', 'lettuce', 'staff', 'crab', 'bar', 'mouth', 'perfection', 'dosa', 'salad', 'food']

['food', 'kind', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'waitress', 'town', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'guest', 'noodle', 'post', 'party', 'mozzarellum', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'chicken', 'bar', 'area', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'owner', 'quarter', 'pad', 'Statue', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Waitstaff', 'Joya', 'pasta', 'Guacamole', 'fries', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'kid', 'minute', 'must', 'restraunt', 'Family', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'rest', 'name', 'ravioli', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'oyster']

['lettuce', 'quarter', 'waitress', 'group', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'crab', 'conversation', 'bottle', 'week', 'town', 'kind', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'guest', 'noodle', 'bar', 'afternoon', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'First', 'party', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'chicken', 'area', 'owner', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'mozzarellum', 'oyster', 'post', 'Joya', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'Waitstaff', 'fat', 'feature', 'flair', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'floor', 'meeting', 'mayo', 'maus', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'food-quality', 'Statue', 'Guacamole', 'pad', 'Family', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'pasta', 'fries', 'kid', 'minute', 'rest', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'restraunt', 'ravioli', 'must', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'perfection', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'name', 'food']

['crab', 'perfection', 'quarter', 'guest', 'glass', 'dumpling', 'dining', 'delivery', 'crust', 'crowd', 'cream', 'conversation', 'bottle', 'week', 'waitress', 'town', 'taste', 'special', 'size', 'music', 'money', 'flavor', 'deal', 'cuisine', 'course', 'room', 'part', 'location', 'date', 'group', 'kind', 'owner', 'noodle', 'mouth', 'idea', 'hostess', 'hall', 'favorite', 'establishment', 'entertainment', 'delight', 'caviar', 'bistro', 'beer', 'bathroom', 'afternoon', 'First', 'waitstaff', 'variety', 'tip', 'sum', 'street', 'soup', 'shrimp', 'setting', 'seafood', 'sake', 'reviewer', 'request', 'party', 'chicken', 'bar', 'area', 'world', 'cheese', 'ambience', 'bagel', 'appetizer', 'way', 'rice', 'dinner', 'people', 'experience', 'roll', 'fish', 'Thai', 'Service', 'table', 'atmosphere', 'sushi', 'wine', 'menu', 'dish', 'staff', 'pizza', 'friend', 'price', 'time', 'service', 'restaurant', 'place', 'drink', 'meal', 'waiter', 'spot', 'visit', 'value', 'sauce', 'quality', 'lobster', 'ingredient', 'gem', 'choice', 'chef', 'anything', 'wait', 'tuna', 'neighborhood', 'fun', 'husband', 'evening', 'dessert', 'Pizza', 'Food', 'sandwich', 'portion', 'order', 'family', 'decor', 'salad', 'lunch', 'mozzarellum', 'oyster', 'post', 'Statue', 'fat', 'fallback', 'factor', 'exprience', 'effect', 'dosa', 'deficiency', 'decour', 'daiquiry', 'crew', 'cost', 'candle-light', 'breast', 'branzino', 'beef', 'bargain', 'banquet', 'band', 'balance', 'attraction', 'atmoshere', 'assortment', 'apppetizer', 'amount', 'Yellowtail', 'Wong', 'Winnie', 'feature', 'flair', 'floor', 'mix', 'pepper', 'penang', 'patty', 'patron', 'pastry', 'panchetta', 'pancake', 'palate', 'operation', 'moving', 'moule', 'model/waitress', 'menu-fare', 'food-quality', 'meeting', 'mayo', 'maus', 'lettuce', 'lawn', 'laugh', 'knowledge', 'kiosk', 'juice', 'jersey', 'impecible', 'halibut', 'Waitstaff', 'Joya', 'pad', 'Guacamole', 'filet', 'fare', 'excuse', 'entree', 'deli', 'company', 'combination', 'chow', 'chip', 'cheeseburger', 'charm', 'Steak', 'Salad', 'Japan', 'work', 'view', 'type', 'surprise', 'style', 'stuff', 'something', 'server', 'sashimus', 'salmon', 'plate', 'planet', 'pasta', 'fries', 'kid', 'minute', 'restraunt', 'Family', 'College', 'Chicken', 'winter', 'weather', 'water', 'vibe', 'trouble', 'tempura', 'seating', 'scallion', 'saturday', 'rest', 'must', 'ravioli', 'quantity', 'potato', 'pizzeria', 'piece', 'pie', 'pastrami', 'occassion', 'occasion', 'notch', 'noise', 'name', 'food']
  
