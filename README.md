# say_my_name
Exploring Breaking Bad's episodes transcripts and making some cool plots.

## Table of Contents
- General Information
- Setup
- Usage
- Challenges
- Project Results
- Future Data Exploration Ideas
- Acknowledgements
- Contact

## General Information
I’m uploading the code of the data I explored from the TV series "Breaking Bad", my favourite of all times!🚛🥼⚗️

The goal was to explore the transcript of the TV series to see if I could find any interesting pattern. I extracted each episode's transcript from an online website and then constructed a data frame with each season, episode number, episode title, character's name, and character's sentence. I also want to support other coders who are BB (or any TV Series/ movies) lovers just like me and want to learn how to plot their own data visualisations!📈

I used a website with Breaking Bad's transcripts available on [Forever Dreaming](https://transcripts.foreverdreaming.org/viewforum.php?f=165), made up of 64 TV series's episodes. I used each episode's URL to download all the webpage source code. This allowed me to extract the required part which included the data I wanted (i.e., transcripts, episode title, number, and season). Once that's done, I then built a data frame, cleansed the data, explored it, analysed it, and made some plots.

## Setup
First off, make sure you have conda🐍👀:

`conda create -n <replace-with-name-you-want> python=3.11`

`conda activate <replace-with-name-you-want>`

`pip install -r requirements.txt`

## Usage
Check out the following files in my repo to see how I've extracted, cleansed, explored, analysed, and plotted the data! 

- `data_processing.ipynb`
- `data_exploration.ipynb`
- `data_clustering_and_network_analysis.ipynb'

## Challenges
One of the biggest challenges was extracting the data from the text of the webpage source code. It wasn't easy to navigate through the webpage source code and find the relevant text. We used the `find()` function and the indices of the substrings to find the transcripts' start and end. This helped us remove any unnecessary text that is unhelpful to our analysis. We also got an error when splitting transcripts into character's names and sentences. This was depending on where the colon was (e.g. `['Walter: "My name is Walter White"']`. With a `Try and Except` statement, we found out that the splitting was not working for some transcripts. This was because, in some text, the colon was missing. We then realised that this was because the character's name itself was missing! This meant that we sadly couldn't use 2 out of the 5 seasons of the TV series. So we carried out our analysis and make our conclusions only with 3 out of 5 TV series of Breaking Bad: Season n1, 2, and 3.

## Project Results
Here are the main conclusions we reached so far:

![This text is displaying because the image is failing to load. To see the image, please click on `longest_sentence_by_char_chart.png`.](https://github.com/pheygiod/say_my_name/blob/main/longest_sentence_by_char_chart.png)

- The top 3 characters with the longest sentences are Hank, Walter, and Skyler. The top 3 characters with the shortest sentences are 'Everyone' (i.e., a group of people), Skyler, and Walter.

![This text is displaying because the image is failing to load. To see the image, please click on `longest_season_chart.png`.](https://github.com/pheygiod/say_my_name/blob/main/longest_season_chart.png)

- Out of all the seasons we managed to analyse, season 2 is the longest. Yet, we only managed to analyse season 1 and 2 and part of season 3. We couldn't analyse season 4 and 5 due to the character's names issue.

![This text is displaying because the image is failing to load. To see the image, please click on `scatter_plot.png`.](https://github.com/pheygiod/say_my_name/blob/main/scatter_plot.png)

- We found a linear correlation between longest sentences and the number of sentences. So he more sentences a character says, the longer their largest sentence is. This is because the main characters often speak profound and deep sentences.

![This text is displaying because the image is failing to load. To see the image, please click on `cluster_graph.png`.](https://github.com/pheygiod/say_my_name/blob/main/cluster_graph.png)

- We discovered that Jesse and Walter Jr have very distinguished clusters compared to other characters. Characters speaking similarly include women (e.g., Skyler, Marie, Jane), young characters (e.g., Walter Jr and Jane), and characters who discuss similar topics (e.g., Walter, Hank, and Saul).

![This text is displaying because the image is failing to load. To see the image, please click on `network_graph.png`.](https://github.com/pheygiod/say_my_name/blob/main/network_graph.png)

- The most frequent conversation happens between Walter and Jesse. The second one is between Walter and Skyler. The third strongest relationship is the one between Jesse and Jane.

## Future Data Exploration Ideas
We could find a way to label the missing transcripts with their character's names. We could also find a different dataset with all labelled transcripts. This would help us draw more accurate analysis on the show. 

##Acknowledgements 
A massive thank you to [Ward Haddadin](https://github.com/wardhaddadin1) for the awesome design of the data extraction process! It wouldn't have been such an enjoyable data adventure if it wasn't for your help!

Big kudos to [Dylan Castillo](https://dylancastillo.co/) for the fantastic article on how to cluster text using Word2Vec!

A special shoutout to `Ken Huang` for inspiring me. Your character network analysis of Harry Potter was astonishing! [Check it out](https://github.com/hzjken/character-network)!
Contact For any question, drop me a line at giorgiadt14@gmail.com and I'll be happy to help you out! Feel free to message me on LinkedIn too! Happy coding!💻

## Contact
For any question, drop me a line at giorgiadt14@gmail.com and I'll be happy to help you out! Feel free to message me on LinkedIn too! Happy coding!💻
