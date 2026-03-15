# 📺 Netflix Content Analysis & Visualization

![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Latest-green?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-Latest-orange?style=flat-square)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-red?style=flat-square)

## 📊 Project Overview

Comprehensive visual analysis of 8,807 Netflix titles exploring content trends, regional patterns, and distribution across movies and TV shows.

**Completion Date:** March 12-14, 2026 | **Time Spent:** 6 hours across 3 days

---

## 🎯 Objectives

- Master data visualization techniques (matplotlib & seaborn)
- Analyze Netflix content distribution and trends
- Practice exploratory data analysis (EDA)
- Create publication-quality visualizations
- Build intuition for data storytelling

---

## 📁 Dataset Information

- **Source:** Kaggle - Netflix Movies and TV Shows Dataset
- **Size:** 8,807 titles
- **Features:** Type, Title, Director, Cast, Country, Date Added, Release Year, Rating, Duration, Genres, Description
- **Missing Values:** 4,307 across 6 columns
- **Time Range:** Content from 1925 to 2021

---

## 🔧 Technologies & Libraries

```python
pandas      # Data manipulation and analysis
numpy       # Numerical computations  
matplotlib  # Basic plotting and customization
seaborn     # Statistical visualizations
```

---

## 🎨 Visualizations Created (7 Total)

### **Day 1: Basic Visualizations (4 plots)**

1. **Line Chart** - Content Added Over Time
   - Reveals Netflix's content acquisition acceleration
   - Peak in 2019-2020 (COVID-19 impact)
   - Clear growth trend from 2015 onwards

2. **Pie Chart** - Movies vs TV Shows Distribution
   - Movies: 69.6%
   - TV Shows: 30.4%
   - Netflix focuses more on films than series

3. **Histogram** - Release Year Distribution  
   - Most content from 2000-2020
   - Some classic content from 1920s
   - Skewed toward recent releases

4. **Bar Chart** - Top 10 Countries
   - United States dominates production
   - India second (Bollywood content)
   - UK third (quality British content)

### **Day 2: Advanced Visualizations (3 plots)**

5. **Box Plot** - Release Year by Content Type
   - TV Shows tend to be newer
   - Movies have wider age range
   - Clear median differences

6. **Count Plot** - Top 10 Genres
   - International content dominates
   - Dramas most popular
   - Documentaries significant presence

7. **Scatter Plot** - Release Year vs Year Added
   - Classic content added recently
   - Most new releases added quickly
   - Netflix diversifying content age

---

## 🔍 Key Insights & Findings

### **Content Distribution**
- **69.6% movies** vs 30.4% TV shows
- Netflix prioritizes film content
- Movie library significantly larger

### **Geographic Trends**
- **United States** leads in content production
- **India** rapidly growing presence (Bollywood)
- **European content** well represented (UK, France, Spain)

### **Temporal Patterns**
- **2019-2020 spike** in content additions (pandemic effect)
- Steady growth from **2015 onwards**
- Recent focus on **2000-2020** releases

### **Content Strategy**
- Acquiring **classic films** from 1900s-1990s
- Producing **original content** (2015+)
- Balancing **international** and US content

### **Genre Distribution**
- International content prioritized
- Drama and comedy most common
- Documentaries significant category

---

## 🛠️ Data Cleaning Process

### **1. Column Standardization**
```python
df.columns = df.columns.str.strip()  # Remove whitespace
```

### **2. Feature Engineering**
```python
# Extract year from date_added
df['year_added'] = pd.to_datetime(df['date_added'], errors='coerce').dt.year

# Extract main genre
df['main_genre'] = df['listed_in'].str.split(',').str[0].str.strip()
```

### **3. Data Reduction**
```python
# Dropped irrelevant columns
df = df.drop(columns="show_id")
```

### **4. Missing Value Strategy**
- `director`, `cast`, `country`: Left as-is (informational only)
- `date_added`: Handled with `errors='coerce'`
- `rating`, `duration`: Minimal missing, analyzed as-is

---

## 💡 Skills Demonstrated

### **Data Analysis**
- ✅ Exploratory Data Analysis (EDA)
- ✅ Feature extraction from text
- ✅ Date/time manipulation
- ✅ Statistical summarization

### **Visualization**
- ✅ Matplotlib fundamentals
- ✅ Seaborn statistical plots
- ✅ Color theory and palettes
- ✅ Plot customization

### **Programming**
- ✅ Function creation (DRY principle)
- ✅ Docstring documentation
- ✅ Clean code practices
- ✅ Professional formatting

