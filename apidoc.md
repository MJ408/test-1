# 1.Campaign List

###  1.1 get available campaigns

    https://www.adhooah.com/aff/api/v2/availablecampaigns?pid=<API_KEY>

- <API_KEY> : Your API Key.

###  1.2 get my live campaigns

    https://www.adhooah.com/aff/api/v2/mycampaigns?pid=<API_KEY>

- <API_KEY> : Your API Key. 

### 1.3 json result

    - {"return": result code, "campaigns":[list]}

- result code

|Result Code | Description                      |
|----------------|-------------------------------|
|0| Success      |
|2| No Campaigns|
|4| Wrong API KEY|
|9| System Error|

- campaigns [list]

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


- example
  
(example)

*request

    https://www.adhooah.com/aff/api/v2/mycampaigns?pid=1ab17f073f4ffd28f8646a784e3a36e5

*output

    {"return":0, "campaigns":[{"preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.webzen.muorigin2.google","end_date":"2999-12-31","kpi":"Login 60% more","payout":3.0,"creatives":[{"dimen":"640x1320","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_30077_1.jpg"},{"dimen":"1040x585","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_30077_2.jpg"},{"dimen":"640x640","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_30077_3.jpg"}],"target_countries":"KR","title":"MU Origin2","url":"http:\/\/tnkd.tnkfactory.com\/tnk\/api\/ref\/c3\/21009\/22727\/c030e0b0-4001-847c-c748-1004090c0f02\/{transaction_id}?sub_id={sub_id}","daily_cap":500,"deduction":" based on 1 more install sub_id\/daily<br> D+1 Retention 50% more = 100% payout<br> D+1 Retention 30%~50% = 90% payout<br> D+1 Retention 10%~30% = 70% payout<br> D+1 Retention 10% less = no payout","os_type":"Android","pay_type":"CPI","currency":"USD","id":21009,"target_market":"GooglePlay","today_remaining":"500","event_postback":"","status":"Live","traffic":"Non-Incent"},{"preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.efunkr.ql.google","end_date":"2999-12-31","kpi":"","payout":4000.0,"creatives":[{"dimen":"640x1320","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_22690_1.jpg"},{"dimen":"1040x585","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_22690_2.jpg"},{"dimen":"640x640","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_22690_3.jpg"}],"target_countries":"KR","title":"The Rulers","url":"http:\/\/tnkd.tnkfactory.com\/tnk\/api\/ref\/c3\/18113\/22259\/c030e0b0-4001-847c-c748-1004090c0f02\/{transaction_id}?sub_id={sub_id}","daily_cap":10,"deduction":"","os_type":"Android","pay_type":"CPI","currency":"KRW","id":18113,"target_market":"GooglePlay","today_remaining":"10","event_postback":"","status":"Live","traffic":"Non-Incent"}]}


### 1.4 campaign approval request

    https://www.adhooah.com/aff/api/v2/approvalrequest?pid=<API_KEY>&campaign_id=<CAMPAIGN_ID>

- <API_KEY> : Your API Key.

- <CAMPAIGN_ID > : campaign id

  
- {"return": result code}

|Result Code | Descripition                      |
|----------------|-------------------------------|
|0| Success      |
|2| Campaign id or campaign state is wrong.(not available)|
|4| Wrong API KEY|
|9| System Error|


(example)

    https://www.adhooah.com/aff/api/v2/approvalrequest?pid=7c9704d674ec0156782e123e92c3d2a3&campaign_id=20625

*output

    {"return": 0}


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

  

      https://api.adhooah.com/aff/api.click.main?campn_id=22479&pub_id=575360&click_id={click_id}&sub_id={sub_aff}&adid={GAID}&idfa={IOS_IDFA}

* your install postback url

    http://YOUR_POSTBACK_URL?click_id={click_id}&sub_id={sub_id}&device_id={adid_or_ifa}&ip={ipaddr}

*your event postback url (optional)

    http://YOUR_EVENT_POSTBACK_URL?click_id={click_id}&sub_id={sub_id}&device_id={adid_or_ifa}&ip={ipaddr}&event={event_nm}

  
  

* If you need support, please email to performance@tnkfactory.com



