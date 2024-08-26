## Overview

This repo contains code for the Pluralsight course [Retrieval Augmented Generation (RAG) with Azure AI Search]

## Pre-requisites
### Local Setup
1. Install [Miniconda](https://docs.anaconda.com/miniconda/miniconda-install/) if you haven't already.
2. Open your terminal and create a new Conda environment using the following command. Replace `myenv` with the name you want to give to your environment.

```bash
conda create -n azure-ai-search python=3.12
```
3. Activate the environment.

```bash
conda activate azure-ai-search
```
4. Install [VS Code](https://code.visualstudio.com/) if you haven't already. Then, install the following extensions:
    - Python
    - Jupyter
    - Data Wrangler (optional)

### Infrastructure Setup
1. Create an [Azure account](https://azure.microsoft.com/en-us/free/search) if you haven't already.
2. Create [OpenAI account](https://platform.openai.com/signup) if you haven't already. This is required to use the `GPT-4o-mini` model.

## Data

The data has been taken from [Hotel Reviews Dataset](https://www.kaggle.com/datasets/datafiniti/hotel-reviews). Since this is a huge file, we have taken a subset of the data for this course. You can create reviews easily by going through the following steps

- Download the data from the above link. You will need to sign in to Kaggle to download the data.
- Unzip the file and you will get a file named `Datafiniti_Hotel_Reviews.csv`
- Run the following command to get the first 1000 reviews

```sh
head -1000 Datafiniti_Hotel_Reviews.csv > hotel_reviews_1000.csv
```

If you need more reviews, you can increase the number in the above command. For example, to get 5000 reviews, you can run the following command

```sh
head -5000 Datafiniti_Hotel_Reviews.csv > hotel_reviews_5000.csv
```

- The file in the `data/raw` folder is the output of the above command. You can do so by running the following command

```sh
cp hotel_reviews_1000.csv <path_to_project>/azure-ai-search/data/raw
```

Replace `<path_to_project>` with the path that locates the project on your machine.

## Resources

- [Azure AI Search](https://azure.microsoft.com/en-us/products/ai-services/ai-search/)
- [What's Azure AI Search](https://learn.microsoft.com/en-us/azure/search/search-what-is-azure-search)