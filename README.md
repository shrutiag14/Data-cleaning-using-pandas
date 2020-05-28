# Data-cleaning-using-pandas

Challenge 1: Fix city names
The city names are dirty, for example:
HAIDRABAD, Hyderabad, Hyderabad
BANGLORE, BANGALORE, Bangalore, Begolore
GUJRAT, GUJARAT, GUJRAAT
AGARA, AGRA
कानपुर, Kanpur
Mumbai, MUMABAI, मुम्बई, मुम्बई भिवडी, VASAI MUMBAI

Your challenge is to fix these names.
One way is to replace them manually like we have done above for the Sex column.
Another way to do it is to use a look up table for replacements.
Use this to clean city names.

We have provided a look up table here (file: cityreplacement.csv)

You can use the upload file method above to upload this table and use it for replacements.

At the end of this task there should not be more than 1 variation for every city.

Challenge 2: 
Clean the YrsExp column
This column can contain many dirty values.
After clean up, all this column should contain is a number that represents number of years.
For example, any years > 10 should be replaced by 10,
and any value in months should be replaced by 0.

This column can contain these values:
['7 MONTH' '5 MONTHS' nan '2 YEARS' '1 YEAR' '6 MONTHS' '3 YEARS' '2 MONTHS' '5 YEAR' '7 MONTHS' '3 YEAR' '2 YEAR' '6 YEARS' '7 YEARS' '4 MONTHS' '4' '6' '7' '2' '8' '15' '5' '10 YEAR' '8 year' '25 YEARS' '3' '1' '1YEAR' '5 YEARS' '1 YERS' '06 MONTHS' '05 YEARS' '03 YEARS' '04 MONTHS' '02 YEARS' '03 MONTHS' '02 MONTHS' '01 YEARS' '4 YEARS' '10' '13' '3YEAR' '6YRS.' '5YRS.' '4YRS.' '7YRS.' '10YRS.' '9YRS.' '3 MOTH' '5 MONTH' '20' '6 YEAR' '33' '18' '11' '4 YEAR' '6 Month' '2 MONTH' '15 YEAR' '25' '40' '19' '27' '7 YEAR' '17 YEAR' '8 YEAR' '9 YEAR' '15 YEARS' '3 MONTH' '11 MONTHS' '6 MONTH' '11 YEARS' '10 YEARS' '12 YEARS' '8 MONTH' '9' '30' '12' '4 MONTH' '5 YERS' '3साल' '10साल' '1साल' '7साल' '5साल' '3 माह' '2 माह' '3 साल' '2 साल' '4साल' '2साल' '18साल' '30साल' '11साल' '40साल' '12साल' '6माह' '3माह' '13साल' '8साल' '3 वर्ष' '10 वर्ष' '8 माह' '7 वर्ष' '9वर्श' '3 बर्ष' '5 वर्ष' '5 माह' '8 वर्ष' '4 वर्ष' '2 वर्ष' '1 वर्ष' '6 माह' '4माह' '5 साल' '25 साल' '9 साल' '5माह' '6साल' '4Y' '20 YEARS' '40 YEAR' '5Y' '12 YEAR' '2MONTHS' '9o"kZ' '5o"kZ' '3o"kZ' '20o"kZ' '25o"kZ' '6MONTH' '10YEARS' '2YRS.' '2 YRS.' '2YRS' '1YRS' '8YRS' '2YEAR' '3YEAT' '5 YS' '8 MONTHS' '4 YS' '6 MTH' '15 YS' '22' '14' '30YEAR' '28' '12 साल' '1 साल' '15 साल' '20 साल' '10 साल' '4 साल']

Challenge 3: 
Clean the city names list using fuzzy string matching. Fuzzy string matching calculates string similarity.

Some examples:

String 1	String2	Match Score
Mumbai	Mumabai	92%
Mumbai	Vasai Mumbai	66%
Mumbai	Bangalore	13%
Bagalore	Bangalore	94%
Using this score, we could replace both the first two examples with

By using a list of possible options, you can look for matches that have a score higher than 60%, and replace them. You can use the list of options in the second column in this file : CITYREPLACEMENT.CSV

Read example tutorial here: https://towardsdatascience.com/how-to-do-fuzzy-matching-in-python-pandas-dataframe-6ce3025834a6
Experiment with similarity here: https://www.tools4noobs.com/online_tools/string_similarity/
