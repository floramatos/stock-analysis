# An Analysis of Wall Street Stocks Performances in 2017 and 2018

## Overview
With the goal of providing insights for stock investors, a VBA coding script was refactored to improve the analysis of a dataset containing information on Wall Street stocks performances for the 2017 and the 2018 years.

## Results
Two main analysis were performed. First, it was examined whether Wall Street stocks performances varied between 2017 and 2018. Second, it was examined whether the execution time of the refactored VBA script was improved compared to the execution time of the original VBA script.

### Analysis of Stocks Performance by Year
To examine the 2017 and 2018 performances of 12 tickers (AY, CSIQ, DQ, ENPH, FSLR, HASI, JKS, RUN, SEDG, SPWR, TERP, and VSLR), total daily volumes and yearly return were measured.

There was no difference across years with respect to the sum of shares traded daily, as the mean total daily volume was 263,886,592 (SD = 223,399,063) for 2017 and 275,503,183 (SD = 187,464,064) for 2018. As seen in Chart 1 below, most tickers had small increases or decreases in total daily volumes between 2017 and 2018. Exceptions were FSLR and SPWR with large decreases in total daily volumes from 2017 to 2018, and ENPH and RUN with large increases in total daily volumes from 2017 to 2018.

Chart 1
![Total_Daily_Volume_Chart](https://user-images.githubusercontent.com/89421440/139780659-957fb5b0-9d24-4b10-ad05-08c8688a8c10.png)

With respect to yearly return, there was an overall positive trend in 2017 and a negative one in 2018. As seen in Table 1, the only tickers with positive returns for 2018 were ENPH and Run, 81.9% and 84% returns respectively. As these tickers were the ones with increased total daily volumes, it is possible to hypothesize the existence of a linear correlation between total daily volume and yearly return that requires further analysis.

Table 1
![Yearly_Return_Table](https://user-images.githubusercontent.com/89421440/139780724-eb280b32-8eee-4166-88f3-0aa54e7553c0.png)

### Analysis of Scripts Execution Times
The main difference between the original and the refactored script used in the analysis presented here was the removal of a nested loop. The original script included the following nested loop:

![Original Script](https://user-images.githubusercontent.com/89421440/139780796-c376aaa1-68aa-4654-9074-368bad917593.png)

By creating one additional variables and arrays, it was possible to break the nested loop into three different loops:

![Refactored Script](https://user-images.githubusercontent.com/89421440/139780902-03e3e8c2-840a-42a3-bb20-482a66019041.png)

This change reduced the script execution time significantly, from 0.48 seconds to 0.07 seconds.

## Summary
- Besides improving the script execution time, the refactored code is more adaptive to future analysis that may include more stocks and years.
- Refactoring code was effective for this project but overall refactoring code can be challenging as coders may not understand the details of the script.
