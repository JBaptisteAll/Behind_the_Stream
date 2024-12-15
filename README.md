# Behind the Stream 🎬: Analyzing Netflix's Catalogue



## **Introduction**
Netflix has transformed the way audiences consume content by pioneering the streaming industry, becoming a global leader in on-demand entertainment. This project focuses on analyzing and visualizing Netflix's catalogue to uncover key trends and insights through interactive dashboards.

The main objectives of this project include:
- Determining the most represented genres on the platform.
- Examining Netflix's availability across countries.
- Identifying the countries with the largest content libraries.
- Exploring the predominant genres in each country.
- Investigating seasonal patterns in the addition of new content.

---

## **Dataset**
This project uses the **Netflix Titles Dataset**, which includes information about TV shows and movies available on Netflix. Key columns in the dataset include:
- `title`: The name of the movie/TV show.
- `type`: Whether the title is a movie or a TV show.
- `country`: The countries where the title is available.
- `release_year`: The year the title was released.
- `genre`: Genres associated with the title.
- `cast`: The actors involved in the title.
- `date_added`: The date the title was added to Netflix.

**Dataset Source**: [Netflix Titles Dataset](https://www.kaggle.com/shivamb/netflix-shows)

---

## **Data Processing**
### **Data Cleaning and Transformation in Power Query**
The dataset underwent significant cleaning and transformation steps in Power Query to prepare it for analysis:

1. **Importing and Initial Exploration**:
   - The dataset was loaded into Power Query for cleaning and transformation.
   - Columns were reviewed for inconsistencies, missing values, and incorrect data types.

2. **Handling the `cast` and `country` Columns**:
   - **`cast`**: The column contained multiple actors listed in a single cell. It was split into multiple columns, and only the **first three actors** were retained for analysis.
   - **`country`**: In cases where multiple countries were listed, only the **first country** was kept, assuming it as the primary country.

3. **Processing the `genre` Column**:
   - The table was duplicated to focus on genre analysis.
   - The **`genre`** column was split into multiple rows, with each genre occupying its own row.
   - Null values in this column were removed.
   - Only the columns **`Show_ID`** and **`country`** were retained in the new table.
   - A relationship was established between the original table and the new table using **`Show_ID`** as the key, ensuring proper cardinality.

4. **Removing Empty and Erroneous Values**:
   - Rows with missing or erroneous data were filtered out to ensure clean and reliable analysis.

5. **Data Type Conversion**:
   - Columns were converted to their appropriate data types, such as dates, text, and numbers, to facilitate accurate visualizations.

---

## **Dashboard Features**
The Power BI dashboard is divided into several interactive pages, each focusing on a specific aspect of Netflix's catalogue:

1. **Home Page**:
   - Provides a global overview of Netflix's availability.
   - Includes a world map showing the distribution of content across countries.
   
---
![Home Page](https://github.com/JBaptisteAll/Behind_the_Stream/blob/main/Print%20Screen/Home.png)
---

2. **General Page**:
   - Displays the most present genres, actors, and directors globally.
   - Provides insights into how genres have evolved over time.
   ---
   ![General Page](https://github.com/JBaptisteAll/Behind_the_Stream/blob/main/Print%20Screen/General.png)
   ---

3. **Movies Page**:
   - Focuses specifically on movies.
   - Highlights the most common genres, actors, and directors in the movies category.
   ---
   ![Movies Page](https://github.com/JBaptisteAll/Behind_the_Stream/blob/main/Print%20Screen/Movie.png)
   ---

4. **TV Shows Page**:
   - Focuses specifically on TV shows.
   - Highlights the most common genres, actors, and directors in the TV shows category.
   ---
   ![TV Shows Page](https://github.com/JBaptisteAll/Behind_the_Stream/blob/main/Print%20Screen/TV_Show.png)
   ---



---

### Demonstrations
Below is a showcase of the interactive features of each page:

#### Behind the Stream 🎥
![Overall Show Page](https://github.com/JBaptisteAll/Behind_the_Stream/blob/main/Print%20Screen/Overall_show.gif)
- The Netflix logo at the top left corner acts as a **"Home" button**, allowing users to return to the main page.
- The three icons at the bottom of the Home page are navigation buttons that direct users to the **General**, **Movies**, and **TV Shows** pages respectively.
- Each page features interactive filters for deeper exploration, allowing users to drill down into specific countries or time periods.


---

## **Technologies Used**
The following tools and technologies were used to develop this project:

- **Power BI**: For creating the interactive dashboard.
- **Power Query**: For cleaning and transforming the dataset.
- **GitHub**: For version control and project hosting.
- **Microsoft Excel**: For preliminary data exploration.

---

## **Future Improvements**
Possible enhancements to this project include:

- Adding deeper insights into watch time and user preferences.
- Integrating real-time updates for dynamic visualizations.
- Expanding the analysis to include revenue and subscription trends.

---

## **Conclusion**
This project demonstrates the power of data visualization in uncovering insights from complex datasets. By analyzing and visualizing Netflix's catalogue, this dashboard provides actionable insights into content availability, genre popularity, and trends over time.

This project highlights skills in data processing, visualization, and storytelling, making it a valuable addition to any data analyst portfolio.