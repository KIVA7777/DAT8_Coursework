# Ciero Kilpatrick
#### Chipotle Homework For Week 2

##### Q1. Think for a minute about how the data is structured. What do you think each column means? What do you think each row means?
For our columns in the Chipoltle.tsv file, we see **order_id**,**quantity**,**item_name**, **choice description**, and **item_price**

* **order id** represents the particular order an item was ordered on. For instance, line 2-5 has an order ID of 1: This means that person A ordered (2) Chips and Salsa(one fresh tomato, one tomatillo), an Izze, and a Nantucket Nectar. As soon and ID 2 comes, that would be the next person in line, who ordered the chicken bowl. *Perhaps order_id 1 was two friends each getting chips and salsa and a drink for a light snack*.
* **quanitiy** simply tells us the amount of a particular item that was ordered for an id. For instance, order_id 2 is a chicken bowl and has a quantity of 2. Either someone is really greedy, or buying their friend a round of chipotle today.
* **item name** describes what the menu item is; Chicken bowl, Corona, Beef burrito, etc.
* **choice_description** explains the what about the item name, and is good for gathering other information or data on the order of a particular item, i.e. Clementine Izze, or the toppings added to a basic steak taco
*  **item_price** is the price of that particular order item
* Each row is then pretty much read out, so line 1 is seen as the first customer orders 1 chips and Salsa, and its choice description is null because there's not really a variant or a way to modify it past what it's item name is. Line 15 and 16 is seen as the seventh customer orders 1 chicken bowl, with corn salsa, rice black beans cheese and sour cream, and an our of chips and guac.

##### Q2. How many orders do there appear to be?
Seems to be 1834 orders
##### Q3. How many lines are in this file?
4,623
##### Q4. Which burrito is more popular, steak or chicken?
`grep -i ''_____'burrito' chipotle.tsv | wc -l` 'chicken' yields 553; 'steak' yields 368. Chicken burritos look more popular.
##### Q5. Do chicken burritos more often have black beans or pinto beans?
Black Beans: 282 , Pinto beans 105
##### Q6. Make a list of all of the CSV or TSV files in the DAT8 repo (using a single command). Think about how wildcard characters can help you with this task.
`find -name *.tsv` ?
##### Q7. Count the approximate number of occurrences of the word "dictionary" (regardless of case) across all files in the DAT8 repo
`grep -r 'dictionary' | wc -w` yields 116
##### Q8. Optional: Use the the command line to discover something "interesting" about the Chipotle data. Try using the commands from the "advanced" section!
`sort -k 5,5 chipotle.tsv`

1786 | 4  |     Chips and Guacamole   |  NULL   | $17.80

From reading through the data, this was the highest someone paid for chips and guac that day
