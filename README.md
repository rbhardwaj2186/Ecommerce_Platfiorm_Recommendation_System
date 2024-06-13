# Ecommerce_Platfiorm_Recommendation_System
 Predict Home Ecommerce search-product relevance
# Ecommerce_Platfiorm_Recommendation_System
 Predict Home Ecommerce search-product relevance
# Ecommerce Platform Search Relevance Prediction

## Project Description

This project involves a dataset containing a variety of products and real customer search terms from an ecommerce platform's website. The challenge is to predict a relevance score for the provided combinations of search terms and products. To create the ground truth labels, the ecommerce platform has crowdsourced the search/product pairs to multiple human raters.

![How-to-Integrate-Recommendation-Engine-with-E-commerce-Platforms.jpg…]()

 


The relevance score is a number between 1 (not relevant) to 3 (highly relevant). For example, a search for "AA battery" would be considered highly relevant to a pack of size AA batteries (relevance = 3), mildly relevant to a cordless drill battery (relevance = 2), and not relevant to a snow shovel (relevance = 1).

Each pair was evaluated by at least three human raters. The provided relevance scores are the average value of the ratings. There are three additional things to know about the ratings:
- The specific instructions given to the raters are provided in relevance_instructions.docx.
- Raters did not have access to the attributes.
- Raters had access to product images, while the competition does not include images.

Your task is to predict the relevance for each pair listed in the test set. Note that the test set contains both seen and unseen search terms.

## File Descriptions

- `train.csv`: The training set, contains products, searches, and relevance scores.
- `test.csv`: The test set, contains products and searches. You must predict the relevance for these pairs.
- `product_descriptions.csv`: Contains a text description of each product. You may join this table to the training or test set via the product_uid.
- `attributes.csv`: Provides extended information about a subset of the products (typically representing detailed technical specifications). Not every product will have attributes.
- `sample_submission.csv`: A file showing the correct submission format.
- `relevance_instructions.docx`: The instructions provided to human raters.

## Data Fields

- `id`: A unique Id field which represents a (search_term, product_uid) pair.
- `product_uid`: An id for the products.
- `product_title`: The product title.
- `product_description`: The text description of the product (may contain HTML content).
- `search_term`: The search query.
- `relevance`: The average of the relevance ratings for a given id.
- `name`: An attribute name.
- `value`: The attribute's value.
