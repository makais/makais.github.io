---
title: Sentiment Index 
description: Full-stack development of a Voice of the Customer system
categpries: ["project"]
tags: ["sentiment", "data visualization", "python", "sql", "2020"]
cover:
    image: "ces-graph-cover.jpg"
    alt: "a line graph"
---

"Voice of the Customer" initiative that gathered user sentiment data across multiple interaction points to provide a cross-sectional view of user experience with Bentley products. The program combined input from four sources: executive interviews capturing Net Promoter Scores (NPS) and qualitative feedback; digital surveys offering periodic sentiment trends and open-text analysis; transactional Customer Effort Score (CES) surveys assessing ease of interaction; and G2.com product reviews providing product-level sentiment insights. 

I implemented the system through a series of workflows to automate survey distribution, data retrieval, and sentiment processing.

- Orchestrated by Azure Data Factory pipelines to initiate sending CES surveys, and retrieve and process various sentiment data.

- The pipelines interacted with Durable Azure Functions in Python through HTTP to initiate and retrieve Qualtrics surveys and to download G2 reviews using REST APIs.

- The various customer feedback streams were processed with SQL to form a multi-component user sentiment index for use in a Voice-of-the-Customer dashboard in QlikSense. 

{{<figure src="sentiment-flowchart.jpg" alt="flowchart image" caption="These data streams collectively formed the basis for a multi-component sentiment index displayed in a QlikSense dashboard for product teams to track and act on user sentiment.">}}

Techniques for generating continuous date ranges, pivoting denormalized data, and computing inline rolling averages are shown in this [SQL example](rolling-ces-avg.sql.txt). This [Python example](sentiment-qualtrics-dl-activity.py.txt) illustrates an Azure Function that retrieves and flattens Qualtrics survey data for ingestion into the sentiment analytics pipeline.