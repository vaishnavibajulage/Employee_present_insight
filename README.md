# Employee_present_insight

# Employee_present_insight
Credit Card Transaction and Customer Dashboard using Power BI

# Employee_present_insight


### Dashboard Link :https://github.com/vaishnavibajulage/Employee_present_insight/blob/main/HR%20Data.pbix
## Problem Statement

Gain real-time insights into workforce attendance dynamics with our comprehensive dashboard. Monitor and analyze all leave types, including WFH, sick leave, and half-day sick leave. Understand the reasons behind each absence, whether it's remote work preferences or health-related concerns. Armed with actionable insights, optimize attendance management strategies to foster a productive and engaged workforce, ultimately driving organizational success

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 10293 rows so you need to select "column profiling based on entire dataset".
- Step 4 : In the report view, under the insert tab, One text boxe added to the canvas, in that  "Employee Prasent insights"  was mentioned .
 
 
- Step 5 :Enhance your dashboard with a month and year slicer for concise filtering. Select specific month and year effortlessly to focus on targeted data analysis and trend monitoring. Boost efficiency and streamline insights with this intuitive navigation feature.

![Snapshort 1](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/6c591aae-ec4b-4252-a19d-88b09e9e59d6)

- Step 6 : Calculated column was created where how many employees are working from home


for creating new column following DAX expression was written;
       

* WFH = SWITCH(TRUE(), 'Find data'[Value] = "wFH",1,'Find data'[Value]="HWFH",0.5,0)

 Step 7 : Calculated column was created where how many employees are Taking sick leaves .

  *SL count = SWITCH(TRUE(),
   'Find data'[Value] = "SL",1,
   'Find data'[Value]="HSL",0.5,0)

        
- Step 8 : New measure was created to find Employee prasence

Following DAX expression was written for the same,
        
* presence% = DIVIDE([prasent days],[Total Working days],0

![Snap short 1](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/2f5d628b-9491-44c9-9d43-d0c1866aa5b8)

-Step 9 : New measure was created to find How many Employee took WFH

Following DAX expression was written for the same,

* WFH % = DIVIDE([WFH count],[prasent days],0)

![Snapshort 2](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/70730fbb-34df-478a-8abb-ef62bcb10b6f)

-Step 10 : New measure was created to find How many Employee took sick leave

Following DAX expression was written for the same,

* SL count = SWITCH(TRUE(),
 'Find data'[Value] = "SL",1,
  'Find data'[Value]="HSL",0.5,0)

![Snapshort 3](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/bf8955ac-b45d-47bb-97af-953509423ff6)



Step 11 : Defined stack area chart to observe how many Employees are prasent by date

![Snap short](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/b421c813-81a6-43da-a7d4-60c3a379d484)

Step 1 : Defined stack area chart to observe how many Employees are taking WFH by date

![Snapshort](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/e770657d-5708-4ece-8e7d-5746f52efe70)

Step 13 : Defined stack area chart to observe how many Employees are taking SL by Qtr ,Month,day

![snapshort](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/36942aa4-86de-49e8-ad3e-81bfc0ef5e39)

# Snapshot of Dashboard (Power BI Service)
![Dashboard](https://github.com/vaishnavibajulage/Employee_present_insight/assets/83158414/262d00c2-4fb8-4dd7-b5ba-698631e79197)

# Insights

A Double page report was created on Power BI Desktop 

Following inferences can be drawn from the dashboard;

### [1] Total Employee prasence days = 92%

Number of Employee who choosen WFH = 11.15%

Number of Employee who took sick leave = 1,08%

- Here people prasent mostly on MON and Tue more compare to other week days

-Here employees Taking WFh Mon,thu comapre to other week days

-sick leave is also taken by so many employees from monday
- In table visual you can see perticulat=r employee how many times he is taking leaves and hes prasent and he is taking wfh 

And In another table you can see on which day he took leave,and wfh or he is prasent
