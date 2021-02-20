# Extracting Covid-19 Economic Impact Using Common Crawler

**Task:** With this coding exercise, I was asked to extract 1,000 URLs from the 2020 archives of Common Crawler that discusses or are relevant to Covid-19 economic impact. 

As stated in the prompt, there is an ambiguous exercise that can be approached in many ways. To not be overwhelmed by the possibilities, I first created an outline of how to attack this large dataset.

1. Identifying trends: Given the time constraint of this project, I wanted to go after low-hanging fruits by first running the query through Google Trends. Using the pytrends package, I found that the majority of queries regarding covid-19 within the business news and fiscal policy news section occured around March-April 2020. I also found most relevant queries to contain keywords such as "stimulus", "stimulus checks", and "unemployment benefits." Using this information, I centered my search queries around those keywords and timeframe.

2. Regex: Using regex to isolate relevant URLs was the most challenging part of this exercise. Given the structure of the dataset. I settled on looking only at results that starts with "https://" to narrow down my searches and only looked at results with my relevant keyword "covid" or "covid-19" after a ".com" domain. Given the time contraint and the limits of my computer, I was only able to parse through of this segment for March-April 2020: http://commoncrawl.s3.amazonaws.com/crawl-data/CC-MAIN-2020-16/segments/1585370490497.6/warc/CC-MAIN-20200328074047-20200328104047-00000.warc.gz

3. I then appended the results to a list which I then filtered results to only keep results that have the following words within the URL: stimulus, check, economic, unemployment and benefits. 

**Other approaches considered:**
1. Looking at particular newspapers: This seemedm like the most straighforward approach by isolating only reowned newspapers to filter out search results. However, in practice I found this difficult given that the URLs can be ID numbers and does not have keywords related to Covid-19.
2. Looking only into social media posts and blogs: If given the time, it would have been interesting to use this exercise to look into posts and blogs concerning covid-19 and economics situation

**Lessons Learned:** If I were to repeat this exercise, I would try to optimize my regular expression to more efficently run through my query. Loading my query took a significant amount of time. One potential way to do this include making sure the query include the specific keywords from the Google Trends report rather than filtering for the keywords at the very end. 



