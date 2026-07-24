# King County Housing EDA – Presentation Notes

## Recommended presentation order

Start with the client and the business problem, not the dataset. The audience should first understand why the analysis matters. Then introduce the dataset, explain the cleaning decisions briefly, present the hypotheses, summarize the findings, and end with business recommendations.

Suggested 10-minute flow:

1. Title and purpose – 30 seconds
2. Client and business question – 1 minute
3. Dataset and cleaning – 1.5 minutes
4. Hypotheses – 1 minute
5. Findings – 4 minutes
6. Recommendations and conclusion – 2 minutes

---

## Slide 1 – Title

**What to say:**

The purpose of this project is to explore the King County housing market through exploratory data analysis (EDA). By analyzing real estate sales data, the project identifies the factors that have the strongest relationship with house prices. 
The findings provide practical insights into how location, renovation, construction quality, and seasonal trends influence property values.

## Slide 2 – The 10-minute story

**What to say:**

I will first explain the client problem and the main business question.
Then I will briefly describe the dataset and the key cleaning decisions. 
After that, I will go through the hypotheses and summarize the evidence for each one. 
Finally, I will translate the results into recommendations for the seller.

---

## Slide 3 – Client & business question

**What to say:**

The client is Timothy Stevens, a seller. 
He owns expensive homes in the city center and wants to sell them within the next year. 
He is also open to renovation if it increases profit. 

Therefore, the business question is: which property factors should he prioritize to maximize resale value?
and
This EDA meant to support a clear selling strategy.

---

## Slide 4 – Data foundation

**What to say:**

The dataset contains 21,597 house sales and 21 variables.
These variables are property characteristics such as bedrooms, bathrooms, living area, grade, condition, location, waterfront status, view, year built, year renovated, and sale date ,,and etcetera,,

Before analyzing the hypotheses, I checked missing values, duplicates, data types, and summary statistics. 
Data converted to appropriate formats.

For example:
Dates were converted into datetime format, and ZIP code was treated as a categorical variable. because it represents a location category, not a numerical measurement.

For renovation, I was careful with missing values. The dataset contained both zero values and missing values in `yr_renovated`. Since the exact meaning of the missing values was not documented, I kept them separate instead of assuming they meant no renovation.

waterfront       2391
view               63
sqft_basement     452
yr_renovated     3848
dtype: int64

Because these missing items were a significant number.
---

## Slide 5 – Hypotheses

**What to say:**

I tested four hypotheses. 
The first hypothesis is that location affects price. 
For location, I looked at ZIP code, waterfront access, and view quality.

The second hypothesis is that renovated homes sell for higher prices. 

The third hypothesis is that higher construction quality, measured by grade, is associated with higher prices. 

The fourth hypothesis is that seasonality affects price, meaning spring and summer sales may perform better than fall and winter sales.

The first three hypotheses are the most important for the client because they are directly related to pricing and property preparation.

---

## Slide 6 – Finding 1: Location

**What to say:**

Now I want to talk about the findings.
The strongest finding is location. 

Median house prices vary substantially by ZIP code. 
The most expensive ZIP code in the analysis has a median price of about 1.895 million dollars, while the lowest ZIP code has a median price of about 235 thousand dollars.

Waterfront access also shows a major price difference. 
Waterfront homes have a much higher median price than non-waterfront homes. 

Better view ratings are also generally associated with higher median prices.

This EDA supports the first hypothesis: location-related features are strongly associated with house prices.

---

## Slide 7 – Finding 2: Renovation

**What to say:**

For renovation, I compared only homes with known renovation status. Homes with unknown renovation information were not forced into either group.  (yr_renovated  3848) observations->Fild->yr-renovation-> NaN

The median price for non-renovated homes is about 448 thousand dollars. The median price for renovated homes is about 607.5 thousand dollars. That is approximately a 36 percent difference in median price.

This EDA supports the renovation hypothesis, but it does not mean every renovation is automatically profitable. The seller should compare expected price uplift with renovation cost.

---

## Slide 8 – Finding 3: Grade

**What to say:**

Grade is one of the clearest value signals in the dataset. 

 As grade increases, median price rises strongly. 
 
 For example, Grade 7 has a median price of about 375 thousand dollars, Grade 10 is around 914 thousand dollars, and Grade 13 is about 2.98 million dollars.

This supports the hypothesis that construction quality is associated with higher selling prices. For the seller, this means quality and finish level should be emphasized in pricing and marketing.

---

## Slide 9 – Finding 4: Seasonality

**What to say:**

Seasonality showed weaker evidence. Monthly median prices ranged from about 426.5 thousand dollars to about 477 thousand dollars. This is a difference of around 12 percent.

Compared with the differences caused by location, waterfront access, renovation, and grade, this is much smaller. Therefore, timing may matter slightly, but it should not be the main strategy.

This hypothesis is weak or not strongly supported.

---

## Slide 10 – Recommendations

**What to say:**

Based on the analysis, I recommend four actions.

First, price each property based on micro-location, especially ZIP code, waterfront access, and view quality. Second, renovate selectively. Renovation is associated with higher prices, but the seller should only invest when the expected uplift is greater than the renovation cost. Third, use grade and quality as a value signal in marketing. Fourth, do not rely too heavily on timing, because seasonality appears weaker than property fundamentals.

---

## Slide 11 – Final answer

**What to say:**

The final answer is that Timothy should maximize resale value by combining location-based pricing with selective property improvements. The strongest signals in the data are location, waterfront/view, renovation status, and grade. Seasonality is secondary.

In simple terms, the seller should focus on what the property is, where it is, and how well it is presented — more than trying to time the market perfectly.
