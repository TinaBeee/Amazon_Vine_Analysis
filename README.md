# Data Analysis with Spark, AWS & Postgres
Analysis of Amazon review dataset using Spark in Google Colab, AWS server and Postgres to determine whether there is a difference in the performance of unpaid reviews and paid reviews as part of the Vine program.

## Resources
- Data: Amazon AWS S3 U.S. Luggage Review dataset: https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt
- Sofware: Google Colaboratory, AWS RDS and S3, pgAdmin 4 Version 5.5

## Analysis
Analysis of U.S. Amazon luggage review dataset, which among others includes star rating, number of helpful votes, total votes, and whether or not the review was part of the paid Vine program. Initially filtering for reviews that have received at least 20 votes:

<img width="529" alt="Screen Shot 2022-02-12 at 22 22 40" src="https://user-images.githubusercontent.com/90064437/153738501-18b3af3d-11b6-4499-87e1-359ed9ac6768.png">

Next filtering for reviews where the share of helpful votes to total votes is at least 50%

<img width="1014" alt="Screen Shot 2022-02-12 at 22 25 00" src="https://user-images.githubusercontent.com/90064437/153738570-92ce96b0-7d13-4ab4-9c2e-87fa49900fcf.png">


## Results
Splitting those results based on paid reviews as part of the Vine program and regular reviews not paid for yields the following results:

<img width="567" alt="Screen Shot 2022-02-12 at 22 28 01" src="https://user-images.githubusercontent.com/90064437/153738618-1f9262eb-701c-4436-864c-855f607c91ae.png">

<img width="612" alt="Screen Shot 2022-02-12 at 22 28 37" src="https://user-images.githubusercontent.com/90064437/153738635-5170e710-3a66-4263-a23d-ec6f0e6c1e47.png">

## Summary
There appears to be no positivity bias when it comes to the Vine program. In fact, reviewers paid for under the Vine program appear to be more critical of the products than those not paid for reviews. However, the sample size for Vine reviews is very small (only 21 reviews were found after the original filtering methods were applied), compared to nearly 6,700 regular reviews.

Further analysis could include a statistical analysis to determine whether the results are statistically significant. The restrictions for the initial criteria could also be loosened, for example by counting all reviews that received at least 10 votes. That would allow for further analysis to determine whether paid reviews are less likely to be deemed helpful or voted on.
