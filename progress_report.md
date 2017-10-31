Kyle Landin ktl14@pitt.edu
# Progress Report

# 10/20 - 10/30
I've been working with the data and have moved the Characters and Pinyin to their own dataframes in the first topic: News Reportage. For some reason, when initially moving them to dataframes, each individual characters (both Chinese characters and individual letters/numbers) get their own column. This is mostly a problem for the pinyin because it caused the dataframe to have 39 columns. I figured out how to combine everything into a single column, but I don't know a better way to remove the excess columns other than doing it one at a time. The process I used is very inefficient and can definitely be improved.

One last problem that I don't know how to solve is that when I concatenate the Character dataframe and the Pinyin dataframe, the Characters show up fine for the first portion of the dataframe while the Pinyin shows up as NaN. This is reversed at the bottom of the table with Characters showing up as NaN an the Pinyin displaying properly. I also know that they aren't missing or adding more rows since both have 73517 rows.

# Initial Report
The first option I had in mind fell through as I am not fully capable of data acquisition on my own through web scraping and had to find a corpus that better suited my limited skill set. I have included a practice Jupyter file that I initially used to try and learn BeautifulSoup4 for web scraping. The corpus data I am using in this project is instead from the Lancaster Corpus of Mandarin Chinese (LCMC).

What I would like to do with this data is to better organize it, try to combine the Character data with its matching Pinyin (romanization) data. I would also like to try and display the parts of speech and possibly organize the data using it since the LCMC came with a key for their tagset. One more thing I would like to try is to figure out a way to include the English translations alongside the characters in each data set.

In regards to the scope of the data, there are 15 data sets total (30 if you count the Chinese character and the Pinyin data sets as individual). The different topics that the data sets cover are: news reportage, news editorials, news reviews, religion, skills, trades, and hobbies, popular lore, biographies and essays, miscellaneous reports and official documents, science: academic prose, general fiction, mystery and detective fiction, science fiction, adventure and martial arts fiction, romantic fiction, and humor. With all of these different categories, this corpus is able to provide much information from all walks of life.
