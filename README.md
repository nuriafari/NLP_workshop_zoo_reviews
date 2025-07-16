# Workshop – Analysis of Edinburgh Zoo Reviews 🐧 

This project was developed as part of an **introductory workshop** for students with minimal Python experience. It offers a hands-on introduction to **Natural Language Processing (NLP)**, with a focus on **Named Entity Recognition (NER)**, **sentiment analysis**, and real-world data exploration.

Participants explore how to detect animals in text (even with typos), group them by species, analyze how people feel about those animals, and generate natural-language summaries based on real visitor reviews.

## What the workshop contains

This workshop walks through a full NLP pipeline using visitor reviews from Edinburgh Zoo. It’s designed to help beginners explore how we can use large language models to explore and extract information from written text, through the `workshop.ipynb` jupyter notebook.

Specifically, `workshop.ipynb`:
- **Loads and cleans raw review data** from Edinburgh Zoo visitors
- **Splits the text into individual sentences** for easier processing
- **Identifies animal mentions** using a trained Named Entity Recognition (NER) model
- **Normalises the mentions** by:
  - Fixing typos (e.g. `"pinguin"` → `"penguin"`)
  - Lemmatizing (e.g. `"penguins"` → `"penguin"`)
  - Handling partial matches (e.g. `"lion cub"` → `"lion"`)
- **Maps mentions to actual zoo species** using a curated alias dictionary
- **Runs sentiment analysis** on each sentence to detect whether the opinion is positive, negative, or neutral
- **Groups sentences by animal** and combines their associated sentiments
- **Visualizes results**, including:
  - Most talked-about animals
  - How people feel about different animals (positivity/negativity)
- **Summarizes visitor feedback** using a local large language model (LLM), creating a concise description of what people say about each animal

The notebook is structured to be beginner-friendly, with code and explanations provided step by step, and with a few prompts to guide the user to modify the code to explore the dataset themselves. 

## Getting Started

Clone the repo:
 ```bash
git clone https://github.com/<your-username>/sutton_workshop.git
cd sutton_workshop
```

Install dependencies
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
Run the Jupyter notebook:
```bash
jupyter notebook workshop.ipynb
```
