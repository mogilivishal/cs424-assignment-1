# CS424: Visualization and Visual Analytics - Assignment - 1
## Chicago Traffic Tracker

### Task 1: Data description
The Chicago Traffic Tracker dataset is a comprehensive collection of historical estimated congestion data for over 1,000 traffic segments in Chicago, starting from around March 2018. This dataset is a valuable resource for understanding traffic conditions on the city's arterial streets, and it comprises 275 million rows and 22 columns of attributes. The congestion estimates are generated every 10 minutes by continuously monitoring and analyzing GPS traces received from Chicago Transit Authority (CTA) buses. The dataset provides information on estimated traffic speed, street names, traffic flow direction, segment length, and various other attributes. It also offers congestion estimates at both the segment and regional levels, making it useful for a wide range of applications, including traffic management, urban planning, transportation research, and public transit optimization. Researchers, city planners, traffic engineers, and transportation companies are among the potential users who can leverage this dataset to gain insights into Chicago's traffic patterns and make data-driven decisions to improve traffic flow and urban mobility. 

### Task 2: Domain questions

#### 1. How does congestion vary by time of day and day of the week?
- Reasoning: This question would help us understand the daily and weekly traffic patterns in Chicago. Visualizing the average traffic speed (attribute: SPEED) by hour of the day (attribute: HOUR) and day of the week (attribute: DAY_OF_WEEK) could reveal peak congestion times and highlight differences between weekdays and weekends.

#### 2. Which arterial streets experience the worst congestion?
- Reasoning: By visualizing the congestion levels on different arterial streets (attribute: STREET), we can identify which streets consistently have the highest congestion rates. This information can be valuable for city planners and commuters seeking alternative routes.

#### 3. What is the impact of bus count on congestion?
- Reasoning: Investigating the relationship between the number of buses providing GPS data (attribute: BUS_COUNT) and congestion levels (attribute: SPEED) through visualization can help determine if there's a correlation. It could shed light on how public transit affects traffic flow.

#### 4. What role does the weather play in congestion during Winters and Summers? Are there any trends in different months?
- Reasoning: Exploring congestion patterns during Winters and Summers (attribute: MONTH) can reveal any seasonal variations in traffic. Visualizations can show weather conditions, impact congestion levels (attribute: STREET), helping with traffic management and event planning.

#### 5. Are there specific traffic segments that consistently experience high or low congestion? 
- Reasoning: Heatmaps based on historical congestion data can pinpoint segments with persistent traffic problems, which can be crucial for identifying areas requiring road network improvements (attributes: SEGMENT_ID, SPEED).

#### 6. What is the relationship between segment length (attribute: LENGTH) and traffic congestion? 
- Reasoning: By visualizing congestion levels against the length of traffic segments, it's possible to determine if there is a correlation between the physical length of a road segment and the likelihood of congestion. This can inform decisions about road design, lane expansions, or traffic signal optimization for specific segment types based on their lengths.

#### 7. How did the COVID-19 affect the traffic patterns in the city of Chicago?
- Reasoning: By Visualizing traffic patterns in the years 2019-2020 and 2021-2022. We can determine the traffic congestion levels across different areas of Chicago. We can use a Choropleth map that displays traffic patterns across different areas of Chicago. (attributes: TIME, STREET, SPEED).



### Task 3: Task abstractions


#### 1. Task Type: Analyze Trends over Time 
   - Action: Observe and compare trends.
   - Target: Determine how congestion levels (SPEED) change over time (HOUR and DAY_OF_WEEK).

   - Reasoning: This task involves analyzing trends in congestion patterns, specifically focusing on variations over different times of the day and days of the week. By observing and comparing these trends, users aim to gain insights into peak congestion periods and understand how congestion fluctuates throughout the week.

#### 2. Task Type: Compare Categories – Horizontal Bar Chart,
   - Action: Compare and contrast categories.
   - Target: Identify which arterial streets (STREET) have the highest congestion levels.

   - Reasoning: This task involves comparing different categories (arterial streets) to identify those with the worst congestion. Users are interested in contrasting the congestion levels on various streets to determine which ones consistently experience the highest congestion rates.

