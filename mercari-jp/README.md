# JP Sales Data: Explore Trends and Predict Prices 
# Mercari Japanese Item Listings (Apr 2024) 🛍

This dataset contains items listed and sold on Mercari's Japanese website (http://mercari.jp) offering a unique glimpse into the world of e-commerce on the website.
It may be useful for various tasks including classification, regression, natural language processing, and price prediction. Non commercial use only. I hope next generation of data engineers find this interesting.

## Data Overview:

- **Content:** List of sold items on Mercari Japanese website
- **Source:** In-house web scraper via official web interface
- **Number of samples:** about 460,000 (one row per item)
- **Data format:** TSV
- **Encoding:** UTF-8

<!--
* **Rich Attributes:** Features item details like name, price, brand, condition, shipping information, category (up to 6 levels), and seller ID (obfuscated).
* **Image URLs:** Each listing includes a link to the primary item image, enabling computer vision and image-based analysis.
* **Time-Series Data:** The "updated_date" field allows you to explore how listings evolve and investigate temporal trends.

## Potential Applications:

* **Price Prediction:** Train machine learning models to predict item prices based on features and historical data.
* **Trend Analysis:** Analyze popular categories, brands, and pricing strategies over time.
* **Market Research:** Gain insights into consumer behavior and preferences on Mercari JP.
* **Natural Language Processing:** Explore item descriptions and titles to understand language used in e-commerce listings.
* **Computer Vision:** Utilize image URLs to classify items or extract visual features.
-->

## Feature Description:

|      Feature Name     |              Description                           |    Data Type    |
|-----------------------|----------------------------------------------------|-----------------|
| **id**                | Obfuscated item identifier                         | str             |
| **is_shop**           | Indicates if the seller is a shop  (0 = n; 1 = y)  | int/bool        |
| **name**              | Item name                                          | str             |
| **item_description**  | Item's description                                 | str             |
| **price**             | Listed price (yen) of the item                     | int             |
| **brand_name**        | Item brand (if available)                          | str/categorical |
| **item_condition**    | Item's condition (e.g., new, used,...)             | int/categorical |
| **shipping**          | Who pays for shipping (0 = buyer; 1 = seller)      | int/bool        |
| **shipping_from_area**| Area where the item ships from                     | int/categorical |
| **shipping_duration** | Estimated shipping time                            | int/categorical |
| **seller_id**         | Obfuscated seller identifier                       | str             |
| **category_name**     | Categories (levels are separated by "/")           | str/categorical/joined |
| **updated_date**      | Last updated date (rounded by 4 hours)             | date            |

<!--
| shipping_payer     | Who pays for shipping (seller or buyer)         | String    |
| condition          | Item's condition (e.g., new, used)              | String    |
| status             | Current status of the item (e.g., active, sold) | String    |
| shipping_method    | Shipping method used                            | String    |
| image_0            | URL of the item's cover photo                   | String    |
| image_N            | URLs of the item's photo (upto 24 photos)       | String    |
| category_name_N    | Category level N (up to 6 levels)               | String    |
-->

## Important Notes:

- This dataset is made public for educational purpose. Please use it for non-commercial use only.
- This dataset includes items across all categories, allowing you to analyze diverse product types
- Certain data points were anonymized (`seller_id`, `item_id`) or removed (`description`, `update_time`) to prevent misuse.
- Brand and category IDs have been replaced with corresponding names for easier use.
- Sellers and items are obfuscated but still identifiable by manually searching it on original site.

## Contact:

If you find this dataset valuable or have suggestions, feel free to contact me.

This dataset is currently on beta. Do you want some Kaggle competition with this?
Do you want other features imported from original data source?
<!--
We encourage you to explore this dataset and share your findings with the Kaggle community!
-->

## Future Data Acquisition:

The dataset is intended to be updated over time.
This version includes data collected between April 1st and April 22th,

