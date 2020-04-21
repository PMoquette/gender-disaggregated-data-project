![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# Approximating Gender-Disaggregated data in Conflict

### Purpose:

Using Natural Language Processing tools, I attempted to disaggregate the ACLED conflict data on Syria by gender. 

I was especially interested in the way gender is represented when talking about victims and perpretrators. 

Aggregating data by gender is an important step in ensuring (humanitarian) aid is needs-based. 

### Process:

1. I first started working on COD data, but decided to work with data from Syria instead, because:
    A. it is more complete
    B. it is fully in English, which removes an extra layer. I did start working on the COD dataframe, which can be found in the notebook `"cod-data-cleaning.ipynb` As both the Syria and COD dataframe come from the same [source](https://acleddata.com/#/dashboard) it wasn't lost effort, as it helped me get acquainted with the structure of the data.

2. Downloaded the ACLED dataframe through [HDX](https://data.humdata.org/dataset/acled-data-for-syrian-arab-republic)<br>
   Source: "Armed Conflict Location & Event Data Project (ACLED)"

3. The key data can be found in the 'Notes' column for the Syria dataframe. Based on this column, I extracted key phrases and words, each of which I gave a separate column (binary). 

4. I compared mentions of specific keywords and phrases with Event Type, to try and find a pattern. 

### Limitations:

Extracting key words and phrases was the first step, and it certainly yielded some interesting insights, but it did not take context into account. By eyeballing the data, for example, I found that 'women' were often mentioned when talking of victims, while the word 'females' was often used when it concerned perpretrators ("Female ISIS member," for example). Context matters, especially considering my initial draw towards this project was to see the gendered division between victimhood and perpretrator representation. 

I made a start with tokenization (extracting nouns and verbs) using TextBlob, and this would be something worth exploring further. 

### Codebook:

Source:<br>
Högbladh Stina, 2019, “UCDP GED Codebook version 19.1”, Department of Peace and Conflict Research, Uppsala University
[Source](https://ucdp.uu.se/downloads/)




