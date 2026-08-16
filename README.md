# Financial KPI Analysis for a Startup

## What is this project?

Every startup founder and investor asks the same three questions: are we spending too much to get one customer, is that customer even worth what we spent, and how much time do we have left before the money runs out? This project builds a simple financial model that answers all three — and turns the answers into a live Excel dashboard that anyone, technical or not, can open and understand in seconds.

## The data

Since real startup financials (revenue, customer-level spend, churn) aren't publicly available for a private company, I generated a **realistic 24-month simulated dataset** in Python, built on real-world SaaS startup patterns: steady month-over-month customer growth (~15%), expenses that start high and gradually improve (a real early-stage spending pattern), and a monthly churn rate typical of an early-stage company (4-7%). This is a standard, honest approach for portfolio projects when real financial data isn't public.

## Tools I used

- **Python** (Google Colab) — to generate and calculate all the financial data
- **Pandas, NumPy** — to build and process the numbers
- **Seaborn** — to build the cohort retention heatmap
- **Microsoft Excel** — to build the live KPI dashboard, formulas, conditional formatting, and charts

## How I approached it, step by step

**1. Built 24 months of realistic startup data.**
Customers growing steadily, revenue following that customer growth, and expenses that start high (typical for an early-stage company) and slowly improve over time.

**2. Calculated Burn Rate and Cash Runway.**
Burn Rate = how much money the company loses every month (expenses minus revenue). Cash Runway = how many months of money are left at that pace — the single most-asked question by any startup investor.

**3. Calculated CAC (Customer Acquisition Cost).**
How much it costs, on average, to get one new customer — marketing spend divided by new customers gained that month.

**4. Calculated LTV (Customer Lifetime Value).**
How much one customer is worth over their entire time with the company — based on their average monthly spend and how long they typically stick around before leaving (churn rate).

**5. Calculated the LTV:CAC Ratio — the single most important number in this whole project.**
This ratio answers: does the company earn more from a customer than it spent to get them? A ratio around 3 is considered healthy. Below 1 means the company loses money on every customer. Above 5 usually means the company could actually afford to spend more on growth.

**6. Built a Cohort Retention model.**
Grouped customers by the month they signed up, then tracked what percentage of each group was still active in the months after — shown as a color-coded heatmap (green = high retention, red = low).

**7. Built a live, self-updating Excel dashboard.**
Four headline KPI numbers with color-coded conditional formatting (so a number turns red automatically if it crosses a risky threshold), three trend charts, and the cohort heatmap — all on one page, all pulling live from the underlying data.

## The dashboard

!<img width="1851" height="696" alt="Screenshot 2026-08-16 140518" src="https://github.com/user-attachments/assets/3aede0ea-bc9a-4367-8d47-da16a38af026" />
)

*(Live Excel dashboard showing: headline KPI cards for Revenue, Burn Rate, LTV:CAC Ratio, and Cash Runway with color-coded health indicators; a Revenue vs Expenses trend; Customer Growth over time; the LTV:CAC Ratio trend; and the Customer Retention by Cohort heatmap.)*

## What I found

- **Monthly revenue (month 24):** ₹1,31,661.89
- **Monthly burn rate:** ₹23,216.70
- **Cash runway remaining:** ~9.2 months at the current pace
- **LTV:CAC Ratio:** 10.99 — well above the healthy benchmark of 3, and stays in a stable 8-14 range once the noisy first month (too few customers to be reliable yet) is excluded

## What this actually means for the business

The startup's unit economics are genuinely strong — it earns far more from each customer than it costs to acquire them. But a ratio this high isn't purely good news either: it can also mean the company is **under-investing** in growth. Since each customer is clearly worth a lot, spending more on marketing while there's still runway left could accelerate growth without hurting profitability. In short: the business model works — the smarter next move is to grow faster, not cut costs.

## Why this project, not just another spreadsheet

Most beginner finance projects stop at "here's a chart of revenue." This one goes further — it calculates the two numbers that actually decide whether a startup survives (LTV:CAC and runway), explains what those numbers mean in plain business terms, and turns them into a dashboard a non-technical founder or investor could open and immediately act on, not just something only a data person could read.
