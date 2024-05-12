# web-scraping-and-analysis

## Completed using Jupyter Notebooks launched from Anaconda

Initially I envisioned this project as scraping a list of news websites and looking for the hottest topics of the day across all of the sites combined. The plan was to then run this each day and perform a basic analysis (war up 10% today, Prince Harry down 20% this week etc) While the first part of this original plan is complete, it already tests the limits of my ageing desktop computer so the second part may take a bit of time. I have therefore decided to share it as it is. I think it still shows some useful Python skills!

In this project I scrape a list of provided urls and extract the text. If you run the notebook you will be prompted to add your list of website links.

The frequency with which each word occurs is then counted for each url. Double weighting is given to words found in the page title, as these are deemed more relevant.

Common 'stop words' are removed, and only words occuring more than once are kept.

I also extract links from the html soup and store internal and external links in separate list

Each URL is then removed from the list to be scraped and added to a list of scraped urls. Internal links are added into the original URL list to repopulate it. Optionally a second run will then scrape all internal pages linked from the homepage of each site. This is disabled by default. If you want to test this out please uncomment the following line at the bottom of the 4th cell:

#CrawlPage(urls)

But please be advised: unless you provide a short list of sites with a small number of pages linked from the homepage, or you have an absolute beast of a machine to run this on, you will probably have problems getting this to run.

The frequency dictionaries for each page is then combined into a final run index!

## Future Development

This is my current project and I am continuing to work on it. Here is my to do list:

Move out of Jupyter notebooks and run as standalone program to improve performance.
Search for common phrases using nltk.collocations rather than just looking at individual words.
Save final run index as CSV and perform analysis of changes over time.
