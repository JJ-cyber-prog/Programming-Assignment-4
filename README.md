# Programming-Assignment 4

This is my fourth programming assignment. It talks about Data Wrangling and Data Visualization. Data Wrangling helps the programmer to clean and preprocess the data, ensuring accuracy and consistency, which are essential for meaningful analysis. Well-wrangled data also leads to faster processing times and more efficient algorithms, which saves a lot of time and computational resources for the data receiver. Data Visualization make it easier to spot trends, outliers, and patterns that might not be obvious in raw data. Good visualizations support data-driven decision-making by providing a clear representation of insights.

# My codes are as follows:

# For number 1, create the following data frames based on the format provided:

Vis_df = df[(df['Hometown'] == 'Visayas') & (df['Math'] < 70)]

Vis_df = Vis_df[['Name', 'Gender', 'Track', 'Math']]

Vis_df

# a. Instrumentation majors who lives in Luzon

Instru_df = df[(df['Track'] == 'Instrumentation') & (df['Hometown'] == 'Luzon') & (df['Electronics'] > 70)]

Instru_df = Instru_df[['Name', 'GEAS', 'Electronics']]

Instru_df

# b. Mindanaoan female board exam takers

Mindy_df = df[(df['Hometown'] == 'Mindanao') & (df['Gender'] == 'Female')].copy()

Mindy_df.loc[:, 'Average'] = Mindy_df[['Math', 'GEAS', 'Electronics']].mean(axis = 1)

Mindy_df = Mindy_df[['Name', 'Track', 'Electronics', 'Average']]

Mindy_df

# For number 2, create a visualization that shows how the different features contributes to average grade.

### Let's start with Average Grade by Gender:

import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (10, 6))

sns.boxplot(x = 'Gender', y = 'Average', data = df)

plt.title('Average Grade by Gender')
plt.xlabel('Gender')
plt.ylabel('Average Grade')

plt.show()

### Then, Average Grades by Track/College:

import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (10, 6))

sns.boxplot(x = 'Track', y = 'Average', data = df)

plt.title('Average Grade by Track')
plt.xlabel('Track')
plt.ylabel('Average Grade')

plt.show()

### Finally, Average Grades by Hometown:

import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (10, 6))

sns.boxplot(x = 'Hometown', y = 'Average', data = df)

plt.title('Average Grade by Hometown')
plt.xlabel('Hometown')
plt.ylabel('Average Grade')

plt.show()

These are my codes for the fourth programming assignment: Data Wrangling and Data Visualization.

# Authors:
Jerome Oldan
