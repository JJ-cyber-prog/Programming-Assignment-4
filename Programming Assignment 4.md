```python
# Create Data Frames
# Create visualization

import pandas as pd

# Initializing and loading the dataset
file_path = 'board2.xlsx'
df = pd.read_excel(file_path)

df.loc[:, 'Average'] = df[['Math', 'GEAS', 'Electronics']].mean(axis = 1)

# Displaying the first few rows of the dataset
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Gender</th>
      <th>Track</th>
      <th>Hometown</th>
      <th>Math</th>
      <th>Electronics</th>
      <th>GEAS</th>
      <th>Communication</th>
      <th>Average</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>S1</td>
      <td>Male</td>
      <td>Instrumentation</td>
      <td>Luzon</td>
      <td>58</td>
      <td>89</td>
      <td>75</td>
      <td>78</td>
      <td>74.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>S2</td>
      <td>Female</td>
      <td>Communication</td>
      <td>Mindanao</td>
      <td>52</td>
      <td>75</td>
      <td>90</td>
      <td>52</td>
      <td>72.333333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>S3</td>
      <td>Female</td>
      <td>Instrumentation</td>
      <td>Mindanao</td>
      <td>83</td>
      <td>74</td>
      <td>77</td>
      <td>57</td>
      <td>78.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>S4</td>
      <td>Male</td>
      <td>Instrumentation</td>
      <td>Visayas</td>
      <td>65</td>
      <td>58</td>
      <td>91</td>
      <td>68</td>
      <td>71.333333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>S5</td>
      <td>Male</td>
      <td>Communication</td>
      <td>Luzon</td>
      <td>59</td>
      <td>86</td>
      <td>43</td>
      <td>88</td>
      <td>62.666667</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Create Data Frames
# Create visualization

import pandas as pd

# Initializing and loading the dataset
file_path = 'board2.xlsx'
df = pd.read_excel(file_path)

# Displaying the first few rows of the dataset
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Gender</th>
      <th>Track</th>
      <th>Hometown</th>
      <th>Math</th>
      <th>Electronics</th>
      <th>GEAS</th>
      <th>Communication</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>S1</td>
      <td>Male</td>
      <td>Instrumentation</td>
      <td>Luzon</td>
      <td>58</td>
      <td>89</td>
      <td>75</td>
      <td>78</td>
    </tr>
    <tr>
      <th>1</th>
      <td>S2</td>
      <td>Female</td>
      <td>Communication</td>
      <td>Mindanao</td>
      <td>52</td>
      <td>75</td>
      <td>90</td>
      <td>52</td>
    </tr>
    <tr>
      <th>2</th>
      <td>S3</td>
      <td>Female</td>
      <td>Instrumentation</td>
      <td>Mindanao</td>
      <td>83</td>
      <td>74</td>
      <td>77</td>
      <td>57</td>
    </tr>
    <tr>
      <th>3</th>
      <td>S4</td>
      <td>Male</td>
      <td>Instrumentation</td>
      <td>Visayas</td>
      <td>65</td>
      <td>58</td>
      <td>91</td>
      <td>68</td>
    </tr>
    <tr>
      <th>4</th>
      <td>S5</td>
      <td>Male</td>
      <td>Communication</td>
      <td>Luzon</td>
      <td>59</td>
      <td>86</td>
      <td>43</td>
      <td>88</td>
    </tr>
  </tbody>
</table>
</div>



# Number 1: Creating Data Frames


```python
# Creating table
Vis_df = df[(df['Hometown'] == 'Visayas') & (df['Math'] < 70)]

# Select necessary columns
Vis_df = Vis_df[['Name', 'Gender', 'Track', 'Math']]

# Print table
Vis_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Gender</th>
      <th>Track</th>
      <th>Math</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>S4</td>
      <td>Male</td>
      <td>Instrumentation</td>
      <td>65</td>
    </tr>
    <tr>
      <th>10</th>
      <td>S11</td>
      <td>Female</td>
      <td>Communication</td>
      <td>48</td>
    </tr>
    <tr>
      <th>21</th>
      <td>S22</td>
      <td>Female</td>
      <td>Communication</td>
      <td>64</td>
    </tr>
  </tbody>
</table>
</div>



# a. Instrumentation majors who lives in Luzon


```python
# Create table for Instrumentation majors whose hometown is Luzon, with scores greater than 70
Instru_df = df[(df['Track'] == 'Instrumentation') & (df['Hometown'] == 'Luzon') & (df['Electronics'] > 70)]

# Select necessary columns
Instru_df = Instru_df[['Name', 'GEAS', 'Electronics']]
Instru_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>GEAS</th>
      <th>Electronics</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>S1</td>
      <td>75</td>
      <td>89</td>
    </tr>
    <tr>
      <th>7</th>
      <td>S8</td>
      <td>64</td>
      <td>81</td>
    </tr>
    <tr>
      <th>29</th>
      <td>S30</td>
      <td>57</td>
      <td>81</td>
    </tr>
  </tbody>
</table>
</div>



# b. Mindanaoan female board exam takers


```python
# Create table for female board exam takers whose hometown is Mindanao and an average of >= 55
Mindy_df = df[(df['Hometown'] == 'Mindanao') & (df['Gender'] == 'Female')].copy()

# Getting the average of the scores of Mindanaon, female board exam takers with an average of >= 55
Mindy_df.loc[:, 'Average'] = Mindy_df[['Math', 'GEAS', 'Electronics']].mean(axis = 1)

# Select necessary columns
Mindy_df = Mindy_df[['Name', 'Track', 'Electronics', 'Average']]
Mindy_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Track</th>
      <th>Electronics</th>
      <th>Average</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>S2</td>
      <td>Communication</td>
      <td>75</td>
      <td>72.333333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>S3</td>
      <td>Instrumentation</td>
      <td>74</td>
      <td>78.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>S15</td>
      <td>Microelectronics</td>
      <td>41</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>S17</td>
      <td>Microelectronics</td>
      <td>79</td>
      <td>79.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>S20</td>
      <td>Communication</td>
      <td>60</td>
      <td>60.333333</td>
    </tr>
  </tbody>
</table>
</div>



# Average Grade by Gender


```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (10, 6))

sns.boxplot(x = 'Gender', y = 'Average', data = df)

plt.title('Average Grade by Gender')
plt.xlabel('Gender')
plt.ylabel('Average Grade')

plt.show()
```


    
![png](output_9_0.png)
    


# Average Grade by Track


```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (10, 6))

sns.boxplot(x = 'Track', y = 'Average', data = df)

plt.title('Average Grade by Track')
plt.xlabel('Track')
plt.ylabel('Average Grade')

plt.show()
```


    
![png](output_11_0.png)
    


# Average Grade by Hometown


```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize = (10, 6))

sns.boxplot(x = 'Hometown', y = 'Average', data = df)

plt.title('Average Grade by Hometown')
plt.xlabel('Hometown')
plt.ylabel('Average Grade')

plt.show()
```


    
![png](output_13_0.png)
    

