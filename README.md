# Practical Application III: Marketing of Bank Products
<p>
 In this Practical Application (III), my goal is to compare the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines (SVC). The dataset that we are working with is related to the marketing of bank products over the telephone. The dataset may be <a href="https://archive.ics.uci.edu/ml/datasets/bank+marketing" target="_blank">found here.</a> Browser-friendly view of this Practical Application may be <u><a href="https://federalcomputing.com/PracticalApplication_III_DanielW.html" parent="_blank">found here,</a></u> which includes all renderings of visuals, plots and representations.
</p>
 <p>
The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns.
  </p>
  <p>
  Within this Practical Application, I will deliver understanding of the business objectives, show the need for data preparation, and modeling. After which, I will demostrate a correct and concise interpretation of descriptive and inferential statistics. My findings, which will include actionable insights, will be used to suggest next steps and recommendations. 
  </p>


# Business Objectives
<p>
&bull; The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed. Find how we can get more of yes instead of no.
<br>&bull; The data represents the work of 17 campaigns that occurred between May 2008 and November 2010, corresponding to a total of 79354 contacts. We will need to find out if the previous campaign has any bearings on the current one or future campaigns. Perhaps their experience with the previous campaign may have an affect. Perhaps it is an important feature.
<br>&bull; During these phone campaigns, an attractive long-term deposit application, with good interest rates, was offered. Find out who is best suitable for this.
<br>&bull; For each contact, a large number of attributes was stored in addition to if there was a success (we identify this as the target variable). Find out what information play this role and what has the most importance.
<br>&bull; Throughout the entire database, there were 6499 successes (8% success rate). Find out how we can increase the success rate. Perhaps this is by identifying a sweet spot for time when placing calls, finding what types of jobs these customers/potential customers have, find out their finacials and if they are in debt or have any credit defaults, etc. It is important to know our customer and what our targeting should be in the future. 
 </p>
 
# Data Preparation & Observations
<p>
&bull; The data is actually pretty clean already. No need for me to touch it with modifications (yet).
<br>&bull; There appears to be a high correlation between Euribor rate and the Employment Variation Rate. The value is .97 or (97%)
<br>&bull; An observation here is that the campaign was most responsive when there were higher numbers of employees. If we look at the upper 50 percentile of this plot, we can see higher response rates. Both yes and no.
<br>&bull; Perhaps there is some underlying issue here we can infer. But lets examine futher for more insights
<br>&bull; From this plot, we can clearly see that the campign opt-inm had higher success when there was an uptick when the Euro Interbank Offered Rate increased. Particularly from 1 to 1.5%, 4%, and 4.85 to 5%.
<br>&bull; It appears that there was a lot more activity going on when the Consumer Confidence Index was over 40pts.
<br>&bull; Still high refusal rates
<br>&bull; There was a peark near 36pts
<br>&bull; Highest acceptance was when pts were from 40-47.
<br>&bull; Most of the campaign outreach happend when the CPI is over 92.89. But, the acceptance and non-acceptance of term-deposits becomes equal when the the CPI
<br>&bull;  Refusal of campaign still noted to be higher than acceptance
<br>&bull; Most of the campaign outreach happend when the EVR is high. But, the acceptance and non-acceptance of term-deposits is equal when the the EVR is between -1.7 and -1.1.
<br>&bull; The best success rate was with individuals who never did business with the bank or hand contact with previous campaigns.
<br>&bull; Most of the campaign outreach happend to customers that were never contacted before and also shows a better acceptance rate to term-deposit.
<br>&bull; Perhaps there is some inference on the trust relationship or user experience with the bank. Results are best when there was no previous relationship. I question if there is some reason existing customers are not opting-in
<br>&bull; Same observation made here. Confirmed. Highest success rate is with those customers that have never been contacted before
<br>&bull; This leaves a question about why previous or current customers are not opting in. The customer relationship process may need to be monitored closely.
<br>&bull; Another observation that high success is with individuals that the bank has not already had contact with.
<br>&bull;  Best success is when individuals are not bombarded.
<br>&bull; There is indication that individuals were contacted up to 21+ times. This seems excessive. Is this a contributor to the problem we noticed earlier? Is repetitive contact to customers ruining their experience?
<br>&bull; There seems to be a sweet spot between 260 and 1050 for acceptance.
<br>&bull; Thursdays appear to be a day with most success
<br>&bull; Thursday is also the day with the most volume of calls- followed by Mondays, Wednesdays, Tuesdays, then Fridays.
<br>&bull; A high campaign was targeted to people during the month of 'May' and the same shows a higher acceptance to term-deposit.
<br>&bull; I remain curious about why the distribution is so involved in the month of May.
<br>&bull; It is clear that high reach was made to those using celluar phone
<br>&bull; Success rate was +5x higher with celluar also
<br>&bull; Campaign was highly targeted at those individuals with no current loan
<br>&bull; Campaign was most successful with +6x more successful with those who did not have a loan
<br>&bull; Interestingly, acceptance rate was almost similar between those who had housing loan vs those who did not.
<br>&bull; Conversely, there was a higher refusal rate amongst those actually had a housing loan.
<br>&bull; The bank targeted those who had no credit default in their history
<br>&bull; Acceptance rate was also highest amongst this group with no credit default
<br>&bull; Highest targeted crows were those with university degree and high school degree
<br>&bull; Highest success was also with these two groups
<br>&bull; Refusal rates were respective in terms of ratios
<br>&bull; Married people were targeted at higher rate
<br>&bull; Out of 24928 people in the Married group, acceptance rate amongst married people was 10.1%
<br>&bull; Out of the 11568 people in the Single group, acceptance rate was 14%
<br>&bull; Perhaps bank should target more single people
<br>&bull; A high campaign was targeted to people with admin, blue-collar, and technician jobs. Individuals with admin jobs shows a higher acceptance to term-deposit.
<br>&bull; Sweet spot for acceptance rate is amongst ages 29 to 36.
<br>&bull; Most refusal is amongst individuals aged 60 and upwards
<br>&bull; Throughout campaign, only 4640 indiduals accepted of 41188.
 </p>

