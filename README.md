📧 Email Campaign Optimization
This project analyzes an email marketing campaign to uncover what drives user engagement and builds a machine learning model to predict click-through probability, guiding future targeting strategies.

*Main file -- first.ipynb*

✅ Project Goals

✔️ Analyze open and click-through behavior across email campaigns

✔️ Understand the impact of email content, personalization, timing, user demographics, and purchase history

✔️ Engineer relevant features (e.g., cyclical time encoding, log-transform for skewed variables)

✔️ Build and evaluate machine learning models (Logistic Regression, Random Forest, XGBoost, LightGBM)

✔️ Optimize threshold to maximize F1 score and click prediction

✔️ Derive key actionable insights to inform future marketing strategies

✔️ Provide an implementation plan for real-world deployment

✅ Summary of Key Insights

🕒 Timing Optimization
✔️ Best hours to send: 23:00, 00:00, 10:00

✔️ Worst hours: 18:00 - 22:00

✔️ Best days: Wednesday, Tuesday

✉️ Email Content

✔️ Short emails outperform long ones

✔️ Personalized emails drive significantly higher CTR

✔️ Personalization works especially well for high-value customers

🌍 Geographic Performance

✔️ Top performing countries (by CTR): UK > US > ES > FR

🛍️ User Segmentation (Purchase History)

✔️ Customers with 6+ purchases had highest engagement

✔️ CTR improves consistently with more past purchases

✅ Modeling Results

✔️ Used SMOTE to balance classes due to low click-through rate (~2.1%)

✔️ Evaluated multiple models using ROC AUC, PR AUC, and F1-score

✔️ Best model: XGBoost, tuned with cross-validation

✔️ Applied optimal probability threshold using Precision-Recall curve

✅ Performance Improvement Estimate

✔️ By targeting the top 50% of users based on model score, we can achieve a ~65.1% increase in click-through rate

✔️ Model-based targeting boosts CTR from 2.1% → ~3.48%

✅ How to Test This in Production

✔️ Phase 1: Score users using the model

✔️ Phase 2: Send emails only to top 50% of predicted high-CTR users

✔️ Phase 3: Conduct A/B test comparing model-selected users vs random users

✔️ Phase 4: Measure actual CTR lift to validate model predictions

✔️ Phase 5: Iterate with new campaign data

✅ Answers to Key Business Questions

💬 "The VP of marketing thinks it's stupid to send emails randomly. Can you build a model to optimize this?"
✔️ Yes! We've built a model that predicts the probability of a user clicking an email based on historical behavior, demographics, email content, and timing.
✔️ It allows intelligent targeting instead of random sends — maximizing ROI and user engagement.

💡 "By how much could this model improve CTR? How would you test it?"

✔️ Our model identifies the top 50% of users with highest predicted CTR.
✔️ When targeting these users, we estimate a 65.1% increase in CTR.
✔️ We'd test this through an A/B test comparing:

Group A: Emails sent using the model

Group B: Emails sent at random
✔️ Track CTR across both groups to validate uplift.

🔍 "Did you find any interesting patterns by user segments?"
✔️ Yes, multiple patterns:

📈 High purchase history users (6+ past purchases) have significantly higher CTR

📬 Personalized emails work better across the board

🌍 Some countries (e.g., UK, US) outperform others — consider localized content

🕒 Send emails late at night or in the morning for better engagement

📄 Keep emails short and to the point

✅ Final Recommendations

✔️ Use the model to score and target the top 50% of your audience

✔️ Focus on personalized, short emails for maximum engagement

✔️ Prioritize high-value customers (6+ past purchases)

✔️ Send emails between 23:00 - 11:00, especially on Tuesdays and Wednesdays

✔️ Prioritize regions like UK and US for better ROI

✔️ Roll out in phases with continuous monitoring
