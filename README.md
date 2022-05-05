# Cision-Metrics
## Goal 
Tasked with finding the 5 metrics for Cision metrics report Q3. 
Our findings were focused on the KPIS of: TVI, pickup, audience, engagement, and traffic.
Our subcategories included the click-through rate raw numbers. 
## Construction 
Leveraged Python via Jupyter Notebook to build out the necessary dataframes for both bar charts, and the 
'heatmap' scatters. 

## Initial Script
Created cision_data_df to read our provided excel/csv file.
See image below: 
![image](https://user-images.githubusercontent.com/102266450/167041472-6e8ad105-95a5-437c-b925-74d67bdeb47c.png)
The dataframe displayed all rows and columns, included the following of interest: 
  1. Release Headline
  2. Previous Q Average per 5 major KPIS outlined above
  3. Pickup score
  4. TVI score
  5. Audience score
  6. Engagement score
  7. Traffic score
## Format Checks
Then we ran simple count and data type checks on each column of interest, as shown below: 
![image](https://user-images.githubusercontent.com/102266450/167041562-74877183-16ca-4d21-82bf-23056076a2e3.png)
We did notice that some columns, such as "Total Potential Audience" would not be possible map out as it is an 'object' type; whereas most of our data was 'integer' formatting. 
## Dataframes for bar charts
We then completed a simple dataframe for each of the 5 major KPIS
For instance, here is the traffic dataframe: 
![image](https://user-images.githubusercontent.com/102266450/167041686-6c36e0f5-9276-4316-b1ee-1bbdd7d9a785.png)
## Click-Through Overlay 
Next, we built a dataframe to track the click-throughs against our release headlines. 
![image](https://user-images.githubusercontent.com/102266450/167041845-b4c85fbf-cfa8-4aa1-b064-9d58745f320c.png)
Upon creating this, we noticed its importance to be plot against each key metric. 
This led to the creation of the following scatter script: 
![image](https://user-images.githubusercontent.com/102266450/167041902-aa8d5880-81d7-499b-8c0a-914b42022c0a.png)
Our output below, shows that the total visibility index, by release (for Q3) can be matched to the number of clicks. 
Here for instance, a larger scatter bubble represents high numbers of clicks on the news release. 
If look closer, the "Fiscal Second Quarter Financial Results" seems to have an extremely high TVI score and the highest clicks. 
We can also focus on the underperforming bubbles (low clicks) with low TVI scores, which in this case came up as: 
"750 Million covertible notes offering" and "Upcoming Investor Events" news releases. 
This is important to note as we can conclude that if our TVI score is high, then the click-through rate should follow (positive correlation between the two). 
In the next Q, we recommend aiming for strategy around increase the TVI score, to increase clicks, and create more conversations with media. 
![image](https://user-images.githubusercontent.com/102266450/167041917-9e76b534-0fd4-47aa-94e8-1b63ea4ef4dd.png)
## Bar chart construction
For the bar charts, we took the previously created dataframes, and repurposed into the following script: 
![image](https://user-images.githubusercontent.com/102266450/167042386-112ff87d-28e3-4ca9-b45a-cb3406767ce5.png)
## Bar chart outputs
TVI: 
![image](https://user-images.githubusercontent.com/102266450/167042526-8aeed546-7025-4286-b5fe-b99357ee9e5b.png)

Pickup:
![image](https://user-images.githubusercontent.com/102266450/167042554-84b1c4c2-3105-4290-8fa9-dfbd78bd6e88.png)

Traffic: 
![image](https://user-images.githubusercontent.com/102266450/167042566-d6372c17-3686-4ea2-b1a3-0a5d44998a2f.png)

Audience: 
![image](https://user-images.githubusercontent.com/102266450/167042590-6033b513-3b1d-4215-8030-8483fcc411b8.png)

Engagement: 
![image](https://user-images.githubusercontent.com/102266450/167042620-794a5007-950f-443b-b3a5-703fa8e4a8ea.png)
Findings: 
  1. 
