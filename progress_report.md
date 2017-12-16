Kyle Landin ktl14@pitt.edu
# Progress Report

# 12/8 - 12/14
I've been trying to do more data collection and analysis. The things I've come up with to look at are looking at different parts of speech and which words are most frequent and how often those parts of speech appear, looking at the relationship between formal and informal language within the corpus based on personal knowledge, and looking at pronouns to see if male, female, or gender neutral appear more frequently.

# 11/19 - 12/6
I've spoken with Narae about my difficulties and we agreed that it might just be easier to start over and just pull the .xml text into lists based on some of my other code. From there I zipped the character lists, pinyin lists, and part of speech lists together. After that I turned those values into tokens to make it easier to collect data. Using the Counter function from Collections made it very easy to find the most common words.
I was also able to create a dataframe of only unique words from the entire corpus and then used that to make a bar graph based on parts of speech.

# 11/4 - 11/12
I've finished transforming the .xml files into dataframes. Starting to try and figure out how to strip the tag values and add them to their own column in the dataframe.

# 10/31 - 11/2
I am about half way through transforming the .xml files into pandas dataframes. I still have not had time to figure out an easier way to remove excess columns other than removing them one at a time, but that isn't a huge problem. I also realized that I should not be using the .concat function with the dataframes and instead use the .merge. This solved the NaN problem I was having previously. I figured this out when looking at the shape of the dataframe and seeing that it was twice as long as it should be. In the next few days I will finish transforming the rest of the .xml files into dataframes and can hopefully move on to trying to create more columns that have the parts of speech or a translation. I would also like to try and remove duplicates, but I'm not sure how to go about doing that.

In terms of actual analysis, I am not entirely sure what to do for that. For hard numbers, the shortest dataframe so far is 28.5 thousand lines long and the longest so far is just over 130 thousand lines long.

# 10/20 - 10/30
I've been working with the data and have moved the Characters and Pinyin to their own dataframes in the first topic: News Reportage. For some reason, when initially moving them to dataframes, each individual characters (both Chinese characters and individual letters/numbers) get their own column. This is mostly a problem for the pinyin because it caused the dataframe to have 39 columns. I figured out how to combine everything into a single column, but I don't know a better way to remove the excess columns other than doing it one at a time. The process I used is very inefficient and can definitely be improved.

One last problem that I don't know how to solve is that when I concatenate the Character dataframe and the Pinyin dataframe, the Characters show up fine for the first portion of the dataframe while the Pinyin shows up as NaN. This is reversed at the bottom of the table with Characters showing up as NaN an the Pinyin displaying properly. I also know that they aren't missing or adding more rows since both have 73517 rows.

# Initial Report
The first option I had in mind fell through as I am not fully capable of data acquisition on my own through web scraping and had to find a corpus that better suited my limited skill set. I have included a practice Jupyter file that I initially used to try and learn BeautifulSoup4 for web scraping. The corpus data I am using in this project is instead from the Lancaster Corpus of Mandarin Chinese (LCMC).

What I would like to do with this data is to better organize it, try to combine the Character data with its matching Pinyin (romanization) data. I would also like to try and display the parts of speech and possibly organize the data using it since the LCMC came with a key for their tagset. One more thing I would like to try is to figure out a way to include the English translations alongside the characters in each data set.

In regards to the scope of the data, there are 15 data sets total (30 if you count the Chinese character and the Pinyin data sets as individual). The different topics that the data sets cover are: news reportage, news editorials, news reviews, religion, skills, trades, and hobbies, popular lore, biographies and essays, miscellaneous reports and official documents, science: academic prose, general fiction, mystery and detective fiction, science fiction, adventure and martial arts fiction, romantic fiction, and humor. With all of these different categories, this corpus is able to provide much information from all walks of life.
