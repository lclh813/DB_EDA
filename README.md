# Database Creation and Exploratory Analysis
## Notice
It is possible that GitHub fails to display Jupyter Notebooks. Should such circumstances arise, please refer to ***Part 4. Steps*** listed below for code samples.

## Part 1. Objective
There are two datasets to be merged and analyzed altogether with the purpose to help figure out what kind of fruits should be replenished together to further improve retail efficiency in restocking.

## Part 2. Data
### 2.1. Data 1
 | Index  | Store   | Order | Fruit_Name_ID | Fruit_Name         | Qty  |  
 | :---:  | ---     | :---: | ---           | ---                | ---: | 
 |      1 | Store 1 |     1 | APPL001       | Red Delicious      |  100 | 
 |      2 | Store 1 |     2 | APPL002       | Royal Gala         |   50 |  
 |      3 | Store 1 |     3 | GRAP001       | Golden Muscat      |   30 |  
 |      4 | Store 2 |     1 | KIWI001       | Sungold Kiwifruit  |  200 |  
 |      5 | Store 3 |     1 | APPL003       | Fuji               |  150 | 
 |      6 | Store 3 |     2 | GRAP002       | Red Globe          |   80 |  
 |      7 | Store 4 |     1 | APPL002       | Royal Gala         |   20 |  
 |      8 | Store 4 |     2 | APPL003       | Fuji               |   30 |   
  
### 2.2. Data 2
 | Index  | Fruit_Type_ID  | Fruit_Type | 
 | :---:  | :---           | :---       | 
 |      1 | APPL           | Apple      |
 |      2 | GRAP           | Grape      |
 |      3 | KIWI           | Kiwifruit  |
 
### 2.3. Data Processing
- Combine Data1 and Data2 in such a condition that the first 4 letters of ***Fruit_Name_ID*** in Data1 are identical with ***Fruit_Type_ID*** in Data2. 
- Summarize what kind of fruits each store often reorders.

 | Store   | Fruit_Type     |
 | :---:   | :---           |
 | Store 1 | (Apple, Grape) |
 | Store 2 | (Kiwifruit)    |
 | Store 3 | (Apple, Grape) |
 | Store 4 | (Apple)        |

### 2.4. Expected Result
- Count the number of times each distinct element in ***Fruit_Type*** appears.

| Fruit_Type     | Count | Store     | 
| :---           | :---: | :---      |    
| (Apple)        | 1     | Store 4   |
| (Kiwifruit)    | 1     | Store 2   |
| (Apple, Grape) | 2     | Store 1,3 |

## Part 3. Outline
### 3.1. Database Creation   
- Since the number of records exceeds the maximum row size allowed by Excel 2013 which is 1,048,576 rows, it is necessary to build up databases from which data can be extracted and processed efficiently. 
- Tool: ```SQLite```  

### 3.2. Datasets Combining 
- Data merging should be applied since the information from two different datasets are both critical to further analysis.
- Tool: ```SQL``` ```Python```

### 3.3. Data Analysis
- Conduct exploratory data analysis to identify underlying characteristics of the datasets.
- Tool: Python ```Groupby```

### 3.4. Data Visualization
- Present findings in graphical formats to better communicate.    
- Tool: Python ```Matplotlib``` ```Bokeh```

## Part 4. Steps
> [***Complete Code***](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/6_CompleteCode.ipynb)
### Step 1. Preparation 
[1.1. Import Library](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/1_1_ImportLibrary.ipynb)  
[1.2. Set Font Stlye](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/1_2_SetFontStlye.ipynb)  
### Step 2. Create Database 
[2.1. Define Function](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/2_1_DefineFunction.ipynb)  
[2.2. Create Blank Database](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/2_2_CreateBlankDatabase.ipynb)  
[2.3. Import Data into Database](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/2_3_ImportDataIntoDatabase.ipynb)  
### Step 3. Combine Data from Two Databases  
[3.1. Option 1: Combine Data by SQL](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/3_1_JoinDatabaseBySQL.ipynb)  
[3.2. Option 2: Combine Data by Python](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/3_2_JoinDatabaseByPython.ipynb)  
### Step 4. Data Analysis
[4. Conduct Exploratory Data Analysis](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/4_DataAnalysis.ipynb)  
### Step 5. Data Visualization
[5.1. Import Data for Plotting](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/5_1_ImportDataToPlot.ipynb)  
[5.2. Plot Static Bar Chart](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/5_2_StaticBarChart.ipynb)  
5.3. Plot Interactive Bar Chart  
[5.3.1. Interactive Bar Chart: Code](https://nbviewer.jupyter.org/github/lclh813/Database_Exploratory_Analysis/blob/master/5_3_1_InteractiveBarChart.ipynb)  
[5.3.2. Interactive Bar Chart: Chart](https://htmlpreview.github.io/?https://github.com/lclh813/Database_Exploratory_Analysis/blob/master/5_3_2_InteractiveBarChart.html) 

