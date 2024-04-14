# Understanding Embeddings with OpenAI and Google Gemini Models

This Jupyter notebook demonstrates how to generate and utilize embeddings using OpenAI and Google Gemini models for various natural language processing tasks. Embeddings are a way to represent text in a dense vector space, capturing the semantic meaning and context of the words. This notebook covers the following topics:

- Generating embeddings using the OpenAI model
- Querying text and calculating similarity with a corpus
- Computing cosine similarity for product descriptions and retrieving the most similar products
- Visualizing the similarity of embeddings using dimensionality reduction and clustering techniques

## Table of Contents

- [Installation](#installation)
- [Generating Embeddings](#generating-embeddings)
- [Querying Text and Similarity](#querying-text-and-similarity)
- [Product Search using Embeddings](#product-search-using-embeddings)
- [Visualization of Similarity](#visualization-of-similarity)

## Installation

Before running the code in this notebook, ensure that you have the following libraries installed:

- `openai`: Install using `pip install openai`
- `dotenv`: Install using `pip install python-dotenv`
- `scipy`: Install using `pip install scipy`
- `scikit-learn`: Install using `pip install scikit-learn`
- `matplotlib`: Install using `pip install matplotlib`

Additionally, make sure you have a valid OpenAI API key and store it in a `.env` file in the same directory as the notebook.

## Generating Embeddings

The notebook demonstrates how to generate embeddings using the OpenAI `text-embedding-3-small` model. It shows how to create a client, specify the model, and generate embeddings for a given text.

The `create_embeddings_from_text` function is defined to simplify the process of generating embeddings for any input text using the specified model.

## Querying Text and Similarity

The notebook illustrates how to calculate the similarity between different text snippets using the generated embeddings. It provides examples of creating embeddings for multiple text samples and computing the cosine distance between them to determine their similarity.

The `scipy.spatial.distance` module is used to calculate the cosine distance between embeddings, which serves as a measure of similarity between the corresponding text snippets.

## Product Search using Embeddings

The notebook demonstrates how to utilize embeddings for product search functionality. It shows how to generate embeddings for a catalog of products and a user query, and then find the most similar products based on the cosine distance between their embeddings.

A sample product catalog is provided, and the `create_product_info_text` function is defined to extract relevant information from each product. Embeddings are generated for the product catalog and the user query, and the top 3 most similar products are retrieved based on the cosine distance.

## Visualization of Similarity

The notebook showcases how to visualize the similarity of embeddings using dimensionality reduction and clustering techniques. It employs Principal Component Analysis (PCA) to project the high-dimensional embeddings onto a 2D plane for visualization purposes.

The `sklearn.decomposition.PCA` class is used for dimensionality reduction, and the `sklearn.cluster.KMeans` class is used for clustering the reduced embeddings. The resulting clusters are visualized using a scatter plot, with each point representing a product and colored according to its cluster assignment.

The notebook also demonstrates how to annotate the plot with product titles to provide more context and interpretability.

## Conclusion

This Jupyter notebook provides a comprehensive overview of generating and utilizing embeddings for various natural language processing tasks. It covers generating embeddings using the OpenAI model, querying text similarity, performing product search, and visualizing the similarity of embeddings.

By following the examples and explanations provided in the notebook, you can gain a better understanding of how embeddings work and how they can be applied to real-world scenarios. Feel free to explore and modify the code to suit your specific requirements and datasets.
