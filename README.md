# price_ab_test
A data challenge to explore the effect after increasing the price of the software. 

Company XYZ sells a software package for $39. Since revenue has been flat for some time, the
VP of Product has decided to run a test increasing the price. She hopes that this would increase
revenue. In the experiment, 66% of the users have seen the old price ($39), while a random
sample of 33% users a higher price ($59).
The test has been running for some time and the VP of Product is interested in understanding
how it went and whether it would make sense to increase the price for all the users.

Hints:

Remember who your audience is here (a VP of product) they are likely not technical.
How do you present your findings, how do you add context to your recommendation?
Was the test well formulated? How much time should it have been run to detect different
effect sizes?
Are there any holistic pieces of information that might change the idea that just upping
the price is a good thing?



Data
"test_results" - data about the test
Columns:
user_id : the Id of the user. Can be joined to user_id in user_table
timestamp : the date and time when the user hit for the first time company XYZ
webpage. It is in user local time
source : marketing channel that led to the user coming to the site. It can be:
ads-["google", "facebook", "bing", "yahoo", "other"]. That is, user coming from
google ads, yahoo ads, etc.
seo - ["google", "facebook", "bing", "yahoo", "other"]. That is, user coming from google search,
yahoo, facebook, etc.
friend_referral : user coming from a referral link of another userdirect_traffic: user coming by directly typing the address of the site on the browser
device : user device. Can be mobile or web
operative_system : user operative system. Can be: "windows", "linux", "mac" for web, and
"android", "iOS" for mobile. "Other" if it is none of the above
test: whether the user was in the test (i.e. 1 -> higher price) or in control (0 -> old, lower price)
price : the price the user sees. It should match test
converted : whether the user converted (i.e. 1 -> bought the software) or not (0 -> left the site
without buying it).
"user_table" - Information about the user
Columns:
user_id : the Id of the user. Can be joined to user_id in test_results table
city : the city where the user is located. Comes from the user ip address
country : in which country the city is located
lat : city latitude - should match user city
long : city longitude - should match user city
This challenge has been taken from the book "A collection of Data Science Take-home
Challenges" by Giulio Palombo.
