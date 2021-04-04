# NLP Tools

A collection of tools, tips and tricks to conduct common NLP tasks. Some of this is just me figuring out different package's syntax, and putting it some where to reference next time I want to do an NLP task.

## Goals
- Scalable NER
- Training pipeline for SpaCy models, to extend NER
- Dependency Parsing for Information Extraction
    - End goal would be to build/extend a Knowledge Graph from semi- or unstructured data
    - "Hearst Patterns" are a good thing to look up to understand this.
- Interoperability with a Semantic Annotation Platform (Doccano, Label Studio, Explosion's Prodigy, etc)
    - Doccano specifically can import/export from a JSON-like format, which you could use for SpaCy training.

## Limitations/Scoping
- I have no intention to build this into a python library. This is just a repo of reference syntax to apply later.

Common packages you'd want to run these:
- **Pandas**
    - Famous Excel/CSV reader for "small data"
- **SpaCy**
    - For Named Entity Recognition (NER), and also Part of Speech tagging. 
    - Offers string similarity checking based on Cosine similarity. This is often the "wrong" answer. To the uninitiated, it'll appear to provide unpredictable answers because it's measure of the word vectors, not the actual levenshtein (edit) distance. On short text it should be able to figure out if two sentences have a similar **meaning**, but it will lose accuracy the larger the body of text. 
    - It's more of a swiss army knife than I'm letting on, but the NER is quick and painless
    - You'll need to download **models** for this to work; check the docs for additional info
- **NLTK**
    - Similar to SpaCy, but a little older. 
    - In SpaCy **tokens** are SpaCy objects, whereas NLTK returns strings. Depending on your use case, it might be a good idea to blend NLTK and SpaCy to get your text processed.
    - You'll need to download **corpora** for this to work; check the docs for additional info
- **GenSim** 
    - For LDA/topic modeling)
- **Huggingface's Transformers** 
    - Allows you to run BERT and GPT-2, the "Heavy duty", State of the Art NLP models)
- **Huggingface's NeuralCoRef** 
    - Allows you to swap indeterminite pronouns to the actual actor (like "When Obama said **he** would do X..." would change **he** to **Obama**)
    - Only works with Spacy 2.x, not 2021's new Spacy 3.0+
- **Boilerpy3**
    - Allows you to download clean article text from a link.
    - Parsing XML sucks, let this do the heavy lifting
- **FuzzyWuzzy or RapidFuzz**
    - Allows you to check string similarity based on levenshtein (edit) distance
    - RapidFuzz is way faster, but may require C++ prereqs


More to come!
