# Cision-Metrics
## Goal 
Tasked with finding the 5 metrics for Cision metrics report Q3. 
Our findings were focused on the KPIS of: TVI, pickup, audience, engagement, and traffic.
Our subcategories included the click-through rate raw numbers. 

## Non-Python Data
Here we used over 1000+ rows of data to construct a quick pivot-chart of the total posts, engagements/engagement rate, and net audience growth over the period of 5 quarters spanning from FY21 Q3 - FY22 Q3. 
![image](https://user-images.githubusercontent.com/102266450/167228914-0e456d46-8d8c-424e-acbb-536933dd4c60.png)
![image](https://user-images.githubusercontent.com/102266450/167228949-21dac464-b1af-407d-92e8-3f30e87a249b.png)


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

## Click-Through Overlay construction
Next, we built a dataframe to track the click-throughs against our release headlines. 
![image](https://user-images.githubusercontent.com/102266450/167041845-b4c85fbf-cfa8-4aa1-b064-9d58745f320c.png)
Upon creating this, we noticed its importance to be plot against each key metric. 

## Click-Through Scatter outputs
This led to the creation of the following scatter script: 
![image](https://user-images.githubusercontent.com/102266450/167041902-aa8d5880-81d7-499b-8c0a-914b42022c0a.png)
  1. Our output below, shows that the total visibility index, by release (for Q3) can be matched to the number of clicks. 
  2. Here for instance, a larger scatter bubble represents high numbers of clicks on the news release. 
  3. If we look closer, the "Fiscal Second Quarter Financial Results" seems to have an extremely high TVI score and the highest clicks. 
  4. We can also focus on the underperforming bubbles (low clicks) with low TVI scores, which in this case came up as: "750 Million covertible notes offering" and "Upcoming Investor Events" news releases. 
  5. This is important to note as we can conclude that if our TVI score is high, then the click-through rate should follow (positive correlation between the two). 
In the next Q, we recommend aiming for strategy around increase the TVI score, to increase clicks, and create more conversations with media. 
![image](https://user-images.githubusercontent.com/102266450/167041917-9e76b534-0fd4-47aa-94e8-1b63ea4ef4dd.png)

## Bar chart construction
For the bar charts, we took the previously created dataframes, and repurposed into the following script: 
![image](https://user-images.githubusercontent.com/102266450/167042386-112ff87d-28e3-4ca9-b45a-cb3406767ce5.png)

## Bar chart outputs
### TVI: 
![image](https://user-images.githubusercontent.com/102266450/167042526-8aeed546-7025-4286-b5fe-b99357ee9e5b.png)
Findings: 
  1. 6 out of 11 releases fell below the industry baseline of a '50' score. 
  2. The top 2 releases were: "Pricing of 750 Million Convertible Notes" and "Fiscal Q2 Financial Results" 
Recommendation: 
  1. For next quarter, we should check the 6 underperforming releases and check for word count, tone, and any other consistent formatting that was NOT found in the top performing releases. 
  2. If we find no key differences in tone/writing style from the low and high performing releases, we then recommend to consider the content types for each release. It seems that financial releases are outperforming event articles, such as the OFC related content. 
  
### Pickup:
![image](https://user-images.githubusercontent.com/102266450/167042554-84b1c4c2-3105-4290-8fa9-dfbd78bd6e88.png)
Findings: 
  1. 11 of 11 releases outperformed the industry standard score of 50; the lowest performing article was set at a pikcup score of 75.
  2. Clearly, we have no points of concern here. We only recommend comparing this to last Q and confirming this is alligned with corporate goals on where these releases are picked up. 

### Traffic: 
![image](https://user-images.githubusercontent.com/102266450/167042566-d6372c17-3686-4ea2-b1a3-0a5d44998a2f.png)
Findings: 
  1. We saw the most variance in scores from one release to next in this KPI. 
  2. Once again, the second release ("750 million convert. notes) performed well above the industry standard. 
  3. "Thought Leaders - OFC" and "Upcoming Investor Events" were 40 points and 36 points below the industry standard of 50, respectively. 
Recommendations: 
  1. From a traffic perspective, we need to ask our Cision partners why the lowest performing articles could not meet industry standards. We are interested in finding why traffic can vary so greatly from month-to-month. 

### Audience: 
![image](https://user-images.githubusercontent.com/102266450/167042590-6033b513-3b1d-4215-8030-8483fcc411b8.png)
Findings: 
  1. We do not make too much of these scores. The 'audience' KPI is the hardest to qauntify on a Q/Q basis. 

### Engagement: 
![image](https://user-images.githubusercontent.com/102266450/167042620-794a5007-950f-443b-b3a5-703fa8e4a8ea.png)
Findings: 
  1. 10 of 11 outperformed the industry standard score of 50 by more than 53%!
  2. Engagement is most nearly tied to clicks, as is the TVI category. Here we are encouraged by nearly all articles as they continue to grow their engagement scores. 
  3. It is important to note that the underperorming article ("") was only 8 points shy of hitting the industry standard to mark. 

## Next Steps 
  1. Confirm with Cision team on script accuracy. 
  2. Set strategy according to KPIS over Q/Q historical data. We are increasingly seeing the trend of lackluster results in traffic, while still maintining high scores in total visibility and engagement. 
 
