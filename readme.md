# A/B Testing to Validate Free Software Advertising Trial

## Introduction
The aim of this project is to investigate an advertising strategy of an e-commerce website to determine whether a new call to action (CTA) of a 7-day free software trial resulted in an increased software download rate (Downloads / Cookies (Unique Users) and increased License Sign Up Rate (Licenses / Cookies). The ultimate aim for the company was to increase revenue from Software Sales License Sales.

## Dataset
The data was a csv file which recorded the traffic on both Control and Experiment pages as well as the number of download and licenses purchased each day. The data was collected over a 29 day period.

Data required minimal cleaning, just some minor formatting of column titles.

As the data only had entries for a 29 day period and didn't appear to be normally distributed when plotted, it was decided to Bootstrap the data with replacement to estimate the Population mean and standard deviation.

## A/B Experiment Length

On average this website receives about 3250 unique visitors per day. Therefore, in order to accurately test both the Download and the License Experiments we would require at least 21 days. The experiment has been run for 29 days which is acceptable.

Seven of those days will not be a valid metric for measuring licenses because the trial period last 7 days and the benefit will only be realised after that period.

## Invariant Metric Review
To ensure a fair test was conducted and that users were randomly assigned to either the Control and Experiment landing pages, it was decided to split users by Cookie. To verify that the user split was random, a check was implemented to ensure that traffic remained constant over both Control and Experiment.

It is evident that there is a slight increase in traffic in the Experiment dataset approx 1%, but this is not statistically significant and there is insufficient data to suggest that the experiment is leading to higher traffic on the original home page.

## Conclusion
The 7-day free trial call to action conclusively demonstrated an increase in download rates, albeit small at +1.5% which equates to approximately 4 additional downloads per day, however it was unable to demonstrate a statistically significant difference in license purchases.

## Further Considerations
- License Rate may lag implementation by a period of 7-days because users are likely to get full value from the free trial.
- Dividing the users by cookies is ineffective if they choose to use incognito mode or a different browser.
- The lack of impact on license purchases may be attributed to the fact that more users are simply downloading the software when they have no real desire/requirement to purchase the final product. Further data would need to be gathered on customers to fully justify this argument.
