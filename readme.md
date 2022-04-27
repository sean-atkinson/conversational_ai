# Chatbots and Conversational AI

# Table of Contents
<a id='table_of_contents'></a><br>
[Executive Summary](#section_1)<br>
[Challenge](#section_2)<br>
[The Data](#section_3)<br>
[Models and Conclusion](#section_4)<br>
[Datasets, libraries, and additional tools used](#section_5)<br>

<a id='section_1'></a>
# Executive Summary
I have spent the majority of my adult life working in sales in some capacity. 

I have worked in retail sales, corporate sales, and, most recently, in online sales as a copywriter and digital marketer.

While each aspect of sales has its positives and negatives, a common feature amongst all of them is burnout. 

Granted, attrition is a fact of life in all industries, but it's especially worrying in sales. The *Harvard Business Review* estimates that <a href="https://hbr.org/2017/07/how-to-predict-turnover-on-your-sales-team#:~:text=Companies%20worry%20about%20employee%20attrition,is%20less%20than%20two%20years.">the annual turnover of U.S. salespeople is as high as 27%, twice the rate in the overall labor force, with the average tenure being less than two years</a>.

Many would like you to <a href="https://www.forbes.com/sites/serenitygibbons/2020/12/08/sales-teams-are-experiencing-a-burnout-epidemic---heres-how-to-prioritize-your-teams-tasks/?sh=73b897444f92">believe</a> that this is a recent phenomenon, the truth is <a href="https://www.jstor.org/stable/40472147">it's not</a>. <a href="https://www.deepdyve.com/lp/springer-journals/the-role-of-emotional-exhaustion-in-sales-force-attitude-and-behavior-2z0VEwPHl0?key=sage">No, really, it isn't.</a> 

You can find <a href="https://blog.hubspot.com/sales/spot-burnout-salespeople">a whole host of ideas and suggestions</a> online as to how companies can tackle this challenge, but, seemingly without fail, every single one of them misses what in my experience has been the most obvious and best solution to motivating salespeople and preventing burnout: giving them better leads.

Sales, with its constant rejection, is a profession that is bruising on the ego.

As rejections pile up, salespeople become less passionate about their jobs.

If you give them higher quality leads, they will experience fewer rejections.

What's more, better leads mean more money for sales reps (which creates even happier salespeople) and helps a company's bottom line. 

Okay, so but how do you give them better leads?

You do that through lead nurturing, the process of engaging prospective customers by providing them with appropriate content and information at each stage of the sales funnel with the end goal of earning their business. 

And this is where Conversational AI aka chatbots come into play.

Currently there is a range of lead nurturing strategies companies employ:
- Email marketing/nurturing
- Retargeting
- Personalization
- Face-to-face interaction
- Content marketing

And while these strategies have borne some fruit, the fact of the matter is there is still a lot of potential business left on the table.

Consequently, <a href="https://contingencies.org/how-persuasive-chatbots-might-be-used-in-insurance/">"companies are starting to implement chatbots as a customer engagement channel, thus reflecting a potential shift in the way companies interact with their customers, exchange data, and provide services."</a>

Unfortunately, due to the rigid nature and adherence to very strict if-this-then-that rules of most chatbots, the chatbots that companies currently deploy haven't been greeted with open arms by the masses.

<a id='section_2'></a>
# Challenge
[(Back to table of contents)](#table_of_contents)<br>
Can I use my knowdlegde of data science to create a chatbot capable of open and dynamic conversation?

<a id='section_3'></a>
# The data
[(Back to table of contents)](#table_of_contents)<br>
Initially, I had hoped to use the <a href="https://www.kaggle.com/Cornell-University/movie-dialog-corpus">Cornell Movie-Dialogs Corpus</a> as my dataset, but after initial disappointing results I pivoted to a [topical chat dataset](https://www.kaggle.com/arnavsharmaas/chatbot-dataset-topical-chat) from Amazon that consists of 8,000+ conversations and 184,000+ messages.

It was created by Arnav Sharma and is a more streamlined version of [this](https://github.com/alexa/Topical-Chat) original Amazon Alexa dataset.

The dataset contains a conversation id, a message (which is either a reply or the start of a conversation), and the sentiment of each message.

The dataset spans 8 broad topics and is made up of conversations between two people who don’t have defined roles (ex. interviewer and interviewee).  It was created with the goal of [aiding in the effort to build a socialbot that can have deep, engaging open-domain conversations with humans](https://m.media-amazon.com/images/G/01/amazon.jobs/3079_Paper._CB1565131710_.pdf).

The eight broad topics are as follows:
- fashion
- politics
- books
- sports
- general entertainment
- music
- science and technology
- movies


<a id='section_4'></a>
# Models and conclusions
[(Back to table of contents)](#table_of_contents)<br>
Since my goal was open and dynamic conversation, I focused on using attention-based models for the creation of my chatbot.

Due to the time constraints, I limited the dataset I used to the first 50,000 entries and dedicated the majority of my time to fine-tuning GPT-2 models. 

My best small GPT-2 model had a final perplexity of 1.1191, while my medium model had a final perplexity of 1.0628.

Though very happy with the scores my models were able to achieve, limiting my dataset to 50,000 entries led to suboptimal performance on certain subjects, simply because they weren't trained on them. Time constraints made it difficult to train them more extensively, but I very much look forward to doing much more in-depth training in the future.

Nonetheless, what I have seen so far excites me for the potential Conversational AI has for lead nurturing, online shopping experiences, interactive brand messaging, and, not to be forgotten, the sanity of salespeople everywhere.

If you are interested in interacting with my chatbots, you can do so here:

- <a href="https://huggingface.co/satkinson/DialoGPT-small-marvin">GPT-2 Chatbot (small version)</a>

- <a href="https://huggingface.co/satkinson/DialoGPT-medium-marvin">GPT-2 Chatbot (medium version)</a>

<a id='section_5'></a>
# Datasets, libraries, and additional tools used
[(Back to table of contents)](#table_of_contents)<br>

<b>Datasets:</b>
- <a href="https://www.kaggle.com/Cornell-University/movie-dialog-corpus">Cornell Movie-Dialogs Corpus</a>
- <a href="https://www.kaggle.com/arnavsharmaas/chatbot-dataset-topical-chat">Chatbot Dataset Topical Chat</a>

<b>Libraries:</b> gensim, glob, logging, matplotlib, nltk, numpy, os, pandas, pickle, pyLDAvis, pytorch, random, re, seaborn, shutil, sklearn, spacy, sys, tensorflow, textblob, time, tqdm.notebook, transformers, typing, and wordcloud.

<b>Additional tools:</b> Google Colab and Hugging Face.