#### 3. Task Type: Discover Patterns
   - Action: Identify patterns or relationships.
   - Target: Explore the relationship between the number of buses (BUS_COUNT), Direction (DIRECTION), Segment length(LENGTH) and traffic congestion (SPEED) and its impact on the commuters.

   - Reasoning: This task seeks to discover patterns or relationships between the number of buses providing GPS data and congestion levels. Users want to determine if there is a correlation between bus count, segment length and traffic congestion, potentially indicating the impact of public transit on traffic flow and take alternate routes.

#### 4. Task Type: Investigate Deviation or Distribution
   - Action: Examine deviations or distributions.
   - Target: Explore the distribution of congestion levels (SPEED) across different months (MONTH).

   - Reasoning: This task involves investigating the distribution of congestion levels across different months to identify any seasonal patterns. Users are interested in examining deviations in congestion to understand if certain months exhibit unusual traffic patterns, possibly influenced by factors such as events, or holidays.

#### 5. Task Type: Examine the Relationship Between Segment ID and Congestion:
   - Action: Determine statistical correlation.
   - Target: Determine if there is a correlation between the Segment ID (SEGMENT_ID) and traffic congestion levels (SPEED) to know the congestion levels on different segments.

   - Reasoning: Users aim to establish a statistical relationship to assess the impact of traffic congestion in different segments, helping in transit planning and scheduling.

#### 6. Task Type: Analyze the Relationship Between Segment Length and Congestion and how it helps in City planning.
   - Action: Explore relationships between two variables.
   - Target: Investigate if there is a correlation between the length of road segments (LENGTH) and traffic congestion (SPEED).

   - Reasoning: Users want to understand if longer road segments tend to experience more or less congestion, potentially influencing road design and infrastructure decisions.

#### 7. Task Type: Compare the streets which are congested over two different periods 2020-2021 (COVID period) and 2022-2023
   -  Action: Locate the streets which are congested.
   - Target: Explore the distribution of congestion levels (SPEED) across different  streets (STREET) over the years with COVID restrictions and the years without.

   - Reasoning: Users are interested in identifying streets that experience significant traffic congestion differences between two distinct time periods, one with COVID restrictions (2020-2021) and one without (2022-2023). This analysis is crucial for understanding how traffic patterns have evolved in response to external factors like the pandemic, helping urban planners and policymakers make informed decisions regarding transportation infrastructure, traffic management, and resource allocation.

### Task4: 

#### Domain Question 1: Identify Daily and Weekly Traffic Patterns

1. #### Heatmap of Congestion by Hour and Day:

