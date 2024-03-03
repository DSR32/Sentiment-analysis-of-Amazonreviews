# Sentiment-analysis-of-Amazonreviews
Create a Python notebook with a function called parse( )
The function should accept 3 parameters:
input_path: the path to the   'amazonreviews.csv' file.
index1: the row number that corresponds to a specific review in the given csv (first row would have index1=0)
index2: the row number that corresponds to another specific review in the given csv
The function should return a list of all nouns for which the review at index1 expresses the opposite opinion than the review at index2.
You should compute the opinion that a review expresses on a noun as follows:
Let P be the number of positive words that appear in the same sentence as the noun in the review
Let N be the number of negative words that appear in the same sentence as the noun in the review
If P>N, then the opinion of the review on the noun is positive.
If P<N, then the opinion of the review on the noun is negative
If P==N, then the opinion of the review on the noun is neutral.
 

Example:

suppose that review 1 says: "I really like this product, the quality is perfect. However, the price is unreasonable"

suppose that review 2 says: "This product has a great price."

review 1 has 2 sentences and 3 nouns:

I really like this product, the quality is perfect.     
However, the price of the product is unreasonable    
product: [2,1]: (2 positives, 1 negative) 

quality: [2,0]: (2 positives, 0 negatives)

price: [0,1]: (0 positives, 1 negative)

 

review 2 has 1 sentence and 2 nouns:

This product has a great price  
product: [1,0]: (1 positive, 0 negatives)

price: [1,0] : (1 positive,  0 negatives)

 

The nouns 'product' and 'price' appear in both reviews.

The overall opinion for 'product' in review 1 is: positive

The overall opinion for 'product' in review 2 is: positive.

The overall opinion for 'price in review 1 is: negative

The overall opinion for 'price in review 2 is: positive

In this case, the two reviews express an opposite opinion for the attribute 'price'. The first review expresses a negative opinion and the second review expresses a positive opinion.

Your function should return ['price']
