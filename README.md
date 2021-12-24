# Data-Science-Challenge

## Challenge #1: Hamlet

For this challenge, you can use R or Python.  Everything you need to perform this challenge should be available - but feel free to install additional packages should you need them. You can find file for this challenge in `/Data/hamlet.txt`

1. Show the number of lines said per character throughout the play.
2. Make word cloud of the script of the least common words.
3. Compute the sentiment score for each scene.

## Challenge #2: Unsupervised Learning

For this challenge, can you predict an _inferred" gender for a customers based on the user behavioural data?

### Task

There are four stages to this task:

**Stage 1** : *SQL* - A lot of our data lives in SQL databases, data scientists need to be comfortable using SQL.

Unhash the sqlite database (`/Data/sample-data/test_data.db.zip`) using the secret key provided by us, extract it.

Write SQL queries to answer the following questions:

*Note: At this stage it is ok to ignore the underlying errors in the data*

1. What was the total revenue to the nearest dollar for customers who have paid by credit card?
2. What percentage of customers who have purchased female items have paid by credit card?
3. What was the average revenue for customers who used either iOS, Android or Desktop?
4. We want to run an email campaign promoting a new mens luxury brand. Can you provide a list of customers we should send to?

**Stage 2** : *CLEAN* - Unhash the data (`/Data/sample-data/test_data.zip`) using the secret key provided by us, extract it, most importantly clean it and put it in a form you can use - all programatically of course. We have also "intentionally" corrupted two columns in this file - two columns that might look correct but are not correct. They need "some correction" to be useful.

**Stage 3** : *BUILD* - Build a model that suitably answers this question and predict the inferred gender using the features provided and deriving more featueres at your end. Remember, there is no gender flag, so you are flying blind here.

**Stage 4** : *DELIVER* - Package all your process, findings and code into a reproducible document that can be understood by a business user. A repo of the code branch would be a great thing to have! This **reproducible report**\* must answer the following questions:

1. How did you clean the data and what was wrong with it? Close to 90% of a Data Scientist's job is in cleaning data
2. What are the features you used as-is and which one did you engineer using the given ones? What do they mean in the real world?
3. What does the output look like - how close is the accuracy of the prediction in light of data with labelled flags?
4. What other features and variables can you think of, that can make this process more robust? Can you make a recommendation of top 5 features you'd seek to find apart from the ones given here
5. Summarize your findings in an *executive summary*

### Evaluation

We are looking for the following:

1. You can write good quality SQL queries
2. You clean the data - we expect to see how you identified and resolved the errors
3. You make sensible decisions
4. Your model achieves high accuracy on our held out labelled gender dataset
5. Your findings, code and executive summary are packaged in an easily reproducible package - given dependencies and other instructions, we should be able to re-run your source code with the dataset in the same directory and obtain the same results and figures. Popular formats for this include RMarkdown and Jupyter Notebook (formerly IPython)

### Data

Within the `/Data/sample-data/` directory we have provided 2 files:

1. For stage 1 we have included a SQLite database `test_data.db.zip`.
2. For stages 2 - 4 we have included `test_data.zip` which contains the data in newline delimited json format.

The files have been super encrypted - the password to the file is "an unserialized lowercase SHA-256 hash" of `welcometotheiconic`.

| Column                   | Value   | Description                                                              |
|--------------------------|---------|--------------------------------------------------------------------------|
| customer_id              | string  | ID of the customer - super duper hashed                                  |
| days_since_first_order   | integer | Days since the first order was made                                      |
| days_since_last_order    | integer | Days since the last order was made                                       |
| is_newsletter_subscriber | string  | Flag for a newsletter subscriber                                         |
| orders                   | integer | Number of orders                                                         |
| items                    | integer | Number of items                                                          |
| cancels                  | integer | Number of cancellations - when the order is cancelled after being placed |
| returns                  | integer | Number of returned orders                                                |
| different_addresses      | integer | Number of times a different billing and shipping address was used        |
| shipping_addresses       | integer | Number of different shipping addresses used                              |
| devices                  | integer | Number of unique devices used                                            |
| vouchers                 | integer | Number of times a voucher was applied                                    |
| cc_payments              | integer | Number of times a credit card was used for payment                       |
| paypal_payments          | integer | Number of times PayPal was used for payment                              |
| afterpay_payments        | integer | Number of times AfterPay was used for payment                            |
| apple_payments           | integer | Number of times Apple Pay was used for payment                           |
| female_items             | integer | Number of female items purchased                                         |
| male_items               | integer | Number of male items purchased                                           |
| unisex_items             | integer | Number of unisex items purchased                                         |
| wapp_items               | integer | Number of Women Apparel items purchased                                  |
| wftw_items               | integer | Number of Women Footwear items purchased                                 |
| mapp_items               | integer | Number of Men Apparel items purchased                                    |
| wacc_items               | integer | Number of Women Accessories items purchased                              |
| macc_items               | integer | Number of Men Accessories items purchased                                |
| mftw_items               | integer | Number of Men Footwear items purchased                                   |
| wspt_items               | integer | Number of Women Sport items purchased                                    |
| mspt_items               | integer | Number of Men Sport items purchased                                      |
| curvy_items              | integer | Number of Curvy items purchased                                          |
| sacc_items               | integer | Number of Sport Accessories items purchased                              |
| msite_orders             | integer | Number of Mobile Site orders                                             |
| desktop_orders           | integer | Number of Desktop orders                                                 |
| android_orders           | integer | Number of Android app orders                                             |
| ios_orders               | integer | Number of iOS app orders                                                 |
| other_device_orders      | integer | Number of Other device orders                                            |
| work_orders              | integer | Number of orders shipped to work                                         |
| home_orders              | integer | Number of orders shipped to home                                         |
| parcelpoint_orders       | integer | Number of orders shipped to a parcelpoint                                |
| other_collection_orders  | integer | Number of orders shipped to other collection points                      |
| average_discount_onoffer | float   | Average discount rate of items typically purchased                       |
| average_discount_used    | float   | Average discount finally used on top of existing discount                |
| revenue                  | float   | $ Dollar spent overall per person                                        |

All the best! Blow us away with your findings and accuracy!



