# Identifying-Reddit-Subject-Lexical-Diversity

## Identifying the subject of Reddit from its most commonly used words and finding the 3 lexical diversity of the subreddit
### Research Questions
It is commonplace to consider and base one’s opinion based on information consumed on the
internet. With an increase in social media platforms, there is an overwhelming amount of information
reaching people everyday and it is of great interest to marketing companies, data scientists, content
creators, linguists and researchers to understand the type of information that is drawing people’s attention
and sparking discussions on social media.
In this study, the focus was on an online discussion forum(Reddit). In this study, we analyze the
following problem:
### Can we identify the subject of a subreddit from its most common words? 
This study offers a systematic analysis of top 10 reddit posts with a large number of comments(ranging from around 900 to 9
comments) in the chosen four subreddits(r/worldnews, r/news, r/books, r/movies). To accomplish this task,
sample comments from four subreddit(r/worldnews, r/news, r/books, r/movies) were considered. Large
sample of posts and comments were used which were subjected to pre-processing steps, tokenization,
finding common words, lexical diversity and building tagged corporas using Part Of Speech(POS) tags. In
addition, the study also attempts to identify the subject of the subreddit with the help of common words and
a frequency distribution plot.
This study also aims to understand the impact of lexical diversity on the content structure; the
content’s readability and clarity which further impacts user engagement with the subreddit.
### Method
To identify the subject of the subreddit used with the help of the most common words used, build
tagged corporas and to find the lexical diversity, the following tasks were performed:
#### Scrapping Reddit:
To collect a representative sample of posts, the PRAW library was used and obtained a Read-Only
Reddit instance by collecting the Client ID, Client Secret and User Agent information. PRAW is a Python
Reddit API wrapper(PRAW 7.7.0 Documentation). For this study, four topic-specific
subreddits(r/worldnews, r/news, r/books, r/movies) were chosen and the top 10 posts with their comments
were collected and saved in a .txt file. The subreddit r/worldnews was chosen
#### Reading the .txt file tokenization
The text downloaded in .txt format was read with the help of load_txt() function and the data was
tokenized with word_tokenize() function. A list of tokenized words were obtained.
#### Data cleaning
A systematic data cleaning process was followed to remove stopwords, punctuations, special
characters and to convert the tokens to lowercase using stopwords(), isalnum() were used and to obtain the
stem words, PorterStemmer() function was used.
#### Frequency Analysis
Frequency analysis was carried out to capture the most common words used in the chosen subreddit
and a frequency distribution graph was plotted to get a visual representation. Based on the most common
words, the study attempted to manually identify whether these words aid in correctly identifying the
subreddit used. The accuracy of identification was evaluated by comparing it with the meta-data of the
subreddit.
#### Lexical Diversity and POS tagging
The lexical diversity was calculated for the chosen subreddits using the type-token ratio and the
values for processed tokens and un-processed tokens were obtained. Tagged corporas were built to
understand the parts of speech.
## Results
This section answers the research question that I set out to address in the study.
In this study, I analyzed the subreddits r/worldnews, r/news, r/books and r/movies, performed word
frequency analysis to find the most common words in the obtained data sets and compared it with the meta
information of the chosen subreddit to validate if the common words help identify the subreddit used. In
conjunction with this, the lexical diversity of the chosen subreddit was obtained and a tagged corpora for
the text was also studied. The results are succinctly summarized below:

### Identifying Common words:
The most common words used in the subreddits are:

| Subreddits  | Most Common Words                                                                 |
|-------------|-----------------------------------------------------------------------------------|
| r/worldnews | ('putin', 114), ('http', 108), ('trump', 91), ('like', 90), ('peopl', 89), ('russia', 84), ('world', 71), ('russian', 69), ('one', 67), ('would', 63) |
| r/news      | ('one', 87), ('like', 85), ('go', 77), ('peopl', 65), ('fuck', 64), ('http', 62), ('time', 59), ('would', 59), ('year', 58), ('rip', 58) |
| r/books     | ('book', 255), ('read', 232), ('like', 183), ('get', 167), ('peopl', 162), ('make', 119), ('would', 104), ('net', 103), ('kid', 101), ('neutral', 99) |
| r/movies    | ('senat', 420), ('power', 145), ('unlimit', 133), ('movi', 83), ('post', 82), ('like', 82), ('one', 70), ('time', 65), ('cancer', 65), ('get', 62) |

On analyzing the common words and comparing it with the chosen subreddit meta data, it can be inferred 
that the common words such as ‘putin’, ‘trump’, ‘russia’, ‘world’ help in identifying the subreddit as
r/worldnews. Similarly, words such as ‘book’ and ‘read’ help identify the r/books subreddit, words like
‘peopl’, ‘rip’ help identify r/news and words like ‘movi’, ‘post’ and ‘time’ help identify r/movies subreddit.
However, r/news and r/movies subreddit’s common words appear to be quite vague and makes it difficult
to identify the correct subject of the subreddit by manually comparing them with the respective subreddit
meta information. So, there is a need for multiple methodological approaches to accurately identify the
subject of the subreddits in the case of r/news and r/books.
The frequency distribution plot for the processed and unprocessed tokens are as below:


