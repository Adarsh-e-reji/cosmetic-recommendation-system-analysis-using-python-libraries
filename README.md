# **Cosmetic Recommendation System Analysis using Python libraries**

## **Project Description**

Choosing the right cosmetic product can be difficult, especially for individuals with sensitive skin. In this project, we built a content-based recommendation system that suggests products based on their ingredients. Using a dataset of 1472 cosmetic products from Sephora, we processed ingredient lists and visualized product similarity using machine learning and data visualization techniques.

The project uses word embedding to process ingredients and t-SNE for dimensionality reduction, helping us create an interactive, 2D visualization of similar products. The system assists users in finding products best suited to their needs based on their ingredient preferences.

---
## **Dataset**
The dataset used in this project, **cosmetics.csv**, contains information about cosmetic products. It has been added to the repository, and you can access it by downloading the file directly from the repo. The dataset is used for analyzing and processing product ingredients to create the recommendation system.

## **Technologies Used**

This project uses several Python libraries and technologies:

- **pandas**: for data manipulation and analysis.
- **numpy**: for numerical operations.
- **scikit-learn**: for machine learning algorithms, including t-SNE (dimensionality reduction).
- **bokeh**: for creating interactive data visualizations.
- **Python 3.x**: programming language.

## **Project Tasks**

### **1. Import and Inspect the Dataset**
The first step involves loading the dataset (cosmetics data) into a **pandas DataFrame** for easy inspection. In this task, you will:
- Import necessary libraries like `pandas`, `numpy`, and `TSNE` from `sklearn.manifold`.
- Load the CSV file containing the cosmetics data and preview the first few rows.
- Display the counts of product types to better understand the dataset.

### **2. Filter Data for Specific Product Categories and Skin Types**
After loading the data, the next step is to filter the data:
- Focus on the **Moisturizer** product category.
- Further filter the data for products suitable for **dry skin**.
- Use the `reset_index()` method to reset the DataFrame index after filtering.

### **3. Tokenize Ingredients and Create a Bag of Words**
In this task, we process the ingredient lists to create tokens:
- Convert the ingredients for each product to lowercase.
- Split the ingredient list into individual tokens (ingredients) by using a delimiter like a comma.
- Create a corpus of tokens for all products.
- Build a dictionary (`ingredient_idx`) to map each unique ingredient to an index.

### **4. Create a Document-Term Matrix (DTM)**
Next, a **Document-Term Matrix (DTM)** is created:
- This matrix represents the frequency of each ingredient in each product's ingredient list.
- The number of products in the filtered dataset is stored in variable **M**, and the number of unique ingredients is stored in **N**.
- A matrix of size **MxN** is initialized to store binary values that indicate the presence of ingredients in products.

### **5. Visualize Product Similarity Using t-SNE and Bokeh**
In this task, we apply **Dimensionality Reduction**:
- **t-SNE** (t-distributed Stochastic Neighbor Embedding) is applied to the document-term matrix to reduce its dimensions from N-dimensional space (ingredients) to 2-dimensional space (x, y coordinates).
- Using **Bokeh**, we visualize the products in 2D space to display similarities between products based on their ingredients.

### **6. Adding a Hover Tool in Bokeh**
An interactive **hover tool** is added to the visualization:
- The hover tool allows users to see details like **Product Name**, **Brand**, **Price**, and **Rank** when they hover over each point (product) in the scatter plot.

### **7. Display the Final Plot**
The final plot is displayed using **Bokeh's show() function**, where users can:
- See how the products are clustered based on their ingredient similarities.
- Interact with the plot and explore the relationship between different products.

### **8. Compare Two Products**
To showcase the effectiveness of the recommendation system, we compare two similar products based on their ingredients and visual output. This step prints out the ingredient lists for the two products for comparison.

## **Screenshots**
![Screenshot 2025-01-30 005850](https://github.com/user-attachments/assets/622d5bc7-76c7-4383-87a9-7a094ae174b8)
![Screenshot 2025-01-30 005946](https://github.com/user-attachments/assets/06e1f382-6640-4141-971a-c1f3b7dea364)
