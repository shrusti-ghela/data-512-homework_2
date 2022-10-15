# data-512-homework_2

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment considers articles on political figures from different countries. For this assignment, I combine a dataset of Wikipedia articles with a dataset of country populations, and use a machine learning service called ORES to estimate the quality of each article.

I also performed an analysis of how the coverage of politicians on Wikipedia and the quality of articles about politicians varies among countries. My analysis consists of a series of tables that show:
- The countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
- The countries with the highest and lowest proportion of high quality articles about politicians.
- A ranking of geographic regions by articles-per-person and proportion of high quality articles.

There is also a short reflection on the project that focuses on how both my findings from this analysis and the process I went through to reach those findings helps me understand the causes and consequences of biased data in large, complex data science projects.

The source data for the Wikipedia articles on politicians comes from MediaWiki Action API which offers access to wiki features like authetication, page operations and search. The source data for the population data is the Population Reference Bureau, a private and nonprofit organization, that specializes in collecting statistics on the environment, and health and structure of populations.

Link to the Mediawiki Action API terms of use: https://foundation.wikimedia.org/wiki/Terms_of_Use/en

Other API documentation:
- https://www.mediawiki.org/wiki/API:Info
- https://www.prb.org/international/indicator/population/table

### Files in the repo

#### data:

- politicians_by_country_SEPT.2022.csv : The list of all the Wikipedia article pages on poiliticians by country used as the source data for looking up page quality values.
- population_by_country_2022.csv : The population dataset drawn from the world population data sheet that is used to combine with the politiciand data before analysis..
- wp_article_quality-no_match.csv : A list of the articles that do not have a ORES page quality value.
- wp_countries-no_match.csv : A list of all the countries that do not have match in the population dataset.
- wp_politicians_by_country.csv : The resulting dataset after combining the Wikipedia data on politicians with the population dataset. 

#### code:

- data_acquisition_and_data_analysis.ipynb - Code for collection and analysis of data.

#### results.ipynb: Notebook containing the tables resulting from the data analysis done in homework2.ipynb.

### Research Implications

One of the lessons I learned from the dataset is how important domain knowledge is when analyzing a given dataset. The data was gathered from the English Wikipedia, which is made up of English articles, and thus there is a potential bias towards English speaking regions. This could be one of the reasons for the large regional differences. This lack of diversity among politicians due to language barriers is concerning because it means that politicians from non-English speaking regions are not represented in decision-making. This can lead to biases in decision-making, which can have a negative impact on the policies that are implemented.

Q1. What biases did you expect to find in the data (before you started working with it), and why?

The language spoken in the country is one of the biases. More articles for that country are more likely if there are more English speakers in the country. Another potential bias that could be observed is that countries with good internet access contribute more to Wikipedia, resulting in more articles.

Q2: What might your results suggest about (English) Wikipedia as a data source?   

The findings indicate that there is more data on Wikipedia for English-speaking politicians, and as such, policymakers and researchers should keep this in mind before implementing any policy, as the data that leads to a conclusion about any region is biased towards one group of politicians (English speakers).

Q3: Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data? 

A realistic data science research scenario in which using these data (to train a model, conduct hypothesis-driven research, or make business decisions) may result in biased or misleading results due to the data's inherent gaps and limitations is when the data is used to study a phenomenon that is not well represented by the data. For example, if the data is used to study the effect of a new medication on a disease, but only a small number of patients with the disease are included in the data, the results may be biased or misleading. Similarly, in our dataset, the data was skewed toward English-speaking politicians. As a result of the data's inherent gaps and limitations, using it to train a model, conduct hypothesis-driven research, or make business decisions may produce biased or misleading results. 
