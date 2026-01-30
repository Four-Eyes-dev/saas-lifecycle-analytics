# SaaS Lifecycle Analytics & Automation Framework
## V
## Overview
This project explores how product and behavioral data can be used to design effective lifecycle campaigns aimed at improving user activation, engagement, and early retention in a SaaS product.

Using real-world SaaS product data, the project focuses on understanding user behavior, identifying drop-off points, and defining lifecycle stages that can power automated customer journeys in tools such as Braze or CleverTap.

## Objectives
- Define key lifecycle stages using behavioral data
- Identify activation and early engagement signals
- Measure retention and churn using subscription data
- Design data-backed lifecycle automation logic
- Translate analytics into actionable growth strategies

## Dataset
The analysis is based on a real-world SaaS product analytics dataset containing:
- User-level attributes
- Event-level behavioral data
- Subscription and churn information

Dataset structure includes:
- `Users` table
- `Events` table
- `Subscription` table

## Tools & Skills Demonstrated
- Product analytics
- Lifecycle modeling
- Funnel and retention analysis
- Python
- Growth & lifecycle strategy

## Project Status
 In progress  
Current phase: Data understanding & lifecycle definition


## V.1
## Current Work (Activation Analysis)

The first phase of this project focuses on **user activation**, answering:

- How soon do users perform their first meaningful action after signup?
- What percentage of users activate within a defined time window?
- How activation can be defined using behavioral data rather than assumptions

### Activation Definition
For this project:
- A user is considered **activated** if they perform their first event within **1 day of signup**

### Analysis Performed
- Event frequency analysis
- Events per user distribution
- Time from signup to first event
- Filtering invalid (pre-signup) events
- Activation rate calculation
- Activation distribution visualization

**Notebook:**  
`notebooks/01_activation_analysis.ipynb`

