# Friends TV Show Script Analysis using Word2Vec

## Overview
This project uses Word2Vec to analyze scripts from the *Friends* TV show. By training a Word2Vec model on the dialogues, we can find relationships between words, visualize word distributions, and understand contextual similarities between characters and phrases.

## Dataset
The dataset consists of script dialogues from multiple seasons of *Friends*, preprocessed for training the Word2Vec model.

## Methodology
1. **Preprocessing the Data**  
   - Tokenization of sentences  
   - Removing punctuation and stopwords  
   - Converting text to lowercase  

2. **Training the Word2Vec Model**  
   - Using the `gensim` library to train a Word2Vec model  
   - Choosing between Skip-gram or CBOW architecture  
   - Configuring vector size, window size, and minimum word count  

3. **Performing Analysis**  
   - Finding similar words  
   - Visualizing word embeddings using PCA/t-SNE  
   - Exploring relationships between words  

## Installation & Dependencies
Ensure you have Python installed, then install the required dependencies:

```sh
pip install gensim nltk matplotlib sklearn
```

## Usage
Run the Jupyter Notebook to train the Word2Vec model and analyze word relationships:

```sh
jupyter notebook Friends_TV_Show_Script_Word2Vec.ipynb
```

## Example Outputs
- **Finding similar words**:
  ```python
  model.wv.most_similar('joey')
  ```
  Example Output:
  ```
  [('chandler', 0.85), ('ross', 0.82), ('monica', 0.80), ...]
  ```

- **Visualizing embeddings**:
  ```python
  from sklearn.decomposition import PCA
  import matplotlib.pyplot as plt
  ```
  *(Full visualization code available in the notebook.)*  

## Results
- Word embeddings reveal character relationships and frequently used words.  
- The model can be extended for NLP applications like chatbots or text prediction.  

## Future Enhancements
- Train on a larger dataset for better accuracy.  
- Experiment with different hyperparameters for improved embeddings.  
- Extend embeddings for text generation tasks.  

## Contributing
Feel free to fork and contribute to this project! 🚀  

## License
This project is for educational purposes only.
