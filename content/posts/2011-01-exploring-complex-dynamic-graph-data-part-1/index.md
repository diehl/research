---
title: Exploring Complex, Dynamic Graph Data - Part 1
date: 2011-01-04T08:51:17-07:00
tags: [Exploratory Data Analysis, Graph Mining]
---
When I was in graduate school in the late 90s working on computer vision problems, MATLAB was my environment of choice. It provided all the tools I required for analysis and then some. Life was simple and grand.

Five years after leaving graduate school, I decided to take a dramatic turn in my research direction. Video surveillance no longer motivated me. Instead, I chose to explore problems at the interface between machine learning and the social sciences.

The implication of this move in terms of data analysis was significant. My experience base was rooted firmly in the non-relational world. I needed a new bag of tricks.

For my first foray into analyzing relational data, Python and MySQL were my friends. I rolled a lot of custom Python code to support my work in email analysis. While that code met my near-term needs, it provided limited benefit for future research objectives.

Now that I'm revisiting the Enron email dataset and thinking ahead to other types of social media, I've been reconsidering my approach to exploratory data analysis (EDA) for this class of data. When thinking about the way forward, the first question that came to mind is the following.

_What is the analog to MATLAB / R for exploratory data analysis when one is working with complex, dynamic graph data?_

In contrast to non-relational (tabular) data, social media presents rich attribute and relational data, in structured and unstructured forms, that evolves over time. Such data is most naturally represented in a graph structure; although representational choices abound. The additional complexity introduces complications across the entire EDA process.

To tease this apart further, it's worth reflecting on what capabilities we need to perform EDA. Four general capabilities come to mind.

*   _Persistence -_ Provides a non-volatile representation of the data we intend to explore.
*   _Query_ - Supports filtering and transformation operations to condition the data for analysis.
*   _Analysis -_ Enables the synthesis and execution of complex analytics on the data.
*   _Visualization_ - Facilitates rapid composition of a range of visualizations to interpret results.

MATLAB and R are appealing because they offer these capabilities to the user in one integrated environment. This allows a user to compose a wide range of EDA processes with relative ease. To my knowledge, no analogous environment exists for the relational domain.   

One may argue that MATLAB and R already provide the means to work with relational data. Clearly many are using these environments to analyze relational data. In my view, this is a significant compromise. MATLAB and R are environments rooted in the non-relational world. By using tools from that world, we are accepting constraints on the types of questions we can ask of our data with relative ease. My sense is those restrictions are severe, preventing us from exploiting the richness available in the data.  

It's not terribly surprising that no comparable integrated environment exists for the relational domain as it's not clear to me the patterns of EDA are even well understood for this class of data. If no integrated environment exists, the next question is what EDA environments can we construct through the composition of different existing capabilities? What technology stacks can we realize that meet the above needs in some fashion? I'll share my thoughts and discoveries from the past two months in my next post.