![image](https://github.com/mogilivishal/cs424-assignment-1/assets/115042657/2a3b6564-ed37-4d48-afd8-9bfdf4fec746)

   - Description: Created a heatmap with the x-axis representing days of the week (attribute: `DAY_OF_WEEK`) and the y-axis showing hours of the day (attribute: `HOUR`). Color intensity can indicate congestion levels (attribute: `SPEED`).
   - Main Idea: This heatmap's main idea is to visualize congestion patterns by representing congestion levels at different hours of the day and days of the week.
   - Rationale: A heatmap is chosen because it can efficiently show variations in congestion intensity throughout the week and day. Color intensity indicates congestion levels, making it intuitive for users.
   - Motivation: The motivation behind this sketch is to help users identify peak congestion times and days to optimize their travel routes and for city planners to make informed decisions.
   - What Worked Well: It effectively highlights peak congestion times and is visually intuitive.
   - What Didn't Work So Well: It can become cluttered with excessive data, and selecting appropriate color scales is critical for clarity.

2. #### Weekly Average Congestion Line Chart:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/cdeb9d68-274d-404b-8733-b20427f5948b)

   - Description: Generated a line chart with the x-axis displaying days of the week and the y-axis representing the average congestion level (attribute: `SPEED`). This chart provides insights into the weekly traffic patterns.
   - Main Idea: This line chart's main idea is to simplify data to showcase the average congestion levels on each day of the week, helping users understand weekly traffic patterns.
   - Rationale: A line chart is chosen to simplify complex data and show trends. Days of the week are on the x-axis, and the average congestion level is on the y-axis.
   - Motivation: The sketch aims to provide a clear overview of weekly congestion trends, helping users plan their commutes and city planners allocate resources.
   - What Worked Well: It simplifies complex data and reveals overall congestion patterns.
   - What Didn't Work So Well: It may not capture variations within each day, and data smoothing is needed to avoid noise.

**Domain Question 2: Locate Highly Congested Streets**

3. #### Choropleth Map of Congestion by Street:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/f4298247-06a8-4030-9a7e-45dc92e658a8)

   - Description: Developed a choropleth map of Chicago streets (attribute: `STREET`) with color-coded segments based on their average congestion levels (attribute: `SPEED`). Lighter colors represent higher congestion.
   - Main Idea: The main idea is to create a choropleth map that highlights streets with the highest average congestion levels, making it easy to identify highly congested areas.
   - Rationale: Choropleth maps are effective for geographical data visualization. Color-coded segments show congestion levels, and darker colors represent higher congestion.
   - Motivation: This sketch aims to pinpoint problematic areas for both commuters and city planners, enabling targeted solutions.
   - What Worked Well: Efficiently identifies highly congested streets.
   - What Didn't Work So Well: Doesn't facilitate direct street-to-street comparisons.

4. #### Bar Chart :

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/1a97e2b9-4812-40d1-bdb0-8bff9cfda88e)

   - Description: Created a bar chart where the x-axis represents street (STREET) and y-axis represents speed (SPEED). This chart tells us the speed or congestion levels in particular streets.
   - Main Idea: The main idea is to create a bar chart that directly lists streets on the x-axis and their corresponding congestion levels on the y-axis.
   - Rationale: A bar chart simplifies the visualization by providing a straightforward view of congestion levels on specific streets.
   - Motivation: This sketch is motivated by the need for a quick and direct overview of congestion on individual streets.
   - What Worked Well: It's easy to understand and identifies congestion on individual streets.
   - What Didn't Work So Well: Lacks the ability to show broader trends or patterns.

**Domain Question 3: Examine Relationship Between Bus Count and Congestion**

5. #### Time Series Plot:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/438470f1-5084-4ce0-9ccb-cb015c6fea2a)

   - Description: Generated a time series plot with the number of buses on the y-axis and the hour of day on the x-axis and color representing the direction. This tells us how many buses (BUS_COUNT) are there in the street during which part of the day (HOUR).
   - Main Idea: The main idea is to generate a time series plot that shows the relationship between the number of buses and the hour of the day, highlighting bus count patterns.
   - Rationale: A time series plot is suitable for showing changes over time. Buses (BUS_COUNT) are on the y-axis, and the hour of the day (HOUR) is on the x-axis.
   - Motivation: This sketch aims to help users understand how bus count varies throughout the day, which is valuable for both commuters and public transportation planners.
   - What Worked Well: Provides insights into bus count patterns.
   - What Didn't Work So Well: May require additional context to explain congestion patterns.

6. #### Hexbin Plot:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/b4902fab-57fa-4866-a97c-f429b923e6e7)

   - Description: Created a hexbin plot to visualize the relationship between bus count (x-axis) and congestion level (y-axis) with size of hexagon representing segment length. This plot groups data points into hexagonal bins, allowing you to see the density of points and any patterns more clearly.
   - Main Idea: The main idea is to create a hexbin plot that groups data points into hexagonal bins to visualize the density and patterns between bus count and congestion level.
   - Rationale: Hexbin plots are effective for revealing point density and patterns in scatter data. It helps overcome issues of overcrowding.
   - Motivation: This sketch is motivated by the need to clearly visualize the relationship between bus count and congestion.
   - What Worked Well: Offers a clearer view of point density.
   - What Didn't Work So Well: May not capture fine-grained details of individual data points.

