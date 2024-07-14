# Analysing  Customers Churn in Excel
## Table of content 
- [Project Overview](project-overview)
- [Data preparation](data-preparation)
- [Results](results)
- [Recommendation](recommendation)

## Project Overview 

 Analysing churn doesn’t just mean knowing the churn rate: it’s also about figuring out why
 customers are churning at the rate they are and how to reduce churn. You'll answer these
 questions by creating calculated columns and fields, building PivotTables, and creating an
 eye-catching dashboard.

 
 ## Data preparation
 
  Before you do any analysis, the first step is to ensure that your data is prepared. First, we'll
 verify the data with a simple check- in this exercise you'll put your data in a table formats
 and then investigate whether there are any duplicate rows in our customer level data.
 In this case study, you'll be working with two different datasets in the following worksheets:
 Databel- Aggregate and Databel- Customer. For chapter 1 we'll focus on our customer level
 data before working with aggregate data later in the case study. The aggregate views are
 based on data in Databel- Customer.
 - Open the workbook called 1_1_data_preparation.xlsx from the Workbooks folder.
 -  Navigate to Databel- Aggregate and convert the range of data ($A$1:$U$6670) into a
 tabular format.
 - Rename this table "Aggregate".
 -  Navigate to Databel- Customer and convert the range of data ($A$1:$AC$6688) into
 a tabular format.
 -  Rename this table "Customers".
 -  Identify whether there are any duplicate values in the Customers table, there are two
 approaches that you can use:
 -  Removeduplicates feature
 -  Conditional formatting
   
 ### Calculating churn
 
  It will be extremely useful to have a measure that calculates churn before deep-diving into the analysis.There is a column called Churn Label that indicates "Yes" or "No", but this column isn't the easiest to work with. You'll convert this column to a binomial column indicating if the customer churned or not.You need to use that to calculate the churn rate.
 - Create a new column "Churned" in our Customers table that uses an IF() to convert the
 values in Churn Label based on the following criteria:
 ● "Yes"then 1
 ● "No"then O
 -  Create a blank PivotTable of the Customers table and place it in a new Worksheet. Rename this worksheet "Customer Pivots".
 -  In the PivotTable, display the total count of customers and number of churned customers.
 -  uppdate the column headers to user-friendly names such as "Total Customers" and "Churned Customers".
 -  Great! Now we can easily identify how many customers have churned, but what if we want to find out what our churn rate is?
 -  Next to your PivotTable, create a new calculation with the header "Churn Rate" that divides churned customers by total customers.
 -  Format this as a % to two decimal places.
   
 ### Investigating churn reasons
 
 The logical next step is to investigate the different reasons why customers churned. Your job
 is to create a column chart listing the different reasons why customers churn.
 1. Create a blank PivotTable of the Customers table in the Customer Pivots worksheet.
 2. Analyse the total number of churned customers by Churn Reason.
 3. Rename the row header to "Churn Reason" and the column header to "Churned
 Customers".
 4. Order the churn reasons ascending, to the most popular churn reason appears at the
 bottom .
 5. Showthe Churned Customers as a "% of Grand Total".
 6. Visualise your analysis with a 2D Bar Chart and title it "Churn Reasons".
 7. Hide all field buttons on the chart and delete the Legend .
    
 ### Digging deeper into churn categories
 Churn Reasons are grouped together in the Churn Category column. It's your job to identify
 which churn category is accounting for the highest proportion of churn and understand which
 priority we should tackle first based on the churn reason.
 1. Create a blank PivotTable of the Customers table in the Customer Pivots worksheet.
 2. Analyse the total number of churned customers as % of grand total by Churn
 Category and Churn Reason.
 3. Rename the row header to "Churn Reason" and the column header to "Churned
 Customers".
