# 1.Campaign List

###  1.1 get available campaigns
```
https://www.adhooah.com/aff/api/v2/availablecampaigns?pid=<API_KEY>
```
- <API_KEY> : Your API Key.

###  1.2 get my live campaigns
```
https://www.adhooah.com/aff/api/v2/mycampaigns?pid=<API_KEY>
```
- <API_KEY> : Your API Key. 

### 1.3 json result
```
{"return": result code, "campaigns":[list]}
```
* result code

|Result Code | Description                      |
|----------------|-------------------------------|
|0| Success      |
|2| No Campaigns|
|4| Wrong API KEY|
|9| System Error|

* campaigns [list]

 | Column           | Description                                                 |
|------------------|---------------------------------------------------------------
| title            | campaign title                                                
| id               | campaign ID                                                   
| url              | campaign URL                                                  
| pay_type         | CPI or CPA                                                    
| payout           | payout                                                        
| daily_cap        | daily cap                                                     
| status           | campaign status (ex, Live, Stop, Available)                   
| currency         | payout currency                                               
| preview          | campaign preview                                              
| traffic          | Incentive or Non-Incentive                                    
| kpi              | campaign KPI                                                  
| end_date         | campaign end date                                             
| today_remaining  | number lef today                                              
| deduction        | deduction condition                                           
| os_type          | Andorid or IOS or mobile Web                                  
| target_countries | targeted countries (ex, KR, US, …)                            
| target_market    | targeted market (ex, GooglePlay, AppStore, Web)               
| event_postback   | event postback name. (ex, login, level_3, purchae, … ) |
| creatives        | [list] {dimen, url}          |


* example
  
(example)

* request
```
https://www.adhooah.com/aff/api/v2/mycampaigns?pid=1ab17f073f4ffd28f8646a784e3a36e5
```
* output
```json
{
   "return":0,
   "campaigns":[
      {
         "preview":"https:\/\/apps.apple.com\/jp\/app\/id982410763",
         "end_date":"2999-12-31",
         "kpi":"Conversion action: Driver registration\n* Install → Member registration → Credit card & phone number authentication → Driver registration\n(Average conversion rate from Install to Driver registration is about 8-10%)\"",
         "payout":29000.0,
         "creatives":[
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84451_600x500.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84452_600x500.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84453_640x100.jpg"
            }
         ],
         "target_countries":"JP",
         "title":"Anyca iOS JP (Driver registration)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28767&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":5,
         "deduction":"Please check this sheet:\nhttps:\/\/docs.google.com\/spreadsheets\/d\/188SGAsieVle6UwFpGz2B5BvAVlCAseWJ5_zKlahYMDM\/edit?usp=sharing",
         "os_type":"iOS",
         "pay_type":"CPI",
         "currency":"KRW",
         "id":28767,
         "target_market":"AppStore",
         "today_remaining":"5",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/store.steampowered.com\/app\/1190130\/Araha__Curse_of_Yieun_Island\/",
         "end_date":"2999-12-31",
         "kpi":"Purchase",
         "payout":10.0,
         "creatives":[
            
         ],
         "target_countries":"KR",
         "title":"Araha(CPC)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28904&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":100,
         "deduction":"test",
         "os_type":"Web",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":28904,
         "target_market":"Web",
         "today_remaining":"100",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.btckorea.bithumb",
         "end_date":"2021-01-31",
         "kpi":"Registration complete\n(Send a postback when registration is completed.)",
         "payout":6000.0,
         "creatives":[
            {
               "dimen":"627x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85539_627x627.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85540_640x100.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85541_640x200.jpg"
            }
         ],
         "target_countries":"KR",
         "title":"Bithumb (Registration)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=29001&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":0,
         "deduction":"** Fraud traffic\n-  Fraud traffic is discussed separately\n- Country : other than KR\n- Language : other than \"Ko-Kr\"\n- CTIT < 5 sec\n- Carrier : other than KT, LG U+, SKTelecom OR Unkown\n-  Overlap ADID\n-  Sign up after install time : less 60 sec\n-  Exclude if there is no ADID \/ IDFA.\n-  install-Registration time < 60s\n-  Deduction if the difference between the actual installation time and the actual installation time indicated in the tracker \"Customer User ID\" is more than 1 minute",
         "os_type":"Android",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":29001,
         "target_market":"GooglePlay",
         "today_remaining":"0",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      }
      
   ]
}
```

### 1.4 campaign approval request
```
https://www.adhooah.com/aff/api/v2/approvalrequest?pid=<API_KEY>&campaign_id=<CAMPAIGN_ID>
```
* <API_KEY> : Your API Key.

* <CAMPAIGN_ID > : campaign id

  
* {"return": result code}

|Result Code | Descripition                      |
|----------------|-------------------------------|
|0| Success      |
|2| Campaign id or campaign state is wrong.(not available)|
|4| Wrong API KEY|
|9| System Error|


(example)
```
https://www.adhooah.com/aff/api/v2/approvalrequest?pid=7c9704d674ec0156782e123e92c3d2a3&campaign_id=20625
```
* output
```
{"return": 0}
```

# 2. Postback
### 2.1 Postback macro

| Column        | data type | Description                                                      |
|---------------|-----------|------------------------------------------------------------------|
| {app_id}      | number    | campaign id                                                      |
| {sub_id}      | string    | sub publisher id (campaign url’s	&sub_id={sub_id})        |
| {click_id}    | string    | your click id (your transaction id)                              |
| {ipaddr}      | string    | ip address of conversion devices                                 |
| {attr_seq}    | number    | unique transaction id  (generated by tnk)                        |
| {ios_ifa}     | string    | ios idfa                                                         |
| {aos_adid}    | string    | google aid                                                       |
| {adid_or_ifa} | string    | ios idfa or google aid                                           |
| {ph_mdl}      | string    | conversion device’s model name                                   |
| {os_ver}      | string    | conversion device’s version (ex. 5.2)                            |
| {ntn_cd}      | string    | conversion nations (ex.KR)                                       |
| {payout}      | number    | conversion payout                                                |
| {event_nm}    | string    | event name. It’s event postback only (ex.login,				level_10) |

  
### 2.2 install/event postback url

When install or conversion occurs, install postback url is called.

If the campaign supports in-app events, the event postback url is called.

You should send the following value to your campaign URL:

{click_id} : your click id

{sub_id} : your sub publisher id

  
  

(example)

* campaign url
```
https://api.adhooah.com/aff/api.click.main?campn_id=22479&pub_id=575360&click_id={click_id}&sub_id={sub_aff}&adid={GAID}&idfa={IOS_IDFA}
```
* your install postback url
```
http://YOUR_POSTBACK_URL?click_id={click_id}&sub_id={sub_id}&device_id={adid_or_ifa}&ip={ipaddr}
```
* your event postback url (optional)
```
http://YOUR_EVENT_POSTBACK_URL?click_id={click_id}&sub_id={sub_id}&device_id={adid_or_ifa}&ip={ipaddr}&event={event_nm}
```
  
  

* If you need support, please email to performance@tnkfactory.com



