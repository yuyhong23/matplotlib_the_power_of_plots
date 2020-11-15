# Matplotlib Challenge - The Power of Plots

Data and instructions provided by UC Berkeley Extension Data Analytics Bootcamp.

# Introduction 

The goal of this assignment is to use my newfound Matplotlib knowledge and skills to create various graphs and plots from data imported from a csv file.

# Technologies

- Matplotlib

- Python Pandas

- Jupyter Notebook
  - (file:///Users/yyh/Downloads/pymaceuticals_jupyter_notebook.html) for a html format view of the notebook.
  
- Conda Environment used: PythonData

# Detailed Instructions/Assignment Background

  ### Pymaceuticals

  What good is data without a good plot to tell the story?
  
  So, let's take what you've learned about Python Matplotlib and apply it to a real-world situation and dataset:
  
   - While your data companions rushed off to jobs in finance and government, you remained adamant that science was the way for you. Staying true to your mission, you've joined Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.
    
   - As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. You have been tasked by the executive team to generate all of the tables and figures needed for the technical report of the study. The executive team also has asked for a top-level summary of the study results.

# Files
  
  The Pymaceuticals  folder contains:
  
    - The jupyter notebook where my codes are for creating dataframes and plots/graphs based on the csv file (observations/inferences are at the beginning of the notebook)
    
    - The data folder where the csv file is store

# Process and Credits

My first assignment using Matplotlib to create insightful plots and graphs from a csv file (data). I used class materials and outside resources for references, asked Bootcamp's Learning Assistant App for help to complete this assignment.

1. When I was trying to merge the newly created last timepoint with the original dataframe to identify the tumor volume at the last time point for the quartiles, outliers and boxplots section, I overcomplicated things by trying to first match the last timepoint values with the original timepoint, and from there to drop the values that don't match. I even used numpy.where during this attempt (https://www.kite.com/python/answers/how-to-compare-two-pandas-dataframe-columns-in-python as reference), but at the end, I ran into a dead end and couldn't proceed. So I asked for Learning Assistant's help, where I was reminded that I could have just done merge(how="left"). I couldn't believe how convenient and useful that function can be! At least I learned in what situation I can use how="left" now.

2. When I was trying to determine the outliers in the same section, I also got stuck trying to have the outliers print out. So I aksed Learning Assistant for guidance again. The learning assistant pointed that out I should have created a key for holding "last_timepoint_tumor.loc[last_timepoint_tumor["Drug Regimen"] == regimen,"Tumor Volume (mm3)"]" instead of using that directly to compare with the lower and upper bound (which didn't worked out). In addition, I was reminded to create a list key to hold the tumor volumes from each iteration of the regimen. At first, I was kind of lost as to what list key I am supposed to created. It became clear to me as I work on creating the boxplots.

Here are the outside resources I used for this assignment (as well as attempts):
  - https://www.codegrepper.com/code-examples/python/find+duplicated+rows+with+respect+to+multiple+columns+pandas
  - https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/03_subset_data.html
  - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sem.html
  - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.duplicated.html
  - https://pandas.pydata.org/pandas-docs/stable/user_guide/groupby.html
  - https://www.analyticsvidhya.com/blog/2020/03/groupby-pandas-aggregating-data-python/
  - https://pandas.pydata.org/pandas-docs/stable/user_guide/groupby.html#applying-multiple-functions-at-once
  - https://www.kite.com/python/answers/how-to-count-unique-values-in-a-pandas-dataframe-group-in-python
  - https://www.datasciencemadesimple.com/bar-plot-bar-chart-in-python-legend-using-matplotlib/
  - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.plot.pie.html
  - https://kanoki.org/2019/09/16/dataframe-visualization-with-pandas-plot/
  - https://dfrieds.com/data-visualizations/style-plots-python-matplotlib.html
  - https://thispointer.com/pandas-find-duplicate-rows-in-a-dataframe-based-on-all-or-selected-columns-using-dataframe-duplicated-in-python/
  - https://www.shanelynn.ie/using-pandas-dataframe-creating-editing-viewing-data-in-python/
  - https://stackoverflow.com/questions/48000487/how-to-use-agg-method-to-calculate-the-column-average-in-pandas
  - https://www.kite.com/python/answers/how-to-compare-two-pandas-dataframe-columns-in-python
  - https://stackoverflow.com/questions/15834244/how-to-map-multiple-lists-to-one-dictionary
  - https://stackoverflow.com/questions/209840/convert-two-lists-into-a-dictionary
  - https://stackoverflow.com/questions/43342564/flier-colors-in-boxplot-with-matplotlib
  - http://blog.bharatbhole.com/creating-boxplots-with-matplotlib/
  