# Modeling
<p>
 <b> A baseline analysis:</b><br>
Training time :[0.0009992122650146484]<br>
Training accuracy :[0.5025840241406819]<br>
Test accuracy :[0.5020636076717649]<br>
Accuracy score : Not Yet Available<br>
AUC score : Not Yet Available<br>
 <br>
############LOGISTIC REGRESSION ANALYSIS###############<br>
<br>
Training time :0.15794897079467773<br>
Training accuracy :0.9102355103881239<br>
Test accuracy :0.9101723719349356<br>
Accuracy score : 0.9101723719349356<br>
AUC score : 0.6906601848219758<br>
<br>
######################################################<br>
 <img src='https://awesomescreenshot.s3.amazonaws.com/image/3446742/30517597-a518b4b20adbc81949c04ed8ef361673.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220722T200329Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=05d8c4b12cba8678b27082c777775eb158791d301b1e887f361d7faf219f7da1'>
<br>
 
 <b>Logistric Regression Feature Importance Score</b><br>
 <img src='https://awesomescreenshot.s3.amazonaws.com/image/3446742/30517627-ac6e004f8fb775e8d93676dd126f0a7e.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220722T200437Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=25524da21c10cb4573bfbf098bcbb606a104b6e8482f6f22d376ea178fa67645'><br><br>
 <b> Decision Tree Feature Importance Score</b><br>
<img src='https://awesomescreenshot.s3.amazonaws.com/image/3446742/30517673-b6d7d5e4bd63a3abdc0fa6ce2beb4c70.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220722T200625Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=1bdf6d1366b452b649a9cdd41d535faaa3061043ec0069d7add14c61fd381729'><br><br>

 <b>SVM Feature Importance</b><br>
 <img src='[https://tinyurl.com/2yrmnkfz](https://awesomescreenshot.s3.amazonaws.com/image/3446742/30517721-aa718ff3832a1405e8a78eaca6d4f3e1.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220722T200803Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=5c709d76e132a81f796fc25aa7f9f9edc5d05136e42c88e3f546fe070b646934)'><br><br>
 
 
 
 </p>
 
# Actionable Insights, Next Steps, and Recommendations
<p>
&bull; Investigate current culture of the company
<br>&bull; Investigate how workers are interacting when phone banking
<br>&bull; Explorer employee morale
<br>&bull; Our data indicates that efforts are best geared toward acquisition of 'new' customers and not current
<br>&bull; Our data indicates that current campaign results is higlybased on previous outcome of campaigns (feature POUTCOME).
<br>&bull; Our data indicates that the duration of the call is key to winning a successful campaign. You have a time window of opportunity. Do not abuse it. Perhaps time series analysis can be conducted on this in the future.
<br>&bull; EURIBOR 3Month was an important feature in determination of success of campaign
<br>&bull; Other salient observations highly regard duration and nr.employed as highly important. This should be looked at by management.
<br>&bull; Our logistic regression model suggest that the type of job that our potential customer has, plays a key role in our campaign success. Perhaps we can guide our marketing team towards targeting these groups of people.
<br>&bull; Our logistic regression model also suggest that individuals without previous credit defaulting are good candidates for our campaign.
 </p>
