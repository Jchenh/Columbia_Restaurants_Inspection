About my project:

I scraped the results of Columbia restaurants' safety inspections from the Columbia/Boone County Public Health and Human Services’ website. (The link is: https://www.gocolumbiamo.com/CMS/health_inspections/) I then used "agate" to analyze my data and used Tableau to map it.

How I made it:

1. I used Python to scrape the data I want from five restaurant inspection pages separately. I first extracted all the subpages' urls from the root page, and then loop over all the subpages to get the information I want. As I only want the most recent result, instead of using "find_all", I used "find" to get the first set of data. I then used “replace” to replace the content that I don’t need into "comma", which makes it easier when I imported the .txt data file into csv.

2. After getting the data in my terminal, I put it into a txt.file, and then imported it into csv. As the data is very dirty and there are only about 490 lines of rows, I went through each row and made sure that there was no repeating data or irrelevant restaurant. I also converted addresses into geocode for mapping the data later.

3. I then used "agate" to analyze my data. According to my analysis, the median critical violation and median non-critical violation of Columbia restaurants are both 0, which is pretty good in general. El Tigre, a Mexican restaurant, had nine critical violations, ranking the first in the latest inspection. Among the top ten restaurants with the most critical violations, five are Asian restaurants.

In terms of non-critical violation, Chinese Wok Express ranked the first with a total of nine non-critical violations. Surprisingly, Kaldi’s Coffee ranked the fifth, which had five non-critical violations.

I then combined the critical and non-critical violations, and the data suggests that Chinese Wok Express ranked the first again with 14 violations in total. The top five unsafe restaurants consist of four Asian restaurants and one Mexican restaurant.

4. Finally, I made a restaurant map by using Tableau, and published it at: https://public.tableau.com/profile/publish/FinalProject_166/Howsafeistherestaurant#!/publish-confirm. I used the critical violation as a filter, as this is the most important part in the inspections.

