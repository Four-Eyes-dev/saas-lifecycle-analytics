# Project Notes – Lifecycle Analytics

## 1. Business Context
The product is assumed to be a SaaS platform where users sign up, interact with product features, and subscribe to paid plans. A key challenge is that many users sign up but fail to activate or retain long enough to deliver long-term value.

The goal is to design a lifecycle framework that supports onboarding, activation, engagement, and churn prevention.

## 2. Dataset Overview
The dataset contains three main tables:

### Users
Represents user identity and segmentation.
- user_id
- country
- plan
- signup-related date fields

### Events
Captures behavioral activity.
- user_id
- event_type
- event_date / timestamp

### Subscription
Tracks commercial status and churn.
- user_id
- signup_date
- country
- plan
- subscription_status
- revenue
- churn_date

## 3. Initial Observations
- User signup can be inferred from the Users and Subscription tables
- User behavior is tracked at the event level
- Churn is explicitly defined in the Subscription table
- Behavioral inactivity and subscription churn should be treated as separate concepts

## 4. Early Lifecycle Hypothesis
Users who do not complete a meaningful product action shortly after signup are less likely to retain or convert.

This project will focus on identifying that meaningful action (activation) and designing lifecycle interventions around it.
