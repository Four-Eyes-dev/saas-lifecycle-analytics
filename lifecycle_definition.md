# User Lifecycle Definition

## Objective
Define clear, data-driven lifecycle stages for users in a SaaS product using
Users, Subscriptions, and Events data. These definitions will be used to power
lifecycle analysis, growth experiments, and campaign strategies.

---

## Available Data Tables

### Users Table
- user_id
- country
- plan
- signup_date

### Subscriptions Table
- user_id
- signup_date
- country
- plan
- subscription_date
- revenue
- churn_date
  
### Events Table
- user_id
- event_date
- event_type

---

## Lifecycle Stages Overview
This project classifies users into the following lifecycle stages:
1. Signed Up
2. Activated
3. Active
4. At Risk
5. Churned
6. Reactivated (optional)

---

## Lifecycle Stage Definitions

### 1. Signed Up
**Definition:**
A user who has created an account but has not yet performed any meaningful
product actions.

**Data Logic:**
- user exists in `users` table
- no qualifying activation event recorded

---

### 2. Activated
**Definition:**
A user who has completed at least one key action that indicates initial value
realization from the product.

**Data Logic (Initial Assumption):**
- user has at least one qualifying activation event in `events`
- activation occurs after signup date

> Note: Activation events will be finalized after event exploration.

---

### 3. Active
**Definition:**
An activated user who continues to engage with the product within a defined
time window.

**Data Logic (Draft):**
- user has at least one event in the last X days
- user is not churned

---

### 4. At Risk
**Definition:**
An activated user showing declining engagement and is at risk of churning.

**Data Logic (Draft):**
- no events in the last Y days
- user is not yet churned

---

### 5. Churned
**Definition:**
A user who has ended their subscription.

**Data Logic:**
- churn_date is populated in `subscriptions` table

---

### 6. Reactivated (Optional)
**Definition:**
A previously churned or inactive user who returns and resumes meaningful usage.

**Data Logic (Draft):**
- churned or at-risk user
- new qualifying event after inactivity period

---

## Assumptions & Notes
- Signup date is inferred from the Users and Subscriptions tables.
- Churn is explicitly defined in the Subscriptions table.
- Events are the primary indicator of user behavior and engagement.
- Lifecycle logic will be refined after event type exploration.

---

## Next Steps
1. Explore event types and frequencies
2. Finalize activation event(s)
3. Define exact time windows (X, Y days)
4. Translate lifecycle logic into SQL

