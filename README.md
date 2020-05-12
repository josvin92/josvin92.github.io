## Welcome to CS525 - Final Project Website

# COVID-19 Open Research Dataset Challenge (CORD-19) Analysis

![Image](https://github.com/josvin92/josvin92.github.io/blob/master/cord19_2.jpg)  

## ***Project Overview***
In this project we carry out various Information Retrieval and Machine Learning methods to retrieve articles that are most relevant to the crucial medical questions given to us as tasks.
The Major tasks assigned to us are as follows:
- What is known about transmission, incubation, and environmental stability?
- What do we know about COVID-19 risk factors?
- What do we know about virus genetics, origin, and evolution?
- What do we know about vaccines and therapeutics?
- What has been published about medical care?
- What do we know about non-pharmaceutical interventions?
- Geographic variations: how the disease will spread and if there are different variations of the virus in different areas?
- What do we know about diagnostics and surveillance?
- What has been published about ethical and social science considerations?
- What has been published about information sharing and inter-sectoral collaboration?

We have four different approaches to our project.
1. Word2Vec
2. Doc2Vec
3. LDA
4. TF-IDF

## ***Dataset Description***
COVID-19 Open Research Dataset (CORD-19) has over 47,000 biology and medicine scholarly articles in various language, about 4300 of them are related to COVID-19, SARS-CoV-2, and coronaviruses, in English.
Original dataset contains fields like 
- cord_uid	
- sha	source_x	
- title	
- doi	
- license	
- abstract	
- publish_time	
- authors	
- journal	
- full_text_file	
- url	
- text	

For our purpose, we only extract some fields in the 4300 related articles
Fields includes:
- paper_id
- title
- abstract
- body_text
- url

The original dataset can be downloaded at
[Link](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge)

The dataset we extracted can be downloaded at
[Link](https://drive.google.com/file/d/11gE-qSoao3sjkhXGevGEEWasgecaN0rG/view?usp=sharing)




## ***Our Apporaches***
Approach 1: Using spaCy for tokenization, Lemmatization and Removing stopwords and using scikit-learn to build our models for different batches of data and using Ensemble Techniques to create an aggregate prediction result.

Approach 2: Using NLTK for tokenization, Lemmatization and Removing Stop words and using scikit-learn to build our models for different batches of data.

Approach 3: Using Keras for performing Topic Modeling using LDA.

Approach 4: TF-IDF.

###Doc2vec Model
The Doc2vec model is a unsupervised model which transfers docs into vectors, and docs have similar meaning will close to each other in the vector space. 
We assume the description of tasks and the possible answers of that will close to each other in the vectpr space.
So, firstly, we train the model with the 4300 articles, and use the descriptions of tasks to test the model - the model will transfer descriptions into vector, then we find out the most similar articles in the vector space.

For instance:
Task1:  What is known about transmission, incubation, and environmental stability?
[Environmental Engineers and Scientists Have Important Roles to Play in Stemming Outbreaks and Pandemics Caused by Enveloped Viruses](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7099656/)
[Journal Pre-proof Transmission of COVID-19 in the terminal stage of incubation period](https://doi.org/10.1016/j.ijid.2020.03.027)

Task3: What do we know about virus genetics, origin, and evolution?
[Journal Pre-proof Bat influenza viruses: Making a double agent of MHC class II Bat influenza viruses]
(https://doi.org/10.1016/j.tim.2020.04.006)

pro: doc2vec is accruate for large dataset
cons: it's a unsupervised model




### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/josvin92/josvin92.github.io./settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
