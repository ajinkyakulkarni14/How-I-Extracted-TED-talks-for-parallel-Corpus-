# Multilingual TED parallel Corpus: How I Extracted TED talks for parallel Corpus?
----------------------------------------------------------------------------------------
Recently One of my lab mate was working on web scraping with BeautifulSoup for static web site and other was listening to TED talks with interactive transcripts in regional languages. Afterwards It struck to my mind what if I crawled the TED talks to create multilingual Corpus ?

TED Talks are videos that present a great idea in 18 minutes or less. They’re filmed at flagship TED conferences, independent TEDx events, and other special TED programs. Their goal is to share Ideas Worth Spreading — in fields like science, technology, business, culture, art and design — around the world. The Open Translation Project is a global volunteer effort to subtitle TED Talks, and enable the inspiring ideas in them to crisscross languages and borders.

Subsequently, Within few mins of reading documentation on urllib, Beautifulsoup and page source of TED.com. As a enthusisst in corpus lingusitics, I was able to appreciate significance of Multilingual parallel corpus for 109 world languages extracted from TED.com which is powered by open source Opentranslation project. In this article I am explaining the detailed flow of creation of parallel corpus from interactive transcripts of TED talks.

----------------------------------------------------------------------------------------
Prerequisites :
Python 2.7.6    Python Pandas   BeautifulSoup 
----------------------------------------------------------------------------------------
Step 1. Enlisting the TED talk names

TED.com is static website, so talks link location is static and can be acessed if we have prior information of talks details which can be derived through Beautiful soup and urllib library in python as given below

[!1][https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/1.png]



