# Chroma Demo 

This demo is focused around *evaluation* and *automated analysis* of embeddings. 

Originally prepared for SF Tech Week hosted by Bloomberg Beta.

A common problem of working with embeddings is figuring out: 
- What embedding model should I use?
- Where do I know things and where do I not know things?

For this, we are going to look at simple approaches to model both of these! 

We are going to use the Biden's State of the Union Address as our Document. 

## Install

1. `pip install -r requirements.txt`
2.  Drop in your OpenAI API Keys to make the notebooks run.

## Guide to repo

1. `load.ipynb` - chunks up `sota.txt`, embeds it and loads it into Chroma
2. `generate_questions.ipynb` - generates synethetic question for each document chunk by asking GPT to write one, saves to `questions.pickle`
3. `use_questions.ipynb` - does the fun plotting, clustering, summarization

The default path is to use OpenAI embeddings, but I also ran an experiment with `sentence-transformers` and you can see the result of that in `use_questions_st.ipynb`

## License

MIT