7. #### Bubble Chart of Bus Count, Congestion, and Segment Length:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/21397787-6d5f-43fd-a95a-1d0108cbd2ce)

   - Description: Created a bubble chart with bus count (x-axis), congestion level (y-axis), and segment length (bubble size). This visualizes the relationships among bus count, congestion, and segment length.
   - Main Idea: The main idea is to create a bubble chart that visualizes relationships among bus count, congestion level, and segment length.
   - Rationale: A bubble chart allows the visualization of multiple variables simultaneously. Bus count (x-axis), congestion level (y-axis), and bubble size (segment length) are used.
   - Motivation: This sketch aims to provide a holistic view of how bus count, congestion, and segment length are interrelated.
   - What Worked Well: Conveys multiple variables simultaneously.
   - What Didn't Work So Well: Can become cluttered with many data points.

**Domain Question 4: Analyze Seasonal Traffic Trends**

8. #### Box Plot of Monthly Congestion:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/09d098e4-3320-441c-9a45-f9c4c96c9a2c)

   - Descrition: Generated a set of box plots, one for each month (attribute: `MONTH`), showing the distribution of congestion levels (attribute: `SPEED`). This helps reveal seasonal variations.
   - Main Idea: The main idea is to generate a set of box plots, one for each month, showing the distribution of congestion levels to reveal seasonal variations.
   - Rationale: Box plots effectively show data distribution. Each box plot represents a month (MONTH), and congestion levels (SPEED) are on the y-axis.
   - Motivation: This sketch aims to highlight seasonal variations in congestion, helping users and city planners anticipate traffic patterns.
   - What Worked Well: Effectively highlights variations within each month.
   - What Didn't Work So Well: Doesn't facilitate direct month-to-month comparisons.

9. #### Seasonal Congestion Stacked Area Chart:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/fd80b51c-8c9f-4e75-9277-d5765961fbea)

   - Description: Created a stacked area chart with time on the x-axis and congestion levels on the y-axis, using different colors to represent different months. This visualizes how congestion varies seasonally.
   - Main Idea: The main idea is to create a stacked area chart with time on the x-axis and congestion levels on the y-axis, using different colors to represent different months, visualizing seasonal congestion variations.
   - Rationale: Stacked area charts are effective for showing changes over time. Colors represent different months (MONTH).
   - Motivation: This sketch aims to provide a visual representation of how congestion varies seasonally.
   - What Worked Well: Enables clear month-to-month comparisons.
   - What Didn't Work So Well: May become complex when representing many months.

**Domain Question 5: Identify Consistently Congested Segments**

10. #### Bar Chart of Top Congested Segments:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/37a8a066-f60f-4532-bc2f-6c5f57f44936)

   - Description: Created a bar chart listing segments (attribute: `SEGMENT_ID`) with the highest average congestion levels (attribute: `SPEED`). This identifies consistently congested segments.
   - Main Idea: This bar chart's main idea is to list the top consistently congested segments (SEGMENT_ID) based on their average congestion levels (SPEED).
   - Rationale: A bar chart is effective for comparing discrete items, in this case, segments. The y-axis represents average congestion levels.
   - Motivation: This sketch is motivated by the need to identify consistently congested segments for potential intervention or optimization.
   - What Worked Well: Efficiently identifies the most congested segments.
   - What Didn't Work So Well: Doesn't provide detailed insights into how congestion varies over time for these segments.

11. #### Bubble Chart:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/8678390f-9353-4709-bd03-627012ca948c)

   - Description: Created a bubble chart where the bubble refers to segment id (SEGMENT_ID) and size of bubble signifies the speed in that particular segment.
   - Main Idea: The main idea is to create a bubble chart where each bubble represents a segment (SEGMENT_ID), and the size of the bubble signifies the congestion speed in that particular segment.
   - Rationale: A bubble chart efficiently visualizes multiple variables. It uses bubble size to represent congestion speed.
   - Motivation: This sketch aims to provide a quick visual overview of congestion in various segments.
   - What Worked Well: Helps identify congested segments quickly.
   - What Didn't Work So Well: May become cluttered with many segments.

