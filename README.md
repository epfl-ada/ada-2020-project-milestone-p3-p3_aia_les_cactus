# ada-2020-project-milestone-p3-p3_aia_les_cactus

Title: Detecting heterogeneous effects in the benefits of Piso Firme

Abstract:
Although the program is effective,it’s not clear who benefits the most.Are there heterogeneous effects?To answer this question we search correlations between the variables on which the article showed that PisoFirme had a positive effect and engineered variables x*y(x represents the fraction of rooms with cement in the house and y is a variable that could affect the impact of having cement floors).First,we want to know if cement floors have an impact because of sanitary and aesthetic reasons or also because they’re given through a state program(placebo effect).For that we will fit a regression similar to the ones in Table6,but only with statistically significant variables,and compare means between Torreon and the houses in Durango that have cement floors only.Additionally,we will add a dependent variable to account for the number of children born in the wake of the program,to see if PisoFirme had an impact on the number of births.

Research questions:
1. Did PisoFirme have a heterogeneous impact on the population ?
2. Did PisoFirme have a placebo effect ?
3. Did PisoFirme have an effect on the number of births ?

Proposed dataset:
- PisoFirme_AEJPol-20070024_household.dta in the article’s dataset. It provides us with all the useful information: the demographic, economic, cement-floors-related and “psychological” data that we need.

Methods:
- Features engineering: For the correlation part, we will create features that summarize multiple related features. For example, for the level of education, we will take the mean of the level of education of the people running the household (mother and / or father). Similarly, we will regroup the variables corresponding to the access to electricity, water and garbage collection. Afterwards, we will multiply these variables by the share of room with cements to create the variable x * y that we discussed in the abstract.
- Correlation: To compute the correlations, we will use the correlation matrix, using both the features described in the previous paragraph and the dependent variables used in tables 5 and 6. We will then focus on the square where the features interact with the dependent variables.
- Features selection: For the regression part, we will begin with all the features used in table 6 and then use PCA to drop the non-significant features.
- Regressions: We will train linear regression models based on the previously selected features. Only the households with cement floors will be taken into account (for Durango and Torreon). The treatment will be the application of Piso Firme, just as in the article.
- Number of births: We will compare the number of births between Torreon and Durango for the period 2000 - 2005. For that we only need to take into account the number of children between 0 and 5 years old. We want to know if the implementation of a state program has an influence on the number of births (people would feel that they have better means / conditions to raise their children).A bootstrapped confidence interval should be enough for this question.

Proposed timeline:
- Week 1: Clean the data, engineer / select the features, create the appropriate datasets.
- Week 2: Build the correlation matrix, the linear models and the bootstrapped confidence intervals.
- Week 3: Improve data visualization and data analysis, work on the data story / video.

Organization within the team:
- Arthur will work on the correlation task for the first two weeks and then on data visualization in order to include meaningful plots / tables in the presentation, in cooperation with Alice. He will also work on possible extensions given the results he obtained.
- Ilaria and Alice will work on the regressions for the first two weeks. Then Alice will work on writing the data story and possible extensions depending on the results while Ilaria will work on the bootstrapped confidence intervals for the number of births. 
