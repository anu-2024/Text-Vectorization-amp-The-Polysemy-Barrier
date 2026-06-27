LAB Assignment 1 Total Marks - 25
Generative AI

Text Vectorization &amp; The Polysemy Barrier

Core Objective
To programmatically demonstrate the foundational limits of Bag-of-Words / Static Count
Vectors when processing human language. You will use pandas and scikit-learn to filter a
real-world Kaggle dataset and prove mathematically why static representations fail to
capture context when a word changes meaning (polysemy). This directly establishes the
technical necessity for the Self-Attention Mechanisms used in modern Generative AI
models.

Assigned Dataset
 Dataset : https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews
 File to use : Reviews.csv

Step-by-Step Lab Workflow
Step 1: GitHub &amp; Environment Setup
 Create a public GitHub repository named [Name]-gen ai-foundations.
 Clone the repository to your local machine.
 Download Reviews.csv from the Kaggle link and place it inside your project folder.
 Create a Jupyter Notebook named nlp_vector_lab.ipynb and a markdown file named
answers.md.
Step 2: The Coding Challenge
Open nlp_vector_lab.ipynb. You must write a Python script from scratch that implements
the following technical specifications. Do not hardcode vectors; use library methods.
��️ Technical Specifications:
1. Data Ingestion: Load the first 50,000 rows of Reviews.csv using pandas.
2. Text Selection: Create a list containing exactly three specific text strings where the
word &quot;light&quot; is used in different contexts:
o Sentence 1: A review where &quot;light&quot; means low-calorie, weight, or texture
(e.g., &quot;This olive oil is wonderful and very light on the stomach.&quot;).
o Sentence 2: A review where &quot;light&quot; means illumination or physical visibility
(e.g., &quot;The packaging was broken and let too much light inside the box.&quot;).
o Sentence 3: Another review where &quot;light&quot; matches the low-calorie or weight
context of Sentence 1 (e.g., &quot;I prefer this brand because it is a light and
healthy snack.&quot;).

3. Vectorization Engine: Import and initialize a standard word-counting text vectorizer
from scikit-learn. Transform your list of 3 sentences into a document-term matrix,
and explicitly convert that matrix into a standard dense NumPy array.
4. Vector Slicing: Extract the individual raw row vectors for each of the three sentences
from your dense matrix. Assign them to distinct variables: vec_1, vec_2, and vec_3.
5. Similarity Mathematics: Calculate the mathematical similarity between Sentence 1
and Sentence 2 (Different Contexts).

LAB Assignment 1 Total Marks - 25
Generative AI

o Calculate the mathematical similarity between Sentence 1 and Sentence 3
(Similar Contexts).
o Constraint: You must use the linear algebra Dot Product function from the
numpy library to compute these scores.

6. Console Output: Print both calculated similarity scores clearly to the console.

Step 3: Theory &amp; Reflection Questions
Open answers.md and provide a 3-to-4 sentence analytical response for each question:
Question 1: The Vector Conflict
Review your printed dot product similarity scores. Did your code show a significantly high
similarity score between the two contextually different uses of the word &quot;light&quot;? Explain
why a basic frequency-counting vectorizer calculates a false mathematical relationship here.
Question 2: The Context Blindspot
From a Data Science perspective, explain why this bag-of-words approach creates a massive
bottleneck for building search engines or chatbots. What linguistic property is completely
lost when text is turned into static counts?
Question 3: The GenAI Architectural Fix
How do modern Large Language Models (like GPT or LLaMA) solve this exact problem?
Mention how Masked Self-Attention and Context-Aware Embeddings work together to
ensure the word &quot;light&quot; gets completely different mathematical vectors in those three
sentences.

Step 4: Git Submission Workflow
Open your terminal inside your project directory and run these commands to deploy your
work to GitHub:
Bash
git init
git remote add origin &lt;YOUR_GITHUB_REPOSITORY_URL&gt;
git add .
git commit -m &quot;MCA Lab: Completed Amazon Review vector analysis and reflection&quot;
git branch -M main
git push -u origin main

Submit your Github link to the excel file shared with it.
