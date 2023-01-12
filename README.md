# World Nations Statistics Exploration

<img src="https://user-images.githubusercontent.com/95157802/212000132-d2621f4c-4d1e-477a-8406-0221c17d581b.PNG" width=50%>

This study aims to __investigate statistics surrounding nations around the world__, in particular population, GDP and languages spoken. __SQL__ will be used to query the World Nations [MariaDB Sample Database](https://www.mariadbtutorial.com/getting-started/mariadb-sample-database/) to select specific data, and reveal information around a set of questions outlined in the Jupyter notebook.

The following key questions will be answered:

1. What countries have the highest GDP per Capita?
2. How much growth have the most populous countries experienced over recent decades?
3. What are the most densely populated countries?
4. Which languages are most commonly spoken? What countries speak the most different languages?
5. Is there a most common month for a countries' national days?

## This repo includes the following:

- "_Exploring_World_Nations_Statistics.ipynb_" - Jupyter notebook showcasing SQL statements to query key information from relational database, and the associated output from the query.

## Insights

Althought the __Jupyter notebook is more thorough and captures the associated SQL queries and additional markdowns that help explain the project and thinking process__, below are _some_ of the main insights and visualizations of this project:

### __Insights on GDP per Capita of countries__

![country pop and ranks](https://user-images.githubusercontent.com/95157802/212001177-5d867ab2-dc55-4b49-90d3-0fd999f8abb7.PNG)

![gdp per capita vs time](https://user-images.githubusercontent.com/95157802/212000132-d2621f4c-4d1e-477a-8406-0221c17d581b.PNG)

- Amongst the top 10 GDP per Capita countries, most are from Europe and Asia. 
- Australia has the 11th highest GDP per Capita, 13th highest GDP and 52nd largest population (in the year 2018).
- Out of the 239 countries in the dataset, most of the top 10 highest <code>gdp_per_capita</code> countries have population sizes smaller than the 100 largest population countries, as indicated by the <code>population_ranking column</code>.
- The above statement makes the United States an exception, given it has the 9th highest <code>gdp_per_capita_ranking</code>, with the highest country GDP of all countries, and the 3rd highest population size of all countries.

### Insights on Population Growth of most Populous Countries

![country and pop change](https://user-images.githubusercontent.com/95157802/212002100-b9bf58e8-5241-4161-823d-747f0d087193.PNG)

![most pop pop growth 10 years](https://user-images.githubusercontent.com/95157802/212002112-0de88178-35a4-4017-904a-9dc08a010718.PNG)

- Out of the 10 most populous countries, Nigeria and Pakistan have seen the highest proportional increase to their populations in their last 10 and 50 years.
- The 2 most populous countries, China and India, are the only countries to have over 1.3 billion people, with the next largest population being the US at 327 million people.
- Although Japan has the 10th largest population size, the country has seen a decline of 1.21% of its population size over the last decade.

Before moving on, let's see how the world's total population has changed over the last 10 and 50 years...

### Insights on World Population Growth

![world pop snapshot](https://user-images.githubusercontent.com/95157802/212002645-135760f0-592e-4db0-8296-b26ff82b9686.PNG)

- Overall, the data indicates that the __world's population__ has increased by 11.37% over the last 10 years, and 60.86% over the last 50 years. Although the former figure of 11% appears correct, the latter shows a discrepancy to the 53% calculated based on the [Worldometer Website](https://www.worldometers.info/world-population/world-population-by-year/). This could be due to missing or incorrect data in the database of some country populations for specific years (e.g. Russia is missing its 1968 population as seen in an earlier query output).
- 53% increase to the world's population over 50 years indicates on average a 10% increase in the population each year.


### Insights on Population Density

![pop density](https://user-images.githubusercontent.com/95157802/212002814-664678f6-2039-45c0-9e44-81cd991d83b4.PNG)

- Macao, a special administrative region of China, has the highest population density of any country in the world, being more than 3 times higher than the 2nd most densely populated country, Singapore.
- There are 6 countries that have between 1,000 and 10,000 people living per square kilometre.
- Bangladesh is the 7th most densely populated country, and the only country in the top 10 most densely populated countries that has extreme values for its <code>population</code> and <code>country_area</code> compared to the other countries.


### Insights on Country Languages

![country num languages](https://user-images.githubusercontent.com/95157802/212002947-cfec6788-07c4-4c6e-b66d-14d44c2e6acf.PNG)

![num countries speaking language](https://user-images.githubusercontent.com/95157802/212003171-5b888c83-fe30-4299-8b0c-6e13c2ad883a.PNG)

![language and count](https://user-images.githubusercontent.com/95157802/212003062-454e003e-50ee-423e-b045-b6b1fd0aa052.PNG)

- There are 13 countries that speak 10 or more different languages and/or dialects, and 7 of these also have an official language (represented by the "1" in the <code>official</code> field).

- The language that has the __highest number of countries__ that speak it is the English language, followed by Arabic, Spanish, French and Chinese. This should not be confused, however, with the number of people that can speak the language.

### Insights on National Days

![national day month count](https://user-images.githubusercontent.com/95157802/212003410-d07ad66e-cfa8-4f86-a43c-57fc1c6f8681.PNG)

- Out of the countries that have National Days registed in the database, most National Days for nations globally take place on the months between July and December. It is interesting how National Days are consolidated in the latter half of the year!

## Conclusion

This project has allowed for an investigative analysis into the world of statistics about the world. It has revealed some information pertaining a nations' population, GDP, area, languages, national days, countries, continents and more.

By __using existing fields to engineer new meaningful fields we have extracted insights__ into statistics about world nations, such as calculating GDP per Capita, Percentage Change in Population, and Population Density. Aggregate functions such as <code>SUM</code> and <code>COUNT</code> were used to summarize data and return significant values as part of the statistical analysis.

Some interesting findings from the analysis included the difference in GDP per Capita and its change over time between first world and developing nations, the fact that Japan's population has declined between 2008 and 2018 despite it being one of the most populous countries, how Bangladesh is among the top 10 most densely populated nations yet it has considerably higher population and land area compared to the other 10 most densely populated nations.