4. Wecansee that category driving the highest % of churn is Competitor.
 5. Filter the PivotTable to only include this churn category.
 6. Create a visualisation of your choice to display the Churned Customers PivotTable
 you created and name it "Competitor Churn Analysis".
 7. Clean this visual up by removing unnecessary components such as field buttons and
 apply any style customizations.

 ### Analysing demographics
 In this exercise, you are tasked with analysing the different demographic fields from the
 dataset. You'll be using your Excel skills to create a new field to analyse the data with and
 create your first calculated field in a PivotTable.
 1. Navigate to Databel- Aggregate sheet.
 2. We'd like to get further insight into the demographic variables relating to age.
 ● Create a new column "Demographics" next to the Group column using a nested IF()
 formulas that categorises customers into the following categories: "Under 30",
 "Senior" and "Other"
 3. Create a blank PivotTable of the Aggregate table and place it in a new Worksheet.
 Rename this worksheet "Churn Analysis".
 4. In the PivotTable:
 ● Create a calculated field "Churn Rate %" that divides churned customers by total
 customers, then add it to the PivotTable.
 ● Format the calculated field as a % to two decimal places.
 We'll be able to re-use this calculated field throughout our analysis.

 ### Age groups
 Good job on the previous exercise! You found a great insight that senior citizens churn more
 often. This suggests that it might be a good idea to analyze the customer age in general. Your
 job is to create different age bins and make a combo chart visualizing the number of
 customers per bracket and their respective churn rates.
 ● Create a copy of the PivotTable from the previous exercise in the Churn Analysis
 sheet.
 ● Replace Demographics with Age in Rows and add Total Customers to Values.
 ● Create groups for Age with a split of 10.
 ● Create a line and clustered column chart that shows the number of customers and
 churn rate for every age bracket.
 ● Format your chart and make the graph visually appealing.
 
 ### Unlimited plan
 
Databel has a hypothesis that people who are not on an unlimited data plan are more likely to
 churn. Your task is to investigate how the Unlimited Data Plan influences the churn rate.
 1. Create a PivotTable in Churn Analysis based on the Aggregate table that analyses the
 total number of customers who have an unlimited data plan, as well as the churn rate.
 2. It appears that customers who are on an unlimited plan are more likely to churn. To
 see if it is related to a certain amount of mobile data (GB) being used, create a new
 column in Databel- Aggregate called Grouped Consumption that classifies the
 average monthly GB download in the following groups:
 ● Lessthan 5 GB.
 ● Between 5and 10 GB.
 ● 10ormoreGB.
 3. Refresh your PivotTable and re-arrange your table to analyze churn rate by Unlimited
 Data Plan and Grouped Consumption.
 4. Create a stacked bar or column chart to visualize Churn Rate by Unlimited Data Plan
 and broken out by average consumption levels.
 5. Format your chart and make the graph visually appealing.
  
 ### International calls
 
 The analysis requirement given by Databel includes a request to analyze the relationship
 between customers' international activity and churn. They are curious about the behavior of
 customers who call internationally, and if paying for an international plan influences their
 loyalty.
 1. Create a PivotTable in Churn Analysis based on the Aggregate table that displays a
 matrix of churn rate by State and whether a customer is on an Intl Plan
 2. Remove grand-totals from the PivotTable.
 3. Apply a Red- Yellow- Green colour scale on the churn rate values within the
 PivotTable
 Contract type
 Databel also wants to improve its customer service since there have been some reported
 issues. Your job is to investigate two important topics related to customers: the contract type,
 and how many months a person is a customer.
 1. Create a PivotTable in Churn Analysis based on the Aggregate table that displays
 churn rate based on the customers account length.
 ● RemoveGrandTotals from the PivotTable.
 ● Create groups for Account Length (in months) with a split of 12.
 ● It seems the churn rate does decrease over time. Now, investigate how this decrease
 behaves through the different types of contracts.

 ### Overview- Adding KPIs
 
