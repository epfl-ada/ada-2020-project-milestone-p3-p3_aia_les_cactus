# ada-2020-project-milestone-p3-p3_aia_les_cactus

Title: Socio-economic study on disparities inside a mexican slum

Abstract:
Although the program is effective, it’s not clear who benefits the most. Are there heterogeneous effects? To answer this question we search correlations between the variables on which the article showed that PisoFirme had a positive effect and engineered variables. Looking at the correlations, we find some interesting results concerning the number of children per household and the financial situation of the household. These results are even representative of worldwide trends. Aside from that, still focussed on social repercussions, we investigated whether or not PisoFirme had a Placebo effect using bootstrapped confidence intervals.

Research questions:
1. Can we find socio-economic trends in the population ?
2. How is the number of children in a household representative of the financial situation of the household ?
3. Did PisoFirme have a Placebo effect ?

Proposed dataset:
- PisoFirme_AEJPol-20070024_household.dta in the article’s dataset. It provides us with all the useful information: the demographic, economic, cement-floors-related and “psychological” data that we need.
- children-per-woman-by-gdp-per-capita.csv from https://ourworldindata.org/grapher/children-per-woman-by-gdp-per-capita?tab=chart&country=&region=World. It provides us with some insightful informations on the GDP per country in the world and the number of children per woman per country
- child-mortality-gdp-per-capita.csv from https://ourworldindata.org/grapher/child-mortality-gdp-per-capita. It provides us with some insightful informations on the GDP per country in the world and the child mortality per country
These 2 latter datasets serve as comparison to the results found in the first dataset.

Methods:
- Features engineering: For the correlation part, we will create features that summarize multiple related features. For example, for the level of education, we will take the mean of the level of education of the people running the household (mother and / or father). Similarly, we will regroup the variables corresponding to the access to electricity, water and garbage collection.
- Correlation: To compute the correlations, we will use both Pearson and Spearman correlations looking for any correlation, linear or not, using both the features described in the previous paragraph and some carefully chosen dependant variables.
- Regression analysis: we will perform linear regression on previously transformed features to model the relationship between the financial situation of a household and its number of children. Looking at the R² coefficient will tell us how well the model fits.
- Bootstrapped confidence intervals on the difference of Beta coefficients : in order to find out whether or not PisoFirme ellicited a Placebo effect, we will find the Beta coefficients associated to the model: depression (/ stress) = f(difference in share of cement between 2000 and 2005). With the help of bootstrapped confidence intervals, we will evaluate whether or not the betas are similar and thus if we can suppose a Placebo effect or not

Proposed timeline:
- Week 1: Clean the data, engineer / select the features, create the appropriate datasets.
- Week 2: Build the correlations, the linear models and the bootstrapped confidence intervals.
- Week 3: Improve data visualization and data analysis, work on the data story / video.

Organization within the team:
- Arthur will work on the correlation task for the first two weeks and then on data visualization in order to include meaningful plots / tables in the presentation in collaboration with Ilaria. He will also work on possible extensions given the results he obtained.
- Ilaria and Alice will work on features engineering and on finding relevant datasets for the first two weeks. Ilaria will work on the bootstrapped confidence intervals for the Placebo effect and together with Alice she will write the report.