### **Communication**
- ✅ Data storytelling
- ✅ Insight extraction
- ✅ Markdown documentation
- ✅ Visual design

---

## 📊 Technical Details

### **Visualization Techniques Used**

**Matplotlib:**
- Line plots for time series
- Pie charts for proportions
- Histograms for distributions
- Bar charts for categories

**Seaborn:**
- Box plots for comparisons
- Count plots for frequencies
- Scatter plots with hue
- Color palettes (Set2, viridis)

**Customization:**
- Figure sizing (`figsize`)
- Color selection
- Edge colors (`edgecolor`)
- Label rotation
- Tight layouts

---

## 🚀 Future Enhancements

### **Additional Visualizations**
- [ ] Heatmap of content by country and type
- [ ] Time series with trend lines
- [ ] Correlation matrix
- [ ] Interactive dashboard with Plotly

### **Deeper Analysis**
- [ ] Director analysis (most prolific)
- [ ] Actor network analysis
- [ ] Rating distribution analysis
- [ ] Duration trends over time

### **Advanced Features**
- [ ] Sentiment analysis on descriptions
- [ ] Topic modeling on genres
- [ ] Recommendation system
- [ ] Predictive modeling (will content be added?)

---

## 📂 Project Structure

```
netflix-visualization-practice/
├── README.md                    # This file
├── netflix_visulas.ipynb        # Main analysis notebook
├── netflix_titles.csv           # Raw data (download from Kaggle)
└── visualizations/              # Saved plots (optional)
    ├── content_over_time.png
    ├── movies_vs_shows.png
    ├── release_year_dist.png
    ├── top_countries.png
    ├── release_by_type.png
    ├── top_genres.png
    └── release_vs_added.png
```

---

## 🏃 How to Run

### **Prerequisites**
```bash
Python 3.x
pandas
numpy
matplotlib
seaborn
jupyter
```

### **Installation**
```bash
# Clone repository
git clone https://github.com/Hcton75/netflix-visualization-practice.git
cd netflix-visualization-practice

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Download dataset from Kaggle
# Place netflix_titles.csv in project directory

# Launch Jupyter Notebook
jupyter notebook netflix_visulas.ipynb
```

### **Running the Analysis**
1. Open `netflix_visulas.ipynb`
2. Run all cells sequentially (Cell → Run All)
3. Visualizations will display inline
4. Review insights in markdown cells

---

## 🎓 What I Learned

### **Technical Skills**
- **Data Cleaning:** Handling real-world messy data
- **Feature Engineering:** Extracting year, genres from complex strings
- **Visualization:** Creating 7 different plot types
- **Seaborn Mastery:** Box plots, count plots, scatter with hue

### **Analytical Skills**
- **Pattern Recognition:** COVID-19 impact on content
- **Business Insights:** Netflix's content strategy
- **Storytelling:** Communicating findings visually

### **Best Practices**
- **Function Creation:** Reusable `loading_and_inspection()`
- **Documentation:** Professional docstrings and comments
- **Code Quality:** Clean, readable, maintainable
- **Version Control:** Git workflow, GitHub upload

---

## 📝 Learning Resources Used

**Video Tutorials:**
- Corey Schafer - Matplotlib & Pandas tutorials
- StatQuest - Data visualization principles
- Keith Galli - Real-world data analysis

**Documentation:**
- Matplotlib official docs
- Seaborn gallery
- Pandas user guide

**Practice:**
- Kaggle datasets
- Personal experimentation
- Iterative refinement

---

## 👤 Author

**Jeremy Koome**
- Email: jeremykoome475@gmail.com
- GitHub: [@Hcton75](https://github.com/Hcton75)
- Location: Nairobi, Kenya

---

## 🎊 Project Milestones

✅ Day 1: 4 basic visualizations complete  
✅ Day 2: 3 advanced visualizations complete  
✅ Total: 7 high-quality plots created  
✅ Professional notebook ready for portfolio  
✅ GitHub repository published  

**Part of my 18-month journey to become a top 1% data scientist** 🚀

---

## 🌟 Acknowledgments

- **Dataset:** Netflix Movies and TV Shows (Kaggle)
- **Inspiration:** Week 1 of data science bootcamp
- **Coach:** For guidance and feedback
- **Community:** Kaggle and data science community

---

<div align="center">

### ⭐ Star this repo if you found it helpful!

**Week 1, Project 3 of my data science journey**

![Profile Views](https://komarev.com/ghpvc/?username=Hcton75&label=Project+Views&color=brightgreen)

</div>
