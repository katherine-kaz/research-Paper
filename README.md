# Comparative Analysis of Transformer-Based Generative AI Models for Automatic News Text Summarization

##  Project Overview

This project presents a comparative evaluation of three pre-trained Transformer-based Generative Artificial Intelligence (GenAI) models for automatic abstractive news text summarization: **T5-Small, FLAN-T5-Small, and BART-Large-CNN**.

The study uses the BBC News Summary Dataset to examine how effectively these models generate concise summaries that resemble human-written reference summaries.
Their performance is evaluated using ROUGE-1, ROUGE-2, ROUGE-L, and BLEU metrics under the same experimental conditions.

##  Objectives

- Compare three pre-trained Transformer-based models for abstractive news summarization.
- Generate summaries from original news articles.
- Evaluate generated summaries against human-written reference summaries.
- Identify the best-performing model using ROUGE and BLEU scores.

##  Dataset

**BBC News Summary Dataset**

- Total dataset: 2,225 news articles with corresponding human-written summaries.
- Categories: Business, Entertainment, Politics, Sport, and Technology.
- Dataset attributes: Category, Article, and Summary.
- Experimental sample: 100 randomly selected article-summary pairs.
- Sampling method: Random sampling with a fixed random seed (`random_state=42`).

The original article is provided as the model input, while the human-written summary is used as the reference for evaluation. The category is retained as dataset metadata.

##  Models Evaluated

| Model | Description |
|---|---|
| T5-Small | Pre-trained text-to-text Transformer model |
| FLAN-T5-Small | Instruction-tuned version of T5 |
| BART-Large-CNN | BART model fine-tuned for CNN/DailyMail news summarization |

The study evaluates existing pre-trained models rather than training a new model from scratch.

##  Tools and Technologies

- Python
- Google Colab
- Hugging Face Transformers
- Pandas
- Natural Language Processing (NLP)
- Transformer-based Generative AI
- ROUGE and BLEU evaluation metrics
- BBC News Summary Dataset

##  Methodology

1. Extract and load the news articles and their corresponding summaries.
2. Combine the dataset into a structured DataFrame.
3. Check missing values, article-summary alignment, and category consistency.
4. Randomly select 100 article-summary pairs for experimentation.
5. Load the three pre-trained Transformer models.
6. Generate abstractive summaries from the original news articles.
7. Compare each generated summary with its human-written reference.
8. Calculate ROUGE-1, ROUGE-2, ROUGE-L, and BLEU scores.
9. Compare the results to identify the best-performing model.

##  Results

The following are the reported evaluation scores from the study.

| Model | ROUGE-1 | ROUGE-2 | ROUGE-L | BLEU |
|---|---:|---:|---:|---:|
| T5-Small | 0.3138 | 0.2079 | 0.2322 | 0.0156 |
| FLAN-T5-Small | 0.2094 | 0.1415 | 0.1771 | 0.0002 |
| BART-Large-CNN | **0.3892** | **0.2638** | **0.2724** | **0.0602** |

**Key finding:** BART-Large-CNN achieved the highest reported score across all four evaluation metrics, followed by T5-Small and FLAN-T5-Small.

These metrics measure similarity between generated summaries and human-written references. They do not, by themselves, establish factual correctness or overall summary quality.

##  My Contribution and Learning Outcomes

- Prepared and sampled the dataset for model evaluation.
- Worked with three pre-trained Transformer-based GenAI models.
- Generated and evaluated summaries of news articles.
- Compared model performance using standard text-generation evaluation metrics.
- Gained practical understanding of NLP, abstractive summarization, pre-trained language models, and comparative model evaluation.
- Interpreted evaluation results to identify differences in summarization performance.

##  Limitations

- Evaluation was limited to 100 randomly sampled article-summary pairs due to computational constraints.
- Results reflect the selected dataset sample and experimental settings.
- ROUGE and BLEU measure textual overlap and do not fully assess factual consistency, readability, or human preference.
- The study compares pre-trained models without developing or training a new architecture.

##  Conclusion

The study found that BART-Large-CNN performed best among the three evaluated models on the selected BBC News Summary Dataset sample, according to ROUGE-1, ROUGE-2, ROUGE-L, and BLEU.
The results demonstrate the value of comparing pre-trained Transformer models under consistent experimental conditions when selecting a model for automatic news summarization.
