## 📋 Problem Statement

### Context
"Car-ing is sharing", a growing car sales and rental company, is looking to optimize its customer service and market intelligence operations. As part of their digital transformation strategy, the Chief Technology Officer (CTO) wants to integrate Large Language Models (LLMs) into a customer-facing chatbot app. To minimize operational risks and choose the right technical approach, the company needs a functional proof-of-concept pipeline to test how well pre-trained models handle diverse natural language tasks.

### Core Challenges & Requirements
The prototype must successfully process customer reviews and unstructured text across four major operational dimensions:

1. **Customer Sentiment Evaluation**  
   The company lacks an automated system to track customer satisfaction. The pipeline must classify the sentiment of car reviews in `car_reviews.csv` and evaluate performance metrics ($Accuracy$ and $F1\text{-}Score$) against ground-truth data to ensure reliability.

2. **Localization & Expansion**  
   With a growing customer base from Spain, the company needs to translate English inquiries into Spanish accurately. The prototype must translate selected review text and use algorithmic evaluation ($BLEU\text{ }score$) against reference data (`reference_translations.txt`) to measure translation quality.

3. **Targeted Insight Extraction**  
   Manual review analysis is inefficient. When specific feedback stands out (such as brand perception), the system must utilize an extractive Question Answering (QA) model (e.g., `deepset/minilm-uncased-squad2`) to pull exact textual answers directly from customer feedback using specific context and questions.

4. **Information Condensation**  
   Long-form customer reviews take too long to read and digest. The pipeline must leverage generative summarization to condense lengthy feedback into highly precise, actionable summaries strictly limited to approximately 50–55 tokens.

### Business Objective
The ultimate goal of this project is to validate the accuracy, feasibility, and token efficiency of these pre-trained LLM pipelines, establishing a robust, data-backed foundation before building out the final production chatbot application.
