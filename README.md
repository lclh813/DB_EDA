# Project: DB_EDA

## Part 1. Objective
There are two datasets to be merged and analyzed altogether with the purpose to help fugure out what kind of fruits should be ordered together to further improve retail efficiency in restocking.

## Part 2. Data
### 2.1. Data1
 | Index  | Store   | Order | Fruit Name ID | Fruit Name         | Qty  |  
 | :---:  | ---     | :---: | ---           | ---                | ---: | 
 |      1 | Store 1 |     1 | APPL001       | Red Delicious      |  100 | 
 |      2 | Store 1 |     2 | APPL002       | Royal Gala         |   50 |  
 |      3 | Store 1 |     3 | GRAP001       | Golden Muscat      |   30 |  
 |      4 | Store 2 |     1 | KIWI001       | Sungold Kiwifruit  |  200 |  
 |      5 | Store 3 |     1 | APPL003       | Fuji               |  150 | 
 |      6 | Store 3 |     2 | GRAP002       | Red Globe          |   80 |  
 |      7 | Store 4 |     1 | APPL002       | Royal Gala         |   20 |  
 |      8 | Store 4 |     2 | APPL003       | Fuji               |   30 |   
  
### 2.2. Data2 
 | Index  | Fruit Type ID  | Fruit Type | 
 | :---:  | :---           | :---       | 
 |      1 | APPL           | Apple      |
 |      2 | KIWI           | Kiwifruit  |
 |      3 | GRAP           | Grape      |
 
### 2.3. Data Processing
- Combine Data1 and Data2 in such a condition that first 4 letters of "fruit Name ID" in Data1 are identical with "Fruit Type ID" in Data2. 
- Summarize what kind of fruits are often reordered by each store.

 | Store   | Fruit Type     |
 | :---:   | :---           |
 | Store 1 | (Apple, Grape) |
 | Store 2 | (Kiwifruit)    |
 | Store 3 | (Apple, Grape) |
 | Store 4 | (Apple)        |

### 2.4. Expected Result
- Assign unique value to each "Fruit Type" and count the number of times each distinct element in "Fruit Type" appears.

 | Furit Number | Fruit Type     | Count | Store     | 
 | :---:        | :---           | :---: | :---:     |    
 | 1            | (Apple)        | 1     | Store 4   |
 | 1            | (Kiwifruit)    | 1     | Store 2   |
 | 2            | (Apple, Grape) | 2     | Store 1,3 |

## Part 3. Outline
### 3.1. Database Creation   
- Since the number of records exceeds the maximum row size allowed by Excel 2013 which is 1,048,576 rows, it is necessary to build up databases from which data can be extracted and processed efficiently. 
- Tool: SQLite  

### 3.2. Datasets Combining 
- Data merging should be applied since the information from two different datasets are both critical to further analysis.
- Tool: SQL, Python

### 3.3. Data Analysis
- Conduct exploratory data analysis to identify underlying characteristics of the datasets.
- Tool: Python Groupby

### 3.4. Data Visualization
- Present findings in graphical formats to better communicate.    
- Tool: Python Matplotlib, Bokeh

## Part 4. Steps
### Step 1. Preparation 
[1.1. Import Library](https://github.com/lclh813/Database/blob/master/1_1_ImportLibrary.ipynb)  
[1.2. Set Font Stlye](https://github.com/lclh813/Database/blob/master/1_2_SetFontStlye.ipynb)  
### Step 2. Create Database 
[2.1. Define Function](https://github.com/lclh813/Database/blob/master/2_1_DefineFunction.ipynb)  
[2.2. Create Blank Database](https://github.com/lclh813/Database/blob/master/2_2_CreateBlankDatabase.ipynb)  
[2.3. Import Data into Database](https://github.com/lclh813/Database/blob/master/2_3_ImportDataIntoDatabase.ipynb)  
### Step 3. Combine Data from Two Databases  
[3.1. Option 1: Combine Data by SQL](https://github.com/lclh813/Database/blob/master/3_1_JoinDatabaseBySQL.ipynb)  
[3.2. Option 2: Combine Data by Python](https://github.com/lclh813/Database/blob/master/3_2_JoinDatabaseByPython.ipynb)  
### Step 4. Data Analysis
[4. Conduct Exploratory Data Analysis](https://github.com/lclh813/Database/blob/master/4_DataAnalysis.ipynb)  
### Step 5. Data Visualization
[5.1. Import Data for Plotting](https://github.com/lclh813/Database/blob/master/5_1_ImportDataToPlot.ipynb)  
[5.2. Plot Static Bar Chart](https://github.com/lclh813/Database/blob/master/5_2_StaticBarChart.ipynb)  
5.3. Plot Interactive Bar Chart  
[5.3.1. Interactive Bar Chart: Code](https://github.com/lclh813/Database/blob/master/5_3_1_InteractiveBarChart.ipynb)  
[5.3.2. Interactive Bar Chart: Chart](https://htmlpreview.github.io/?https://github.com/lclh813/Database/blob/master/5_3_2_InteractiveBarChart.html)  

