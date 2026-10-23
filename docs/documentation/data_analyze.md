## Research Topic:
### How Social Media Affects High School Students' Grades and Stress

### A short description on data analyze:
Data analysis is the process of collecting, cleaning, and examining data to find patterns, answer questions, and draw conclusions. For this technology project, we use Python to analyze student survey data from Kaggle to understand how daily screen time impacts high school students.

---

## 1. Project Goal & Questions
The goal of this project is to analyze high school student data to see if social media usage affects academic performance and mental well-being.

* **Key Question 1:** Does higher daily screen time result in lower student GPAs?
* **Key Question 2:** Which social media app is associated with the highest stress levels?
* **Key Question 3:** Does late-night screen time reduce total hours of sleep?

---

## 2. Dataset Overview (Kaggle)
The dataset used in this project is sourced from Kaggle and contains high school student survey responses.

* **Screen_Time:** Hours spent on social media per day.
* **Primary_App:** Main social media platform used (TikTok, Instagram, YouTube, etc.).
* **GPA:** Grade Point Average (0.0 – 4.0).
* **Sleep_Hours:** Average sleep duration per night.
* **Stress_Level:** Self-reported stress scale (1 to 10).

---

## 3. Step-by-Step Data Analysis Process

1. **Data Collection:** Downloaded student survey data from Kaggle in CSV format.
2. **Data Cleaning:** Removed duplicate records and handled missing values using statistical averages.
3. **Data Analysis:** Calculated summary statistics (mean GPA, average screen time, average stress levels).
4. **Data Visualization:** Created charts using Python libraries (`pandas`, `matplotlib`, and `seaborn`).

---

## 4. Python Analysis Code

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Set visual style for plots
sns.set_theme(style="whitegrid")

# 1. Load the Kaggle Dataset
df = pd.read_csv('student_social_media.csv')

# 2. Data Cleaning
df = df.drop_duplicates()
df = df.fillna(df.mean(numeric_only=True))

# 3. Print Key Summary Statistics
print("--- Project Data Summary ---")
print("Average Daily Screen Time (Hours):", round(df['Screen_Time'].mean(), 1))
print("Average GPA:", round(df['GPA'].mean(), 2))
print("Average Hours of Sleep:", round(df['Sleep_Hours'].mean(), 1))

# 4. Generate Visualizations
plt.figure(figsize=(12, 4))

# Chart 1: Screen Time vs GPA
plt.subplot(1, 2, 1)
sns.scatterplot(data=df, x='Screen_Time', y='GPA', color='blue')
plt.title('Screen Time vs. GPA')
plt.xlabel('Screen Time (Hours)')
plt.ylabel('GPA')

# Chart 2: Stress Level by Main App
plt.subplot(1, 2, 2)
if 'Primary_App' in df.columns and 'Stress_Level' in df.columns:
    sns.barplot(data=df, x='Primary_App', y='Stress_Level', ci=None, palette='mako')
    plt.title('Average Stress Level by Main App')
    plt.xlabel('Social Media App')
    plt.ylabel('Stress Level (1-10)')
    plt.xticks(rotation=30)

plt.tight_layout()
plt.show()
