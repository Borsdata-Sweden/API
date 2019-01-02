#Börsdata API
##This repository contains information about Börsdata API. 
 
##Getting started
If you dont have an API KEY you need to Apply for it on Börsdata MyPage.
Then you can download one of our sample projects and start coding.

##Code documentation
The API calls is documented here with swagger.

##Code samples
We use swagger to generate some sample code project to get you started.
You find them in our other repositories.

##Rate Limits
The API is rate limited to 2 calls pr.second. 
You will recieve a 403 when exceding the rate limit. 
In the header you will find the time (ms) you need to wait before you can call again.

##Best practice
Börsdata update Stockprices and KPIs once a day.
The API only support end-day stockprice that Börsdata recieves when the market is closed. 
The stockdata and KPIs is normaly fully updated after 20:00 UTC time.
-	Only get the data for the companies you need. (Reduce our server load)
-	Call API after 20:00 to get today latest data. (Or you will get yesterday data)
-	Respect the Ratelimit. If you get 403, then wait before calling again.

##Issues Tracking
We use GitHub's Issues tracker for our project. Feel free to create bug reports and features requests. Make sure to read the documentation before asking questions - this will avoid repeated questions, leaving us more time for developing the library.

##Stay Tuned
Follow us on Twitter and Facebook to receive updates.