12. #### Radar Chart for Top Congested Segments:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/bb8efbf2-c04e-4b82-8972-ecad0a7ea019)

   - Description: Created a radar chart (also known as a spider chart) that displays congestion levels (attribute: SPEED) over time for the top five consistently congested segments (attribute: SEGMENT_ID). Each segment is represented by a separate radar chart, and the axes represent different time points. This visualization allows you to compare congestion patterns among the most congested segments over time.
   - Main Idea: This radar chart (spider chart) displays congestion levels (SPEED) over time for the top five consistently congested segments (SEGMENT_ID). Each segment has a separate radar chart, and the axes represent different time points.
   - Rationale: Radar charts are useful for comparing multivariate data. Each chart represents a segment, and axes represent time points.
   - Motivation: This sketch allows for comparing congestion patterns among the most congested segments over time.
   - What Worked Well: Enables comparison of congestion trends.
   - What Didn't Work So Well: Can become cluttered when more segments are added.

**Domain Question 6: Analyze Relationship Between Segment Length and Congestion**

13. #### Violin Plot:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/6586b4f3-3ae9-47dd-bafd-406e210f64b1)

   - Description: Created a violin plot that combines a box plot and a kernel density estimation, providing a richer view of the distribution of congestion levels (attribute: SPEED) within different segment length ranges (attribute: LENGTH).
   - Main Idea: The main idea is to create a violin plot that combines a box plot and a kernel density estimation to provide a richer view of the distribution of congestion levels (SPEED) within different segment length ranges (LENGTH).
   - Rationale: Violin plots offer a detailed view of data distribution. They are particularly effective for showing variations within categories.
   - Motivation: This sketch aims to provide a comprehensive understanding of how congestion levels vary within different segment length ranges.
   - What Worked Well: Offers a rich view of congestion distribution.
   - What Didn't Work So Well: May not be familiar to all users.

14. #### Scatter Plot:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/f6aa6c4d-5c01-40af-8a2f-8a60f563b46a)

   - Description: Created a scatter plot that has length on x-axis and speed on y-axis. This displays the distribution of congestion levels (attribute: `SPEED`) within each range (attribute: `LENGTH`).
   - Main Idea: The main idea is to create a scatter plot with length on the x-axis and speed on the y-axis, displaying the distribution of congestion levels (SPEED) within each range (LENGTH).
   - Rationale: Scatter plots are efficient for visualizing relationships between two continuous variables. They help understand congestion patterns within each length range.
   - Motivation: This sketch aims to efficiently display congestion levels within segment length ranges.
   - What Worked Well: Provides a clear view of congestion within each range.
   - What Didn't Work So Well: May not capture distribution details as richly as a violin plot.

15. #### Parallel Coordinates Plot:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/a2206371-9ae4-4824-a36b-f6a0fb7be3cb)

   - Description: Used a parallel coordinates plot with segment length (attribute: `LENGTH`) on one axis and congestion level (attribute: `SPEED`) on another. Connect lines to visualize how congestion levels change with different segment lengths.
   - Main Idea: The main idea is to use a parallel coordinates plot with segment length (LENGTH) on one axis and congestion level (SPEED) on another. Connecting lines help visualize how congestion levels change with different segment lengths.
   - Rationale: Parallel coordinates plots are effective for visualizing multivariate data and relationships between variables.
   - Motivation: This sketch aims to highlight how congestion levels change with varying segment lengths.
   - What Worked Well: Effectively shows congestion patterns with different segment lengths.
   - What Didn't Work So Well: May become complex with many segments.

**Domain Question 7: How did the COVID-19 affect the traffic patterns in the city of Chicago?**

