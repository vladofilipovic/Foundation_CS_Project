# Asignment

You have to work on the [Kiva](https://drive.google.com/file/d/1-tJtnIbo1Rt-F1XfoWGVkmBXiI-ciuRx/view) dataset. Some information on the datasets are on the [Kaggle](https://www.kaggle.com/gaborfodor/additional-kiva-snapshot) web page.

## For all

All groups and individual must do the following:

1. Normalize the `loan_lenders table`. In the normalized table, each row must have one `loan_id` and one `lender`.

2. For each loan, add a column `duration` corresponding to the number of days between the disburse time and the planned expiration time. If any of those two dates is missing, also the duration must be missing.

3. Find the lenders that have funded at least twice.

4. For each country, compute how many loans have involved that country as borrowers.

5. For each country, compute the overall amount of money borrowed.

6. Like the previous point, but expressed as a percentage of the overall amount lent.

7. Like the three previous points, but split for each year (with respect to `disburse time`).

8. For each lender, compute the overall amount of money lent. For each loan that has more than one lender, you must assume that all lenders contributed the same amount.

9. For each country, compute the difference between the overall amount of money lent and the overall amount of money borrowed. Since the country of the lender is often unknown, you can assume that the true distribution among the countries is the same as the one computed from the rows where the country is known.

10. Which country has the highest ratio between the difference computed at the previous point and the population?

11. Which country has the highest ratio between the difference computed at point 9 and the population that is not below the poverty line?

12. For each year, compute the total amount of loans. Each loan that has planned expiration time and disburse time in different years must have its amount distributed proportionally to the number of days in each year. For example, a loan with disburse time December 1st, 2016, planned expiration time January 30th 2018, and amount 5000USD has an amount of 5000USD * 31 / (31+365+30) = 363.85 for 2016, 5000USD * 365 / (31+365+30) = 4284.04 for 2017, and 5000USD * 30 / (31+365+30) = 352.11 for 2018.

## For 2+

The following part of the exercise must be done only by groups with two or three people:

1. For each value of repayment_interval, add a new column to the lenders dataframe that contains the total amount of money corresponding to loans in such state

2. What is the occupation with the highest average amount of money lent (the average must be computed over all lenders with a given occupation)?

3. Cluster the loans according to the year-month of disburse time.

4. For each country, compute its overall GNI, by multiplying the per capita GNI with its population.

## For 3+

The following part of the exercise must be done only by groups with three people

1. Find the country with the highest rate of irregular repayment interval.

2. Find the country with the highest fraction of loaned amount with irregular repayment interval.

## Notes

1. It is mandatory to use GitHub for developing the project.

1. The project must be a jupyter notebook.

1. There is no restriction on the libraries that can be used, nor on the Python version.