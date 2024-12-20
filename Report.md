{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "e41fddbc-262f-402c-9ccd-fdcf5e77d7e0",
   "metadata": {},
   "source": [
    "# Report"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ab7693ec-5914-4160-98e6-9f04e46ecbf6",
   "metadata": {},
   "source": [
    "## Exploring 120 Years of Olympic History: Trends in Athletes and Results"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "0b6897fd-6447-40f1-bc03-5e3647ff7c05",
   "metadata": {},
   "source": [
    "## Objective"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6df61461-b648-40eb-8395-0057705b6a90",
   "metadata": {},
   "source": [
    "```Analyzing Olympic Trends: A Data-Driven Exploration of Athlete Demographics, Sport Evolution, and Participation Over 120 Years```\n",
    "\n",
    "The objective of this project is to examine trends in athlete ages, sex, and physical attributes (e.g., height and weight) across 120 years of Olympic history. This includes investigating how the number of participating countries has increased over time and analyzing the rise of female participation, particularly as female categories of sports were introduced—something that was not prevalent in the early 1920s.\n",
    "\n",
    "Additionally, the project aims to explore the representation of smaller countries, examining their ability to win medals compared to historically dominant nations. Lastly, the analysis seeks to understand age diversity by studying how participants span across different age groups."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6135209b-7e1d-4e75-b9c7-19104837ab84",
   "metadata": {},
   "source": [
    "## Introduction"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "645c3c3c-a4a8-449e-9ef0-c14680d0b6bb",
   "metadata": {},
   "source": [
    "This is a historical dataset on the modern Olympic Games, including all the Games from Athens 1896 to Rio 2016. The data contains 271116 rows and 15 columns. Each row corresponds to an individual athlete competing in an individual Olympic event (athlete-events). \n",
    "The data can be interpreted in different ways. I aim to understand the trends of the Olympics over the 120 years. I started with understanding the data by going through the different columns for what data can be used to understand the trend. The data had good percentage of missing values for columns like Age, Weight, Height and Medals. These were important columns needed to understand the demographic trends and also to understand what are the top teams with most wins. So, I had to clean up the data for visualization and analysis. "
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6d9cc6da-4faa-4410-8bcc-a64661bd69a1",
   "metadata": {},
   "source": [
    "## Method\n",
    "\n",
    "```Handling Missing Values```:\n",
    "* Age, Height, and Weight: Missing values for these columns were replaced with median values to preserve the underlying trends and ensure meaningful analysis.\n",
    "* Medals: Missing medals were assigned as \"None\" to maintain the integrity of the dataset and prevent the exclusion of any athlete records.\n",
    "\n",
    "```Data Cleaning```:\n",
    "* Removing Duplicate Rows: Ensured data quality by removing duplicate records that could skew the analysis.\n",
    "* Consistency Checks: Uniform capitalization for country names and renaming columns (e.g., \"Team\" to \"Country\") to maintain consistency.\n",
    "\n",
    "\n",
    "```Exploratory Data Analysis```:\n",
    "* Grouping and summarizing data to identify patterns over time : For example for understanding the trends of several sports over the years, grouping the data in several decades helped me better understand the trends of the popularity of the sports over the recent decades compared to the past decades. The trends of the sports does not changes over few years. So, this gives more clarity.\n",
    "* Identifying outliers and anomalies in the data is essential if you have large set of data some outliers can be disregarded."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "37068819-c5d1-48e8-ab3a-7806f2f1a1aa",
   "metadata": {},
   "source": [
    "### Understand dataset"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ef0cc2d6-8ac6-4a18-8665-120f5e10cc58",
   "metadata": {},
   "source": [
    "```Data Wrangling```:\n",
    "* Loading and Inspecting: Loaded the dataset and inspected its structure, including columns, data types, and missing value percentages.\n",
    "* Copying the DataFrame: Created a working copy to ensure that any modifications did not affect the original dataset."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "631462b7-dba5-41d9-ba59-273effc5cea6",
   "metadata": {},
   "source": [
    "### Validate Data"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "49b635c6-b0f2-435e-9420-6e8ae8d13065",
   "metadata": {},
   "source": [
    "```Data Validation```: Checked for duplicates, inconsistencies, and ensured that all numeric columns were in a valid format, free of outliers, and properly standardized."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5872dc97-e4cb-4714-a46f-ffa20d5f2296",
   "metadata": {},
   "source": [
    "## Story Telling"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a8a29dda-b15d-4867-ab47-0845c261064b",
   "metadata": {},
   "source": [
    "![Bar Graph for Gender Participation](imgs/bar_graph_sex.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "86d0b2f1-bf05-4016-8c19-8f88cc66a4d7",
   "metadata": {},
   "source": [
    "\n",
    "```Participants Trends```: Trying to understand the participants based on the sex over the different decades. This shows that majority of the females started participating in late 2000s. However, the first time women started participating in the Olympics was from 1990s. However, the participants only increased significantly once since 1960s. Due to the World War I, **1916 Olympics** was cancelled. Again, World War II, the Olympics for years **1940 & 1944 Olympics** were cancelled."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9e4cd7bc-356e-4091-8f52-4a3a22963bcd",
   "metadata": {},
   "source": [
    "![Bar Plot](imgs/medal_gender.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9356182d-c8b5-4736-beac-118936a07e17",
   "metadata": {},
   "source": [
    "```Bar Plot for Gender Participation```: There has been a steady increase in the number of participants in the Olympics over the years. Small bumps in the trend are noticeable due to higher participation in the Summer Olympics compared to the Winter Olympics, which naturally features fewer sports and athletes. Grouping the data by Year, Season, and Sex reveals distinct trends in gender participation. There has been a notable rise in female participation since the 1980s, especially for the Summer Olympics, where the gap between male and female athletes began to narrow significantly. A similar increase in female participation is also evident in the Winter Olympics starting in 1984."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ae335be1-3d33-484f-81f2-70a9ab87b28c",
   "metadata": {},
   "source": [
    "![Bar Plot](imgs/bar_plot_gender_output_expected.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a640ac74-932c-409d-a667-62fd4c35649b",
   "metadata": {},
   "source": [
    "```Bar Plot for Gender Representation Over Time:```The trend can be seen here as well in the plot above which again proves that there is significant increase in the number of female athletes in recent years. Also, we can see that the number of participants in the Summer Olympics are significantly more. Possible reason could be since there are more sports events in Summer Olympics compared to the Winter Olympics."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7f024b6c-674d-423e-9147-9576ddea9b3a",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "cdc92dd4-2e54-4529-9490-21f23baecd46",
   "metadata": {},
   "source": [
    "![Heatmap](imgs/heatmap.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b55fa877-9af5-4782-b593-86cd0eb20420",
   "metadata": {},
   "source": [
    "``` Heatmap of Medals by Sport and Decade```A heatmap visualized which sports have gained popularity over time. Athletics and Swimming dominated the medal count across decades, while other sports saw fluctuating engagement. The heatmap illustrated how medal distribution has evolved across different sports over time. Athletics and Swimming consistently dominated the medal count across decades, highlighting their popularity and wide range of events."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "610bbf36-a955-4632-a4d9-6262c812ca2b",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5dca7573-b5ab-4157-9481-1236c073978b",
   "metadata": {},
   "source": [
    "![Scatter Plot](imgs/scatterplot.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "49b6f74c-6476-4388-94f1-9ca4f683eb86",
   "metadata": {},
   "source": [
    "```Countries with higher Participation have higher Medal Counts```:In the Olympics, countries that send larger athlete delegations tend to win more medals. This positive correlation makes intuitive sense: more athletes mean more opportunities to participate in different events, which naturally leads to a higher probability of winning medals. Countries that are able to participate in a wide variety of sports increase their chances of winning medals across multiple disciplines. By fielding athletes in a range of sports, these countries are more likely to secure medals in at least a few events."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2a5947e0-27f5-4183-b10d-50a6ddf753b3",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "dfb95577-1f02-4d9f-bd64-adc5057973ee",
   "metadata": {},
   "source": [
    "![Medal Season](imgs/medal_season.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "24dee94c-5701-44ba-95b1-ee4a0beb6039",
   "metadata": {},
   "source": [
    "```Seasonal Trends for Medals```: The Summer Olympics have consistently attracted a larger number of participants and awarded more medals compared to the Winter Olympics, mainly due to a broader range of sports and events."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9143db09-d4ff-47c1-8e58-170056b9e182",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "20c18054-8cdd-47ac-aded-d5019c2d3a2e",
   "metadata": {},
   "source": [
    "![BoxPlot](imgs/box_plot.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9e4db643-9e20-4271-a5b9-863b140dcaf6",
   "metadata": {},
   "source": [
    "```BMI Distribution by Sport```: A box plot highlighted the diversity of physical requirements across sports, demonstrating how different body types excel in different disciplines. Sports like gymnastics favored leaner body types, whereas weightlifting showed a preference for higher BMI."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "183e2f0b-428c-4ecd-b472-6637905b7dd4",
   "metadata": {},
   "source": [
    "![Bar Plot](imgs/top10winners.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5ea23979-6c54-4cba-a65d-021fc0256cd4",
   "metadata": {},
   "source": [
    "```Top 10 COuntries with most medal wins```:\n",
    "* The United States and the Soviet Union have been dominant forces in the Olympics, with large delegation sizes and investments in sports programs leading to significant medal counts.\n",
    "* Germany, Italy, France, and other European nations have had balanced success across all medal categories, indicating sustained performance in a diverse range of sports.\n",
    "* Smaller nations like Finland and Australia have managed to compete among the top 10 by specializing in particular disciplines, highlighting that focused training programs can lead to significant success.\n",
    "* These are mostly the economically flourished countries which are able to invest a lot in these athletes which might be the reason - they have the greatest number of wins."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6cc00ce9-eba9-4c73-8ec7-04d23d70111b",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "e3ec683e-6d08-4f21-b9a2-bc90be44193e",
   "metadata": {},
   "source": [
    "![Bar Plot](imgs/height_sex.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b7dcdadf-4868-434a-997d-31b779e9554b",
   "metadata": {},
   "source": [
    "Male athletes tend to be taller, with the average height peaking around 180 cm, while female athletes peak around 165 cm. These differences reflect both biological factors and the specific physical requirements of different sports.\n",
    "The analysis also highlights overlap in height for both genders, particularly in sports where height plays a less critical role, such as gymnastics or diving."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a23094a1-6a64-4ea2-b1a4-7e11f23a675d",
   "metadata": {},
   "source": [
    "---"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "8ade25f7-064a-4523-b232-790dfda223a3",
   "metadata": {},
   "source": [
    "## Conclusion"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c5efdc98-9f2f-436f-bdf6-ceaad53ce1a1",
   "metadata": {},
   "source": [
    "The Olympics have grown not only in size and scope but also in terms of inclusivity and diversity. The increasing representation of female athletes and the rise of new sports have contributed to making the games more equitable and engaging.\n",
    "Medal success is often a reflection of a nation's ability to invest in and nurture its athletes. Countries with larger athlete delegations generally perform better, but focused training and specialization allow even smaller nations to achieve greatness.\n",
    "The analysis of athlete physical attributes across sports shows that different body types are favored in different disciplines, emphasizing the unique demands of each sport and the diversity of talents required to excel.\n",
    "\n",
    "The Olympic Games serve as a reflection of global progress in sports, inclusivity, and competitive excellence. The trends observed in participation, medal success, and the evolution of sports underscore the dynamic nature of the Olympics—continually adapting to reflect societal changes and the pursuit of human excellence.\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "dfaa36ef-d0c3-444c-95fb-0ffbf72bd20b",
   "metadata": {},
   "source": [
    "### References"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "48f3e6c9-90f8-4287-9d34-77d43595ab1c",
   "metadata": {},
   "source": [
    "* https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results/data\n",
    "* https://www.sports-reference.com/\n",
    "* https://plotly.com/python/getting-started/"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "36c30b17-1f6e-4bf8-9411-ef7e48e69c75",
   "metadata": {},
   "source": [
    "## Acknowlegment"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b5ece74a-802d-49fb-8280-27050f6a5e14",
   "metadata": {},
   "source": [
    "I would like to thank Dr. Nerolu for her great support and guidance to explore these techniques and I really think this would be helpful in the field that I will working on. "
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