16. #### Density Map:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/25cb0e7d-f34c-4a95-85ad-7c306c5b91ef)

   - Description: Developed a map that tells us before and after COVID-19 which streets (STREET) have experienced congestion (SPEED) and which have not.
   - Main Idea: The main idea is to create a density map illustrating changes in congestion before and after COVID-19. It highlights streets (STREET) that experienced congestion (SPEED) and those that did not.
   - Rationale: Density maps provide a clear visual representation of spatial data changes. It helps compare congestion patterns before and after COVID-19.
   - Motivation: This sketch aims to help users understand the impact of the pandemic on traffic congestion in different parts of Chicago.
   - What Worked Well: Offers a clear before-and-after view of pandemic-related changes.
   - What Didn't Work So Well: May not explain the causes of changes.

17. #### Grouped Bar Chart:

![image](https://github.com/uic-cs424/assignment-1-chicagobulls/assets/115042657/5f67269d-473b-4e85-9a85-d5d649e98222)

   - Description: Created a grouped bar chart the first bar represents bus count (BUS_COUNT) and second bar represents the speed (SPEED). This chart tells us the speed and number of buses in a particular month (MONTH).
   - Main Idea: The main idea is to create a grouped bar chart comparing bus count (BUS_COUNT) and speed (SPEED) before and after COVID-19. It provides insights into pandemic-related traffic changes on a monthly basis (MONTH).
   - Rationale: Grouped bar charts effectively compare data across categories. This chart helps users understand changes in bus count and speed over time.
   - Motivation: This sketch aims to visualize specific changes in bus count and speed before and after the pandemic, helping users comprehend the impact.
   - What Worked Well: Efficiently visualizes specific changes over time.
   - What Didn't Work So Well: May not capture all factors influencing traffic patterns during the pandemic.


### Task 5: Summarizing:

The 17 visualization designs presented above offer a variety of strengths and weaknesses in relation to each other and their effectiveness in answering the domain questions:

1. Congestion by Time: The heatmap and weekly average congestion line chart are effective for understanding congestion patterns by time of day and day of the week. Strengths include clarity in showing peak congestion times (Heatmap) and overall trends (Line Chart). However, they might not capture fine-grained details within days (Weakness).

2. Worst Congested Arterial Streets: The choropleth map and bar chart efficiently identify highly congested streets. The strengths lie in pinpointing problematic areas (Choropleth) and providing direct street-level information (Bar Chart). However, the bar chart lacks broader trend insights (Weakness).

3. Bus Count Impact: Time series, hexbin plot, and bubble chart effectively illustrate the relationship between bus count and congestion. They offer insights into bus count patterns (Time Series), point density (Hexbin Plot), and multiple variables (Bubble Chart).

4. Weather and Seasonal Trends: Box plots and seasonal congestion stacked area charts are suitable for analyzing seasonal trends. Box plots reveal variations by month, while stacked area charts visualize month-to-month comparisons. Both provide insights into seasonal variations but may become complex with many months.

5. Consistent Congestion in Segments: Bar charts, bubble charts, and radar charts help identify consistently congested segments. The bar chart is effective in listing top segments, while the bubble chart and radar chart provide insights into congestion patterns over time. However, they can become cluttered with excessive data.

6. Segment Length and Congestion: Violin plots, scatter plots, and parallel coordinates plots explore the relationship between segment length and congestion. Violin plots offer rich distribution insights (Strength) but might be less familiar to users (Weakness). Scatter plots provide a clear view of congestion within length ranges. Parallel coordinates plots effectively show how congestion levels change with different segment lengths but may become complex with many segments.

7. COVID-19 Impact: The density map and grouped bar chart are well-suited for understanding the impact of COVID-19 on traffic patterns. The density map provides a clear before-and-after view (Strength), but it may not explain the causes of changes (Weakness). The grouped bar chart efficiently compares bus count and speed before and after the pandemic, but it may not capture all factors influencing traffic patterns during the pandemic.

In summary, each visualization has its strengths and weaknesses, and their effectiveness in answering the domain questions varies. A combination of these visualizations would be most effective in providing a comprehensive understanding of Chicago's traffic patterns. For instance, combining the heatmap with the weekly average congestion line chart can answer Question 1 effectively, while the density map and grouped bar chart can address the impact of COVID-19 (Question 7).


