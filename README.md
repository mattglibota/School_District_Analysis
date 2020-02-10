# School District Analysis
## Comparison

### District Summary
* Percentage passing rate for math, reading and overall decreased by one-point, average math score dropped by 0.1

### School Summary
* Percentage passing rate for math, reading and overall at Thomas High School dropped significantly from 93 – 67 for math, 97 to 70 for reading, and 91 to 65 for overall. 
* Because of the invalid scores of 9th graders, the average math and reading score changed by less than 1 percentage point. The drop in passing but virtually unchanged scores is because NaN is not included in averages, but it is counted as a fail.

### Performance relative to other schools
* Thomas High School went from being 2nd highest school in terms of overall passing percentage down to 9th. It is the worst Charter school and remains higher than all District schools.

### How does replacing scores affect
* It makes all of Thomas High School’s 9th grade scores N/A which counts as a “fail” by our metrics. 
* Thomas High School belonged to the spending range $630 to 644 and the invalidated test scores reduced passing percentages for that range from 73 to 66 for math, 84 to 77 for reading, and 63 to 56 for overall. 
* Thomas High School is a Medium school size and the invalidated test scores reduced passing percentages for that size from 94 to 88 for math, 97 to 91 for reading, and 91 to 85 for overall. 
* Thomas High School is a Charter school type and the invalidated test scores reduced passing percentages for that size from 94 to 90 for math, 97 to 93 for reading, and 90 to 87 for overall.

### Notes
* Reported numbers are rounded to whole numbers for simplicity purposes. Formatting was avoiding in final analysis because formatting changed datatypes to string from floats. 
* Main change to the challenge assignment was addition of following code before the DataFrame merge

`student_data_df.loc[(student_data_df["grade"]=="9th") & (student_data_df["school_name"] == "Thomas High School"), ["reading_score","math_score"]] = np.nan`
* All DataFrames are output again at the end of the Jupyter Notebook.

### Challenge