Now that we've created a series of visuals and pivot tables, we need to collate this
 information to provide the best insights possible to address any key concerns around churn.
 In this exercise, we'll start by preparing our dashboard sheet to display key information such
 as total customers, number of churned customers and churn rate.
 1. Create the following headers in cells B2, C2 and D2:
 ● Total Customers
 ● Churned Customers
 ● ChurnRate %
 2. Under each header input the KPIs from your Customer Analysis that you completed
 in Chapter 1. You can use cell references or manually enter the data in.
 3. Apply formatting and styling to your KPIs to make them visually appealing.
    
 ### Overview- Adding churn reasons
 Great work! We've added the first key data points in our overview page. Now let's add some
 context into why our customers are churning with a particular focus on customers who churn
 as a result of our competitors' activities.
 1. You've visualized your KPIs and highlighted issues around churn, so let's provide
 some detail as to why customers are churning.
 ● Add a visualization that shows the breakdown of churn rate based on the reason
 customers provided
 2. Since competitor gets highlighted a lot in our previous visual, let's focus on this
 category.
 ● Add a visualization that shows a filtered view of Churn Category based on
 'Competitor' with Churn Rate % and Churn Reason visible.
 3. Apply formatting and styling to your visuals for consistent branding with your KPIs.
    
 ### Overview- Adding demographics
 Our dashboard is looking great so far! Now let's provide some context into the demographics
 of our churned customers to help the business understand what customers we need to
 prioritize our retention efforts.
 ● Create a visualization of your choice to display the Churn Rate of the Demographic
 groups. You can use the PivotTable you created earlier to achieve this.
 ● Clean this visual up by removing unnecessary components such as field buttons and
 apply any style customizations.
 ● Addthenewvisualization you created to your Overview page.
 ● Add a visualization that shows the breakdown of customers and churn rate based on
 age ranges.
● Apply formatting and styling to your visuals for consistent branding with your
 dashboard.
 
 ### Overview- Adding consumption
 We're almost finished! We now need to add the finishing touches by including our
 consumption data.
 1. Add a visualisation that shows the breakdown of churn based on the average amount
 of data the customer uses.
 2. Apply formatting and styling to your visuals for consistent branding with your
 dashboard.
 3. Create a copy of the table matrix that displays churn rate by state and international
 plan into the Overview page.
 4. Update the PivotTable with a filter to only include those on an international plan.
 5. Sort the PivotTable by highest to lowest churn rate.
 6. Apply a value filter that only displays the top 25 states based on the highest churn
 rate.

## Results 
Key Findings:
Total Customers and Churn Rate:
Total Customers: 6687
Churned Customers: 1796
Churn Rate: 26.86%
 - Churn Reasons:The top reasons for customer churn include competitors offering better deals, issues with support personnel, and dissatisfaction with the product or services.
 - Competitor Churn Analysis:A significant portion of customers churn due to competitors offering higher download speeds, more data, better devices, or better offers.
 - Age Demographics:The largest segment of churned customers are seniors (44%), followed by those under 30 (27%).The churn rate varies across different age groups, with higher churn rates among older customers.
 - State-wise Churn Rates:There is significant variation in churn rates across different states, with some states like LA, NH, and MS having particularly high churn rates.
 - Usage Patterns:Customers with different usage levels (10 or more GB, 5-10 GB, less than 5 GB) have varying churn rates, with a noticeable trend indicating that lower usage correlates with higher churn rates.
   
## Recommendations:
 - Enhance Competitiveness:Offer Better Deals: To counter competitors, consider offering more attractive deals, such as higher download speeds, more data, or bundled services.
 - Device Incentives: Provide incentives for upgrading to better devices, which can improve customer satisfaction and reduce churn.
 - Improve Customer Support
 - Training Programs: Invest in training programs for support personnel to enhance their interaction skills and resolve issues more effectively.
 - Feedback Mechanism: Implement a robust feedback mechanism to identify and address support-related issues promptly.
 - Targeted Marketing and Retention Strategies  
 - Senior-Friendly Services: Develop and market services that cater specifically to senior customers, such as simplified user interfaces and customer service options tailored to their needs.
 - Youth Engagement: Engage younger customers through digital channels, social media, and promotions that resonate with their preferences and lifestyle.
 - Regional Strategies 
 - State-Specific Campaigns: Conduct detailed analysis to understand why certain states have higher churn rates and develop targeted campaigns to address specific issues in those regions.
 - Localized Offers: Consider localized offers and promotions that cater to the specific needs and preferences of customers in high-churn states.
 - Usage-Based Retention Programs
 - Incentivize Higher Usage: Develop programs that encourage higher usage through rewards and loyalty programs, particularly targeting low-usage customers.
 - Usage Monitoring: Monitor usage patterns and proactively engage with customers who show signs of reduced usage to prevent churn.
 - Product Improvements
 - Service Range Expansion: Expand the range of services offered to cover any gaps that might be causing dissatisfaction.
 - Quality Assurance: Continuously monitor and improve the quality of products and services to ensure customer satisfaction and loyalty.
