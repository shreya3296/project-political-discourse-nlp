
# **Deciphering Democratic Discourse: A Deep Dive into India's Political Landscape through Parliamentary Questions, Speeches, and Tweets**

This repository contains the project deliverables, analysis, and results for our research project, **Deciphering Democratic Discourse**, which explores political communication and sentiment in India. The project offers insights into the tone, themes, and sentiment across various political communication mediums, including parliamentary questions, speeches by Prime Minister Narendra Modi, and tweets from key political parties.

### **Project Overview**
India's political discourse is rich and multifaceted, involving formal parliamentary questions as well as public communications through speeches and social media. This project aimed to analyze:
- **Thematic trends and sentiments** in parliamentary questions over two decades (1999-2019).
- **Public communications**, such as Prime Minister Modi's speeches (2014-2020) and political parties' tweets.
- **Comparisons** of discourse in Parliament with public sentiment in speeches and tweets.

### **Data Sources**
1. **Parliamentary Questions Data Portal**: Includes parliamentary questions raised in the Lok Sabha (Lower House of Parliament) from 1999 to 2019. Each question contains detailed metadata such as the ministry it pertains to, members of parliament involved, and the specific issue discussed.
2. **Prime Minister Narendra Modi’s Speeches**: A comprehensive collection of speeches from 2014 to 2020, reflecting on policy, development, and governance themes.
3. **Indian Political Parties Tweets Dataset**: Daily updated tweets from the Bharatiya Janata Party (BJP), Congress (INC), and Aam Aadmi Party (AAP) from 2014 to 2020, capturing real-time public engagement and sentiments.

### **Methodology**
Our project combines **Exploratory Data Analysis (EDA)** and **advanced machine learning techniques** to examine political discourse across parliamentary questions, speeches, and tweets. We employed multiple approaches to explore patterns, classify political content, and predict sentiment. The key methodologies include:

- **Exploratory Data Analysis (EDA)**:
    - We conducted a **trend analysis** on parliamentary questions over time to detect shifts in focus across different periods. The data was broken down by ministry, party affiliations, and key policy topics.
    - A **keyword analysis** was performed on the text corpus to identify frequently recurring terms in each medium. We also used term-frequency inverse document frequency (TF-IDF) to understand the importance of specific terms.
    - **Outlier analysis** was performed to detect extreme values, particularly for certain years where the number of questions, topics, or mentions of certain issues spiked dramatically.
  
- **Thematic Modeling**:
    - **Latent Dirichlet Allocation (LDA)** was used to extract themes from the parliamentary questions dataset. The model helped uncover hidden topics such as healthcare, infrastructure, education, and defense, and their evolution over time.
    - **Topic coherence scores** were used to assess the quality of the topics generated, ensuring that each topic was distinct and meaningful.
    - We applied **BERT embeddings** to capture the semantic meaning of the text across the tweets and speeches, ensuring a deep understanding of the context behind political discourse.

- **Sentiment Analysis**:
    - We used **TextBlob** for a basic sentiment polarity analysis to classify each entry into positive, negative, or neutral sentiment categories. This helped identify whether public discourse (tweets and speeches) is generally optimistic, pessimistic, or neutral.
    - We extended this by using **BERT-based sentiment classification** to refine the sentiment categorization, offering a more nuanced and context-aware analysis, particularly for politically charged texts such as parliamentary debates.
  
- **Classification Models**:
    - **BERT (Bidirectional Encoder Representations from Transformers)** was used to classify tweets and parliamentary questions as being either affiliated with BJP or not. The model was fine-tuned to ensure high accuracy, and it achieved around 73% accuracy in classifying political content.
    - **Prime Minister Modi's speeches** were similarly classified, providing insights into how closely aligned his public communications are with his party's broader strategy.
    - The models were trained using **cross-validation** to ensure robustness and prevent overfitting. **Grid search** was used for hyperparameter tuning, and **class weighting** was applied to address any imbalance in the datasets.

- **Time-Series Analysis**:
    - We performed a **temporal analysis** of speech and tweet trends to assess how political messaging changes during key events, such as elections, policy launches, and national crises.
    - This approach also allowed us to study the interplay between major events, such as the COVID-19 pandemic or demonetization, and political discourse, highlighting shifts in public communication strategies during times of crisis.
  
- **Visualization**:
    - We visualized the distribution of topics and sentiment over time, creating **word clouds**, **bar charts**, and **line graphs** to display trends. Interactive dashboards were built to allow deeper exploration of the data.
    - **Feature importance plots** from tree-based models such as Random Forest were used to enhance the interpretability of the classification results, allowing us to understand which features (terms, keywords, ministries, etc.) were most influential in predicting party affiliation.

### **Key Findings**
- **Thematic Analysis**: Parliamentary questions were dominated by domestic concerns such as healthcare, education, and infrastructure, but global issues such as defense and trade have seen a rise in recent years.
- **Sentiment**: Prime Minister Modi’s speeches consistently carried a positive sentiment, often focusing on national pride and development, while tweets from political parties varied greatly, reflecting the more confrontational and reactive nature of social media.
- **Party Classification**: Using BERT, we successfully classified tweets and parliamentary questions, showing that BJP’s public communication is strategically aligned with its parliamentary discourse, particularly on topics like nationalism and development.
