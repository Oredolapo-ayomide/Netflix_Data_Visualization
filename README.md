
# Netflix Data Visualization

## **Overview**

This project analyzes and visualizes Netflix shows and movies data using both **Python** and **R**.
The dataset contains information such as the title, director, cast, country, release year, rating, duration, genres, and description of Netflix content.

The goals of this assignment were:

1. **Data Preparation** – Unzip and rename the dataset to `Netflix_shows_movies`.
2. **Data Cleaning** – Handle missing values and ensure correct data types.
3. **Data Exploration** – Generate descriptive statistics and understand data patterns.
4. **Data Visualization (Python)** –

   * Plot the top 10 most frequent genres.
   * Plot the distribution of ratings.
5. **R Integration** – Recreate one visualization (ratings distribution) in R using `ggplot2`.

---

## **Project Structure**

```
Module 4 Assignment/
│
├── Netflix_shows_movies_cleaned.csv     # Cleaned dataset after Python preprocessing
├── netflix_analysis.py                  # Python script for data cleaning, exploration, and visualization
├── ratings_distribution.R               # R script for recreating the ratings distribution chart
├── README.md                             # Documentation (this file)
```

---

## **Requirements**

### **Python Requirements**

Install the following Python libraries:

```bash
pip install pandas matplotlib seaborn
```

### **R Requirements**

Install `ggplot2` in R (only needs to be done once):

```r
install.packages("ggplot2")
```

---

## **Step-by-Step Instructions**

### **1. Data Preparation (Python)**

* Load the raw CSV dataset.
* Save a cleaned version as `Netflix_shows_movies_cleaned.csv`.
* Ensure:

  * `date_added` is converted to `datetime`.
  * Missing values are handled (e.g., `date_added` filled with `NaT`).
  * Data types are appropriate.

### **2. Data Exploration (Python)**

* Generate summary statistics with:

  ```python
  df.describe(include='all')
  ```
* Identify missing values:

  ```python
  df.isnull().sum()
  ```

### **3. Data Visualization (Python)**

#### **a. Top 10 Most Frequent Genres**

* Genres were extracted from the `listed_in` column by splitting on commas.
* The **top 10 genres** were plotted using `seaborn.barplot()`.

#### **b. Ratings Distribution**

* Counted occurrences of each rating in the dataset.
* Plotted using `seaborn.barplot()`.

To run:

```bash
python netflix_analysis.py
```

This will generate both plots in Python.

---

### **4. Data Visualization (R)**

The file `ratings_distribution.R` recreates the **Ratings Distribution** chart from Python using `ggplot2`.

**Run in RStudio or R Console:**

```r
# Load ggplot2
library(ggplot2)

# Set working directory to folder containing this project
setwd("C:/Users/AyomideOgunsiji/OneDrive - VFD Group/Assignments/Module 4 Assignment")

# Run the script
source("ratings_distribution.R")
```

This will display the bar chart of ratings in R.

---

## **Outputs**

### **Python Charts**

1. **Top 10 Most Frequent Genres** – Horizontal bar chart showing the number of titles per genre.
2. **Distribution of Ratings** – Vertical bar chart showing how many titles fall into each rating category.

### **R Chart**

1. **Distribution of Ratings** – Same chart as above, but created in R with `ggplot2`.

---

## **Important Notes**

* **You must unzip** the entire `Module 4 Assignment` folder before running the codes.
* Do **not** run the codes directly from within the zipped folder. The script will not be able to access files.
* Unzip (extract all files) to a known location like `Desktop or Document` before running the script.
* Ensure `Netflix_shows_movies_cleaned.csv` is in the **same folder** as the `.py` and `.R` scripts before running them.
* If running the R script from another location, adjust the `setwd()` path accordingly.

---

