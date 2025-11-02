About Dataset
-------------

AI vs Human Content Detection Dataset Documentation
===================================================

Overview
--------

This synthetic dataset contains text samples labeled for AI vs human content detection, with comprehensive linguistic and stylistic features extracted from each text sample. The dataset is designed for machine learning classification tasks to distinguish between AI-generated and human-written content.

-   Total Features: 17 columns
-   Target Variable: `label` (1 = AI-generated, 0 = Human-written)
-   Dataset Size: Large collection of text samples with varied content types
-   Use Case: Binary classification for AI content detection

Column Specifications
---------------------

| Column Name | Data Type | Description | Sample Values | Notes |
| --- | --- | --- | --- | --- |
| `text_content` | String | The actual text content being analyzed | "Score each cause. Quality throughout...", "Board its rock. Job worker..." | Primary feature - raw text data |
| `content_type` | String | Category/genre of the text content | academic_paper, essay, creative_writing, news_article, blog_post, social_media, article, product_review | Categorical feature with 8 distinct types |
| `word_count` | Integer | Total number of words in the text | 288, 253, 420, 196 | Ranges from small social media posts to longer articles |
| `character_count` | Integer | Total number of characters including spaces | 1927, 1719, 2849, 1310 | Strong correlation with word_count |
| `sentence_count` | Integer | Number of sentences in the text | 54, 45, 75, 34 | Used to calculate average sentence length |
| `lexical_diversity` | Float | Ratio of unique words to total words | 0.9514, 0.9723, 0.9071, 0.9592 | Range 0-1, higher = more diverse vocabulary |
| `avg_sentence_length` | Float | Average number of words per sentence | 5.33, 5.62, 5.6, 5.76 | Calculated as word_count/sentence_count |
| `avg_word_length` | Float | Average character length per word | 5.69, 5.8, 5.79, 5.69 | Indicates vocabulary complexity |
| `punctuation_ratio` | Float | Ratio of punctuation marks to total characters | 0.028, 0.0262, 0.0263, 0.026 | Measures punctuation density |
| `flesch_reading_ease` | Float | Flesch Reading Ease score | 53.08, 50.32, 46.86, 53.8 | Higher scores = easier to read (0-100 scale) |
| `gunning_fog_index` | Float | Gunning Fog readability index | 7.41, 8.1, 7.86, 7.0 | Grade level required to understand text |
| `grammar_errors` | Integer | Number of detected grammar errors | 1, 6, 5, 2 | Count of grammatical mistakes |
| `passive_voice_ratio` | Float | Ratio of passive voice sentences | 0.1041, 0.2045, 0.2308, 0.1912 | Range 0-1, measures passive construction usage |
| `predictability_score` | Float | Measure of text predictability | 105.86, 100.29, 96.88, 88.79 | Higher values indicate more predictable patterns |
| `burstiness` | Float | Measure of sentence length variation | 0.5531, 0.5643, 0.4979, 0.6241 | Higher values = more variation in sentence lengths |
| `sentiment_score` | Float | Sentiment polarity of the text | 0.2034, 0.4854, -0.2369, null | Range typically -1 to +1 (negative to positive) |
| `label` | Integer | Target variable: AI (1) or Human (0) generated | 1, 1, 1, 1 | Binary classification target |

Data Quality Notes
------------------

-   Missing Values: Some entries have null values in `sentiment_score` column
-   Label Distribution: Mix of AI-generated (1) and human-written (0) content
-   Content Variety: Includes diverse text types from academic papers to social media posts
-   Feature Engineering: Multiple derived features from raw text (readability scores, linguistic metrics)

Key Insights for ML Applications
--------------------------------

-   Stylometric Features: Rich set of writing style indicators
-   Readability Metrics: Multiple standardized readability measures
-   Linguistic Complexity: Vocabulary diversity and grammar analysis
-   Content-Type Awareness: Genre classification available for stratified analysis

Potential Use Cases
-------------------

-   AI content detection systems
-   Writing style analysis
-   Educational content assessment
-   Content authenticity verification
-   Automated essay scoring research

Feature Categories
------------------

-   Text Metrics: word_count, character_count, sentence_count
-   Linguistic Features: lexical_diversity, avg_word_length, punctuation_ratio
-   Readability Scores: flesch_reading_ease, gunning_fog_index
-   Style Indicators: passive_voice_ratio, burstiness, grammar_errors
-   Content Analysis: sentiment_score, predictability_score
-   Metadata: content_type, label