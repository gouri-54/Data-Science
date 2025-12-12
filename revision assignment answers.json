{
  "metadata": {
    "kernelspec": {
      "name": "python",
      "display_name": "Python (Pyodide)",
      "language": "python"
    },
    "language_info": {
      "codemirror_mode": {
        "name": "python",
        "version": 3
      },
      "file_extension": ".py",
      "mimetype": "text/x-python",
      "name": "python",
      "nbconvert_exporter": "python",
      "pygments_lexer": "ipython3",
      "version": "3.8"
    }
  },
  "nbformat_minor": 5,
  "nbformat": 4,
  "cells": [
    {
      "id": "014d7cc6-d01d-4143-a591-01beea92319a",
      "cell_type": "code",
      "source": "Answers",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "287f7727-558a-40a2-9adc-9e6f5f681ed9",
      "cell_type": "code",
      "source": "1.Q1. \n•\tSelect any random dataset.\n•\tLoad it using Pandas.\n•\tDisplay the first 10 rows, shape, column names, and data types.\n    \n import pandas as pd\nimport numpy as np\nnp.random.seed(42)  \ndata = {\n\"Product\": np.random.choice([\"Laptop\", \"Mobile\", \"Tablet\", \"Headphone\", \"Camera\"], 500), \n                    #categorical\n    \"Price\": np.random.randint(5000, 80000, 500),  # numerical integers\n    \"Quantity\": np.random.randint(1, 20, 500),    # numerical integers\n    \"Category\": np.random.choice([\"Electronics\", \"Accessories\"], 500),  # categorical\n    \"Rating\": np.random.uniform(1.0, 5.0, 500).round(1),  # numerical float\n}\ndf = pd.DataFrame(data)\nprint(df.head())\ndf\n# Display first 10 rows\nprint(df.head(10))\n\n# Dataset shape\nprint(\"Shape:\", df.shape)\n\n# Column names\nprint(\"Columns:\", df.columns)\n\n# Data types\nprint(\"Data types:\\n\", df.dtypes)\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "3f212a72-4e52-469b-877c-2f32bd6b6dd9",
      "cell_type": "code",
      "source": "2. Create a bar chart for any categorical column showing counts.\nimport seaborn as sns\nimport matplotlib.pyplot as plt\n\nsns.countplot(data=df, x=\"Product\")\nplt.title(\"Count of Products\")\nplt.show()\n    ",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "5899d1ea-51b5-46cb-aab5-ec9abdd794de",
      "cell_type": "code",
      "source": "3.Create a pie chart for the same or a different categorical column.\n    import matplotlib.pyplot as plt\ndf['Category'].value_counts().plot.pie(autopct='%1.1f%%', colors=['skyblue', 'orange'])\nplt.title(\"Category Distribution\")\nplt.ylabel('')\nplt.show()",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "0d4f37f0-1403-49a6-a4db-3910f198d885",
      "cell_type": "code",
      "source": "4.Create a histogram for any numerical column.\n\n    plt.hist(df['Price'], bins=10, color='green', edgecolor='black')\nplt.title(\"Price Distribution\")\nplt.xlabel(\"Price\")\nplt.ylabel(\"Frequency\")\nplt.show()\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "7e6adca0-4b8a-4483-ad29-f0c5e6bebe94",
      "cell_type": "code",
      "source": "5.Create a scatter plot between any two numerical variables.\n    import seaborn as sns\nsns.scatterplot(data=df, x=\"Price\", y=\"Quantity\")\nplt.title(\"Price vs Quantity\")\nplt.show()",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "b4f1e607-d1db-4884-8fff-14e47f04863e",
      "cell_type": "code",
      "source": "6. Create a box plot for a numerical variable.\n    import seaborn as sns\nsns.boxplot(data=df, y=\"Rating\")\nplt.title(\"Box Plot of Ratings\")\nplt.show()\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "1ac018ac-a6c0-451a-9845-baf354c967e3",
      "cell_type": "code",
      "source": "7.Create a scatter plot between two numerical variables.\n   import seaborn as sns\nsns.scatterplot(data=df, x=\"Price\", y=\"Rating\", hue=\"Category\")\nplt.title(\"Price vs Rating by Category\")\nplt.show() ",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "80fa8f6e-5ece-4027-ab6d-6df9eda4a759",
      "cell_type": "code",
      "source": "8. Create multiple histograms for two numerical variables on separate plots.\n    plt.figure(figsize=(12,5))\n\nplt.subplot(1,2,1)\nplt.hist(df['Price'], bins=10, color='blue', edgecolor='black')\nplt.title(\"Price Distribution\")\n\nplt.subplot(1,2,2)\nplt.hist(df['Quantity'], bins=10, color='red', edgecolor='black')\nplt.title(\"Quantity Distribution\")\n\nplt.show()\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "b8e22997-5a9e-4ab6-ad20-2fdfecbf97fe",
      "cell_type": "code",
      "source": "9.Create a box plot grouped by category.\n    import seaborn as sns\nsns.boxplot(data=df, x=\"Category\", y=\"Price\")\nplt.title(\"Price Distribution by Category\")\nplt.show()\n\n    ",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "b3297189-57bb-46b1-bf27-c1f19f0c20c3",
      "cell_type": "code",
      "source": "10.Identify the least frequent categories and visualize them in a bar chart.\n    least_freq = df['Product'].value_counts().nsmallest(2)\nleast_freq.plot.bar(color='purple')\nplt.title(\"Least Frequent Products\")\nplt.xlabel(\"Product\")\nplt.ylabel(\"Count\")\nplt.show()\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "fbda2152-ad77-493e-9d6b-b262554ac59d",
      "cell_type": "code",
      "source": "",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    }
  ]
}