# Analyze text with the Language Service

## Text Analytics Techniques

- Statical analysis of terms used
    - removing common "stop words"
    - frequency analysis
- Extending frequency analysis to multi term phrases
- Applying stemming or lemmatization algorithms to normalize the words before counting them
- Applying linguistic structure roles - nouns, verbs, adjectives
- Encoding words or terms as numeric features that can be used to train a model
- Creating vectorized moldes that captures semantic relationship between words by assigning them to locations in an n dimensional space

## Language service
- Determine the language of the document
    - Language detection 
        - language name
        - ISO 6391 language code
        - Score confidence
            - Can be used mixed languagee content
- Perform Sentiment analysis
    - Detecting positive or negative sentiment in social media
    - Pre-built ML classification evaluates the text and returns a sentiment score in the range 0 to 1
    - score 0.5 is undetermined sentiment 
        - can be caused by worng code language
        - not sufficient text to determine the sentiment
- Extract key phrases from text
    - Concept to evaluate the texxt of a document
    - identify the main talking points   
- Identify and categorize entities 
    - entity
        - item of particular type or category
    - support entity link