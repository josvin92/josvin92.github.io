## Welcome to CS525 - Final Project Website

![Image](img/corona.png)  

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
1. BERT
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



## ***Our Approaches***
Approach 1: Using spaCy for tokenization, Lemmatization and Removing stopwords and using scikit-learn to build our models for different batches of data and using Ensemble Techniques to create an aggregate prediction result.

Approach 2: Using NLTK for tokenization, Lemmatization and Removing Stop words and using scikit-learn to build our models for different batches of data.

Approach 3: Using Keras for performing Topic Modeling using LDA.

Approach 4: BERT.

### Doc2vec Model
The Doc2vec model is a unsupervised model which transfers docs into vectors, and docs have similar meaning will close to each other in the vector space.

We assume the description of tasks and the possible answers of that will close to each other in the vectpr space.
So, firstly, we train the model with the 4300 articles, and use the descriptions of tasks to test the model - the model will transfer descriptions into vector, then we find out the most similar articles in the vector space.

For instance:

**Task1:**  What is known about transmission, incubation, and environmental stability?

- [Environmental Engineers and Scientists Have Important Roles to Play in Stemming Outbreaks and Pandemics Caused by Enveloped Viruses](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7099656/)

- [Journal Pre-proof Transmission of COVID-19 in the terminal stage of incubation period](https://doi.org/10.1016/j.ijid.2020.03.027)

**Task2:** What do we know about COVID-19 risk factors?

- [Association between 2019-nCoV transmission and N95 respirator use](https://doi.org/10.1101/2020.02.18.20021881)

**Task3:** What do we know about virus genetics, origin, and evolution?

- [Journal Pre-proof Bat influenza viruses: Making a double agent of MHC class II Bat influenza viruses](https://doi.org/10.1016/j.tim.2020.04.006)

**Task4:** What do we know about vaccines and therapeutics? What has been published concerning research and development and evaluation efforts of vaccines and therapeutics?

- [Research and Development on Therapeutic Agents and Vaccines for COVID-19 and Related Human Coronavirus Diseases](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7094090/)

**Task5:** What do we know about the effectiveness of non-pharmaceutical interventions? What is known about equity and barriers to compliance for non-pharmaceutical interventions?

- [CAN-NPI: A Curated Open Dataset of Canadian Non-Pharmaceutical Interventions in Response to the Global COVID-19 Pandemic](https://doi.org/10.1101/2020.04.17.20068460)

**Task6:** What do we know about diagnostics and surveillance? What has been published concerning systematic, holistic approach to diagnostics

- [Evaluation of antibody testing for SARS-CoV-2 using ELISA and lateral flow immunoassays](https://doi.org/10.1101/2020.04.15.20066407)

**Task7:** What has been published about medical care?

- [Cardiovascular Considerations for Patients, Health Care Workers, and Health Systems During the Coronavirus Disease 2019 (COVID-19) Pandemic](https://doi.org/10.1016/j.jacc.2020.03.031)

**Task8:** What has been published about ethical and social science considerations?

- [Supporting Clinicians During the COVID-19 Pandemic](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7106065/)

**Task9:** What has been published about information sharing and inter-sectoral collaboration?

- [COVID-19: Vulnerability and the power of privilege in a pandemic](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7165578/)

**pro:** doc2vec provides useful articles to answer crucial questions

**cons:** it's a unsupervised model

## ***Our Results***
- What is known about transmission, incubation, and environmental stability?
BERT answer : 
- What do we know about COVID-19 risk factors?
BERT answer : 
- What do we know about virus genetics, origin, and evolution?
BERT answer : .
- What do we know about vaccines and therapeutics?
BERT answer : 
- What has been published about medical care?
BERT answer : 
- What do we know about non-pharmaceutical interventions?
BERT answer : .
- Geographic variations: how the disease will spread and if there are different variations of the virus in different areas?
BERT answer :
- What do we know about diagnostics and surveillance?
BERT answer : 
- What has been published about ethical and social science considerations?
BERT answer : .
- What has been published about information sharing and inter-sectoral collaboration?
BERT answer :


[Link to the repository containing our project files](https://github.com/alicekenway/CS525_finalpj)

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
![Image](https://github.com/josvin92/josvin92.github.io/blob/master/small_coronavirus.png)  

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/josvin92/josvin92.github.io./settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
