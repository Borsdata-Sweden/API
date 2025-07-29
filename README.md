# Börsdata REST-API
## This repository contains information about Börsdata REST-API. 

## Important changes from 1 Feb-2025

The REST-API to get Json data is moved from PRO to PRO+.    
From 1Feb 2025 you will not be able to use a new PRO membershio to call REST-API.   
Existing PRO members are automaticly moved to PRO+ and will continue to get data from API until the subscription ends.

Excel plugin and Google sheets is not effected.
[Read more](https://borsdata.se/en/info/api/api_page)

## About AI and Support

We love AI, but we often receive questions where AI models generate incorrect API calls.   
As a developer, it's your responsibility to ensure that the API calls are accurate and that all parameters follow our documentation.

To assist you better: 
- We always need the full API URL.
- Please verify the API URL using Swagger to check for any differences.
- Also, make sure the parameters are correct according to our GitHub documentation.


## Getting started
1. If you dont have an API KEY you need to Apply for it on [Börsdata MyPage.](https://borsdata.se/en/mypage/api)
2. Then you can download our sample projects from GitHub and start coding.

## Nordic and Global data
From Sep 2022 we provide Global data in API.  
Global data is only available for Pro+ members.  
Read more about [Global Instruments](https://github.com/Borsdata-Sweden/API/wiki/Global-Instruments)


## Documentation
1. We use this Github as the main info page for programmers. 
2. Most info is in the [Wiki](https://github.com/Borsdata-Sweden/API/wiki).
3. The API calls is documented [here with swagger](https://apidoc.borsdata.se/swagger/index.html)
4. You can read about the API on our [info page](https://borsdata.se/info/api/api_info)
5. Try our [c# sample client](https://github.com/Borsdata-Sweden/API-CSharp-Client).


## Rate Limits
The API is rate limited to 100 calls in 10 second.  

You will recieve a 429 when exceding the rate limit.  
Check header Retry-After to see time to wait before next call. 

There is no set max limit of api calls, but you should try not to exceed 10K api calls per 24h.  
It's ok to do more api calls occasionally, but not every day.  
Please try to stay below 10K per day.

## Issues Tracking
We use GitHub's Issues tracker for our project. Feel free to create bug reports and features requests. Make sure to read the documentation before asking questions - this will avoid repeated questions, leaving us more time for developing the library.

## Sample Code
- [C# API Lib with sample code](https://github.com/Borsdata-Sweden/API-CSharp-Client).

- [Python Lib with full code](https://github.com/alexwox/Modern-Borsdata-Client/tree/main)    
(3d-party code. Special thanks to alexwox)

- [Python Lib with sample code](https://github.com/TapeReaderJoe/BorsdataAPI)   
(3d-party code. Special thanks to Johan for full Python lib!)    

- [Python Lib with sample code v2 (Not all functions)](https://github.com/erab17/borsdata-jerker-branch/tree/dev_branch).     
(3d-party code. Special thanks to Joel Roxell, and Jerker for Python API lib!)   

- [PHP Lib with sample code](https://github.com/reinew/borsdata-api).   
(3d-party code. Special thanks to Reinew for PhP API lib! )

- [javascript code](https://github.com/reinew/borsdata-api-js).   
(3d-party code. Special thanks to Reinew! )

- [Börsdata API i R](https://github.com/JakobJohannesson/borsdata)    
(3d-party code. Special thanks to Jakob Johannesson for R API lib!)     

- [Python Lib - matplotlib samples](https://github.com/TapeReaderJoe/BorsdataAPI)    
[Python Lib - matplotlib docs](https://github.com/TapeReaderJoe/BorsdataAPI/blob/notebooks/borsdata/breadth_indicators.ipynb)    
(3d-party code)     

- [Postman collection](https://borsdata.se/meta/shared/BD-API_SERVICE_V1.postman_collection.json)   


## Stay Tuned
Follow us on [Twitter](https://twitter.com/search?f=tweets&vertical=default&q=BORSDATA%20OR%2040procent20ar&src=savs) and [Facebook](https://www.facebook.com/borsdata.se/) to receive updates.


## Disclaimer
Börsdata and the information contained herein is not intended to be a source of advice or credit analysis with respect to the material presented, and the information and/or documents contained in this website do not constitute investment advice.  
The user is responsible for the risk and should therefore acquire information about the terms that apply to trade with such instruments, and about the qualities of the instruments. Placements or other positions in financial instruments such as stock is done at your own risk. <br> Börsdata cannot in any way be held responsible for any investment decisions that result from the financial information on the website.  
Always do your own Research. 


## Updates
### 2019-04-04  
- Add new API call to get list of Last Stockprice for all Instruments.  
(No need to call all Instruments to get last stockprices on daily basis. One call instead of +1600)
  
- Add new API call to get all reports for one Instrument.  
(To get Year, R12, Quarter Reports you only need one call)

### 2020-04-21
- Add maxCount to get up to 20 year stockprice, 20 year reports and 40 R12&Quarter reports.
[Read more about &maxCount](https://github.com/Borsdata-Sweden/API/wiki/20-year-history)
- Add report/kpi meta data for translations.
- Add stockprices/date to get all stockprice for a specific date.

### 2020-10-19
- Add 4 new data to Report

### 2022-08-17
- Added 3 new Array functions to get max 50 instruments in one call.
- Reports, Stockprice, Kpis history

### 2022-09-08
- Add Global instruments to API.
  
### 2023-09-14
Add new functions   
- Instrument description 
- Report calendar 
- Dividend calendar 
- Holdings Insider (Pro+) 
- Holdings Shorts (Pro+)
- Holdings Buyback (Pro+)

[Calendar](https://github.com/Borsdata-Sweden/API/wiki/Calendar)   
[Holdings](https://github.com/Borsdata-Sweden/API/wiki/Calendar](https://github.com/Borsdata-Sweden/API/wiki/Holdings)https://github.com/Borsdata-Sweden/API/wiki/Holdings) 

### 2024-02-06
Added two new values to /Instruments
- StockPriceCurrency
- ReportCurrency

Report data.   
- Added &original=1 to get original report data currency.

### 2024-02-05
- Add &from parameter to StockSplit.   
You can now receive all stocksplit history 



