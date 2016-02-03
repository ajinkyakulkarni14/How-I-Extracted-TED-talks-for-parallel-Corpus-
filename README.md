# Multilingual TED parallel Corpus: How I Extracted TED talks for parallel Corpus?
----------------------------------------------------------------------------------------
Recently One of my lab mate was working on web scraping with BeautifulSoup for static web site and other was listening to TED talks with interactive transcripts in regional languages. Afterwards It struck to my mind what if I crawled the TED talks to create multilingual Corpus ?

TED Talks are videos that present a great idea in 18 minutes or less. They’re filmed at flagship TED conferences, independent TEDx events, and other special TED programs. Their goal is to share Ideas Worth Spreading — in fields like science, technology, business, culture, art and design — around the world. The Open Translation Project is a global volunteer effort to subtitle TED Talks, and enable the inspiring ideas in them to crisscross languages and borders.

Subsequently, Within few mins of reading documentation on urllib, Beautifulsoup and page source of TED.com. As a enthusisst in corpus lingusitics, I was able to appreciate significance of Multilingual parallel corpus for 109 world languages extracted from TED.com which is powered by open source Opentranslation project. In this article I am explaining the detailed flow of creation of parallel corpus from interactive transcripts of TED talks.

----------------------------------------------------------------------------------------

#Step 1. Enlisting the TED talk names

TED.com is static website, so talks link location is static and can be acessed if we have prior information of talks details which can be derived through Beautiful soup and urllib library in python as given below

![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/1.png)
![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/2.png)
Thus, reference names of all TED talks is stored in all_talk_names as dictionary, to assist in crawling the translation data of talks.
![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/3.png)

-----------------------------------------------------------------------------------------
#Step 2. Extracting translations of TED talks data

![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/4.png)
Text data of talks consisted of time frames, translated text of available language and language code. So to maintain this hierarchy we have used pandas DataFrame to store collection of dictionaries containing aligned text and time frames with other languages which is saved in .csv file format. For this it required more than 48 hrs, extracting 2100+ TED talks of around 800MB text data.
![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/5.png)

------------------------------------------------------------------------------------------

#Step 3. Concatenation of all TED talk csv files to single Data Frame
To access text data of 109 languages of all talks , we need to store it in unified frame, for that all data in csv file is concatenated in single DataFrame df.
![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/6.png)
![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/7.png)

-------------------------------------------------------------------------------------------

#Step 4. Retrieving Parallel Corpus from all ted talk DataFrame df
To extricate the monolingual, bilingual and  multilingual parallel corpus, df[['ar','en','fr']] query is fired to access aligned text from tables in df.

![alt Step1](https://github.com/ajinkyakulkarni14/How-I-Extracted-TED-talks-for-parallel-Corpus-/blob/master/Img/8.png)

-------------------------------------------------------------------------------------------

TED Multilingual Parallel Corpus created using above process is available on github repository on above link :

https://github.com/ajinkyakulkarni14/TED-Multilingual-Parallel-Corpus

Source code : Ipython_notebook.ipynb

---------------------------------------------------------------------------------------------

#Author
Ajinkya Kulkarni

Contact
ajinkyakulkarni14@gmail.com

----------------------------------------------------------------------------------------------




