Criteria hey
- M1 (Individual)
    - The Distinction criteria hold, and all the code is **well-documented** and **clear**, and each provides the **overall aggregate** as well as the **aggregate of each group**.
    - Every member has written Python code that correctly computes some **grouped-aggregate** where the grouping is based on a **nominal attribute** of the data, and each member has written Python code that correctly calculates some **grouped aggregate** where the grouping is based on a **binned quantitative attribute**. All the code pieces are distinct from one another.

- M2 (Individual)
    - The Distinction criteria holds, and also there is at least **one chart** which illuminates connections that involve **at least four aspects or attributes** of the data that are relevant to the question, and where there is a **reasonable expectation of a relationship** where **all four attributes interact** together [not just that each pair are related, but that the way in which any two relate, is impacted by the values of the other two!]. This chart must be **compelling** in communicating the information to the reader (e.g. it draws the reader to easily gain a deep awareness of the patterns, especially how the relationship of some are impacted by the other attributes) and makes them keen to learn more.
    - Each member produces **at least two charts** that accurately convey the relationship between aspects or attributes from their data that are relevant to the topic. For each member, **at least one chart** must show information about **at least three aspects or attributes**. For each member, **at least one of the aspects** shown among their charts must be **nominal or ordinal** and **at least one attribute** (possibly in a different chart) must be **quantitative**. All the charts in the report must be distinct from one another, and **without serious flaws** (such as distortion or misleading or missing crucial information such as axis scales).
- M3 (Individual)
    - The Distinction criteria hold, and, for each chart, there are **good reflections** on how well (or not) the chart design would work **if much more data is obtained**.
    - Every member has written an **evaluation** for each chart in their section, which correctly documents the **encoding between data attributes and visual attributes**, and **documents other decisions** (such as style of chart, scale etc.), and it sensibly **justifies the decisions** in view of the effectiveness of communication. All the charts in the report must be distinct from one another.
- M4 (Group)
    - The Conclusion section has all the Distinction criteria, and discusses honestly and with insight, **the limitations**, and **uncertainties** about the results.
    - The Conclusion section provides some accurate information which provides **insight into important issues** in the topic, **supported** by **at least four relevant tables** and **at least four relevant charts**; the tables and charts must include something **produced by each member of the group** in their sections of the report.
- M5 
    - The Conclusion section has all the Distinction criteria, and it draws the reader in and engages their attention with vivid and stylish prose.
    - The Conclusion section makes it easy for the intended audience to gain understanding they seek. It clearly links to the readers’ background and aims. The structure needs to be logical and well-organised, (for example, tables, charts, and text relate well to one another). It makes explicit what has been learned and aspects which have not been resolved.

Criteria TL;DR
- M1: Calculate Group Aggregates for tables ...
- M2: Produce Charts ...
- M3: Evaluate effectiveness of charts for communications ...
- M4: Derive conclusions from charts and tables ...
- M5: Write good in general ...

Deliverables
- Report
    1. There is an initial section which briefly states the topic of interest, and the stakeholders who care about this. This is not marked as such, it is just so the marker can understand the setting for the rest of the report. (max 1 page)
    2. There should be one section for each member (the section should state the SID/unikey of the group member who did the work reported in this section). In this section, there should be some subsections. (max 4 pages per member)
        - a. A brief description of the dataset being used by this member; showing at least the schema of the dataset. You do not need here to describe the provenance or give a detailed data dictionary. This is not marked as such, it is just so the marker can understand the tables and charts that follow.
        - b. One or more subsections, each giving a grouped-aggregate summary. In any subsection, you should show the Python code that calculates a summary, followed by a table that presents the output of that summary.
        - c. One or more subsections, each giving a chart. In any subsection, you should describe how you produced the chart, followed by a display of the chart, followed by an evaluation of the effectiveness of the chart. If the chart was produced by Python, the description of how you produced it is the relevant Python code; if you used a spreadsheet to produce the chart, you should state in words the actions you took when creating the chart.
    3. If the group is seeking full marks for Chart Production, there will be an extra section, with a chart which shows four attributes and their relationships. This chart may be produced jointly, or by any individual member. (if produced jointly, max 4 pages; if individual, max 2 pages per individual)
    4. This section is jointly written by the group. It is written for readers who are interested in the general topic that you have investigated. In it, you describe the specific issue that you have been investigating, and you present some conclusions or insights about this, which you reached from your analysis. You should include some tables and charts (derived from the data and chosen from among those calculated by the members and reported in Part A), to justify or illustrate the conclusions you give
- Data and Code
    - Dataset
        - the provenance of the data
        - any licence or other restrictions on use of the data
        - description of all the changes you did between the original datasets and the final dataset; and
        - the meaning of each attribute, what format or units are used, etc.
    - Code for Summaries
    - Code for Charts

Plan
- For report Part 1, we can more or less paraphrase the section 1 of our report or just insert excerpt and self cite to avoid plagiarism. Let's try and focus the question to be something along the lines of "Evaluate the impact of the ENSO system, via the ENSO influences on Australian weather, on the Australian agricultural sector."
- For report Part 2 we have
    - Nathan
        - Summaries
        - Chart
    - Oscar
        - Summaries
            - Group by nominal:
                - Group by ENSO cycle and ABARES category, then find the mean of each
            - Group by ordinal:
                -  Group by binned rainfall and CPI category, then find the mean of each
        - Chart
            - Chart A: 3 attributes
                - Box Plot
                - ABARES category (x-axis), production value (y-axis), ENSO event (colour)
            - Chart B: 3 attributes
                - Line Plot
                - Date (x-axis), % change in CPI (y-axis), ENSO Cycle (colour)
            - Nominal or Ordinal: ENSO event
                - Chart A
            - Quantitative: CPI value
                - Chart A
    - Owen N
        - Summaries
        - Chart
    - Owen Y
        - Datasets
            - Original SST data (my part of Stage 1 pre-merge)
            - ENSO cycle data from NOAA [Link](https://psl.noaa.gov/enso/) 
            - SOI and ONI data using NOAA CPC [Link](https://www.cpc.ncep.noaa.gov/data/indices/oni.ascii.txt), [Link](https://www.cpc.ncep.noaa.gov/data/indices/soi)
                - Metadata: [ONI](https://data.noaa.gov/dataset/dataset/climate-prediction-center-cpcoceanic-nino-index/resource/466b8e88-5aea-476a-af49-285e88abc08e), [SOI](https://data.noaa.gov/dataset/dataset/climate-prediction-center-southern-oscillation-index/resource/6aade4a9-641f-42ce-8c76-10369ed3a190)
        - Summaries
            - Group by Nominal: 
                - Group by \[ENSO event\] Aggregate \[SOI/ONI\] using mean (to be specified)
            - Group by Binned Quantitative: 
                - Group by binned \[\] Aggregate \[\] using \[\] (to be determined)
        - Charts
            - Chart A: 3 attributes
                - Quadrant Scatter Plot
                    - Datapoints are different years
                - Rainfall (x-axis), Temperature (y-axis), Colour of Scatter Points (ENSO event)
            - Chart B: 
                - Line Plot
                    - Average Sea Surface Temperatures over time 
                    - 4 different lines for the different NINO.X regions
                - Date (x-axis), SST (y-axis)
            - Nominal or Ordinal: ENSO event
                - Chart A
            - Quantitative: Rainfall
                - Chart A