### Content Structure - Lexical Diversity and Tagged Corporas:
The content structure was analyzed with a POS tagger. In addition the readability and clarity of the
data was analyzed with the help of Lexical Diversity scores(type-token ratio). The Lexical Diversity Score
is as follows:

| Subreddit   | Lexical Diversity (in %) |
|-------------|--------------------------|
| r/worldnews | 33.5                     |
| r/news      | 33.45                    |
| r/books     | 25.92                    |
| r/movies    | 31.6                     |

It was observed that the r/worldnews has the highest lexical diversity and r/books has the lowest lexical
diversity score amongst the other four subreddits.
It can be inferred that, due to low lexical diversity score the language used is mostly colloquial and
significantly impacts the content structure hence impact the user engagement in the case of r/books
subreddit.

## Discussion
The study attempts to analyze the most common words and check whether they can be used to
identify the subject of the subreddit and also to analyze the lexical diversity and tagged corpora to analyze
the content structure for readability and clarity. Not much research publication or articles or journals are
published in this context. But, there are research papers that compare the language usage in multiple
subreddits and study its impact on content structure.
With over 138,000 active subject communities known as "subreddits," Reddit has grown to be one
of the most well-known social media sites on the internet with 52 million daily active members(Marotti,
2018). By enabling users to publish news, queries, and other material in the form of text, photographs, and
links to other websites, Reddit aspires to be the front page of the internet(Horne et al., 2017). Users
frequently interact with the posts by participating in or reading discussions that are made up of comments
left by other members of the community. Horne et al., in their research also state that reddit's discussions
are a crucial and useful feature(2017). Politics is generally one of the most talked about subjects on the site,
and numerous subreddits devoted to American politics frequently rank among the most popular
communities there. With millions of subscribers on Reddit and other online platforms, these communities
have a huge reach.
Reddit, which is structured around its communities known as subreddits, has unquestionably
developed its own standards and culture(Horne et al., 2017). Topic, audience, moderation, and style are
four particular areas in which subreddits differ from one another(Horne et al., 2017). Reddit groups have
been described as functioning as communities by researchers (Bergstrom, 2011; Panek et al., 2018),
although this is not to say that they are always stable. The initial subreddit and its community may
disappear due to inactivity if members have a cause to go to another subreddit and completely abandon the
first one(Jones et al., 2021). Jones et al., states that on Reddit, community building is user-driven rather
than enforced by hierarchical organizational structures(2021).
In alignment with my study, Adamov et. al. 's work states that, one of the most significant subfields
in computational linguistics and natural language processing (NLP) is word frequency distribution (WFD).
The size and caliber of the corpora have a significant impact on the reliability and quality of WFD
results(2015).
According to Horne et al., some subreddits (like r/AskHistorians or r/Bitcoin) are subject-specific,
but others (like r/AskReddit) are generic in nature(2017). Whether a subreddit targets a niche audience or
not can vary, as in the instance of r/Bitcoin, which caters to experts in this field(Horne et al., 2017). On
some subreddits, such as r/todayilearned, which prioritizes submissions that are verifiable facts, there is a
very precise way to post questions and comments(Horne et al., 2017). While there are guidelines for what
kinds of content are acceptable in each subreddit, the precision of the guidelines and the degree of
moderation vary widely amongst subreddits(Horne et al., 2017). Although Horne et al. 's work mainly
focuses on language’s impact on reddit discussions, their study on content structure such as readability and
clarity is judged based on POS tagger and type-text ratio is quite similar to the analysis this study aims to
analyze.
The piece by Jaech et al. that most closely relates to our work examines how language affects reddit
debates where the authors employ an SVM ranking algorithm to order comment threads in 6 different
subreddits utilizing a collection of several intricate natural language parameters(2015).

## Conclusion:
To conclude, it is possible to identify the subject of various subreddits with the aid of word
frequency analysis and manually comparing it with the respective subreddit’s meta information. Although
identifying the subject of various reddits were possible with the help of word frequency analysis, working
with Reddit data, though, could be challenging. The variety of media formats on Reddit may need
academics to apply several methodological approaches in their analysis(Proferes et al., 2021). And the
lexical diversity score analysis of various subreddits suggest that the vocabulary usage in subreddit r/books
was more colloquial than that of the other subreddits which implies that it might affect the content clarity
and reliability affecting user engagement with the subreddit.

## References
 - Adamov, A. (2015). Text analysis case study: Determining word Frequency based on Azerbaijan top 500 websites. Advanced Industrial Conference on Telecommunications.
  - "https://doi.org/10.1109/icaict.2015.7338521"
Bergstrom, K., & Poor, N. (2022). Signaling the Intent to Change Online Communities: A Case From a
Reddit Gaming Community. Social Media and Society, 8(2), 205630512210968.
https://doi.org/10.1177/20563051221096817
Bergstrom, K. (2019). Moving beyond churn: Barriers and constraints to playing a social network game.
Games and Culture, 14(2), 170–189. https://doi.org/10.1177/1555412018791697
Horne, B. D., Adali, S., & Sikdar, S. (2017). Identifying the social signals that drive online discussions: A
case study of Reddit communities. ArXiv (Cornell University).
https://doi.org/10.48550/arxiv.1705.02673
A. Jaech, V. Zayats, H. Fang, M. Ostendorf, and H. Hajishirzi, “Talking to the crowd: What do people react
