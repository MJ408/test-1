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
```
https://www.adhooah.com/aff/api/v2/mycampaigns?pid=1ab17f073f4ffd28f8646a784e3a36e5
```
*output
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
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84454_640x100.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84455_640x100.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84456_640x200.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84457_640x200.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84458_640x200.jpg"
            },
            {
               "dimen":"1024x768",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84459_1024x768.jpg"
            },
            {
               "dimen":"1024x768",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84460_1024x768.jpg"
            },
            {
               "dimen":"1024x768",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84461_1024x768.jpg"
            },
            {
               "dimen":"1024x768",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84462_1024x768.jpg"
            },
            {
               "dimen":"1024x768",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84463_1024x768.jpg"
            },
            {
               "dimen":"1024x768",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84464_1024x768.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84465_1200x627.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84466_1200x627.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84467_1200x627.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84468_1200x627.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84469_1200x627.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84470_1200x627.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84471_600x500.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84472_600x500.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84473_600x500.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84474_600x500.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84475_600x500.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/28767_f_84476_600x500.jpg"
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
            },
            {
               "dimen":"640x960",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85542_640x960.jpg"
            },
            {
               "dimen":"640x1320",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85543_640x1320.jpg"
            },
            {
               "dimen":"960x540",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85544_960x540.jpg"
            },
            {
               "dimen":"960x640",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85545_960x640.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85546_1200x627.jpg"
            },
            {
               "dimen":"300x300",
               "url":"http:\/\/www.adhooah.com\/creative\/29001_f_85547_300x300.jpg"
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
      },
      {
         "preview":"https:\/\/apps.apple.com\/jp\/app\/id1455950606",
         "end_date":"2999-12-31",
         "kpi":"■ Achievement point: af_level_b100　\n*Achieved level 100(Expected to arrive in 1-2 weeks after installation)",
         "payout":6800.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/open?id=1CUR6pDfbBJmiG4qHRHxKHqiYVhF7TeH0"
            }
         ],
         "target_countries":"JP",
         "title":"Bokujyo Konkatu iOS JP(level 100)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=27007&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":100,
         "deduction":"▼Among Sub ID-based AND Number of Installs = 10 or more(<- the accumulated number of install per month based on sub ID)\nApplies to any of these below;\n・ CTIT is longer than 24hours = 40％ or above\n・ CTIT is longer than 1hours = 60% or above\n・ CTIT is shorter than 10 seconds = 40% or above\n・ More than 80% of users' CTITs are within a specific 60 seconds.\n・ iOS ver is older than 12.1 (12.1 is OK, 12.0 is NG)  = 50％ or above\n・ Android OS ver is older than 5.1  (5.1 is OK, 5.0 is NG)= 50％ or above\n・ ITET is shorter than standard value = 50％ or above\n - If it is normal, it takes 3 minutes or more from installation to \"Tutorial complete\".\n・ Language setting on the device is not Japanese = 40% or above\n・1d RR(Retention Rate) is less than 10% (1d= next day of install date)\n・Mandatory event(s) is\/are skipped. Timing of fired event(s) discrepant.\n  (Eg. There is no membership registration fired, but some age verifications are fired.)\n・The total daily playing time is 0 seconds. (Applies to sub ID that has 1d retention)\n  (Eg. There are 500 users retaining from 0d to 2d, but each user didn\u2019t have playing time (=0 second of spending time in the app), all the conversions from the same sub ID will be eliminated.\n\n\n▼Among Main ID-based AND Number of Installs = 10 or more(<- the accumulated number of install per month based on sub ID)\nApplies to any of these below;\n・ CTIT is less than 10 seconds or longer than 24hours　= 40％ or above\n・ CTIT is longer than 1hours　= 60% or above\n\n\n\n▼Among users based\n・ CTIT is longer than 8hours\n・ CTIT is shorter than 10 seconds\n・ Language settings other than Japanese\n・ ITET is outlying *Set for each app\n・ Events are fired unrealistically\n(Eg. Purchase occurs even though the tutorial is not completed) *Set for each app\n・ Mandatory events are skipped (not fired). The timing of fired events contradict = 50% or more among all the conversion \n (Eg, The mandatory event is registration.  Registration=0, Age verification=3, and if the outlier is 50% or more among conversions.\nEven if mandatory events are not skipped, if the 1st event is skipped and the 2nd one is fired, or the 1st event is fired after the 2nd event is fired.)",
         "os_type":"iOS",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":27007,
         "target_market":"AppStore",
         "today_remaining":"100",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/itunes.apple.com\/jp\/app\/id1119874095",
         "end_date":"2999-12-31",
         "kpi":"Male monthly purchase",
         "payout":1000.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/open?id=1Y7zGykfWmmjbUG1TEn7lgfxM95EiP_v1"
            },
            {
               "dimen":"1200x628",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_f_75173_1200x628.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_f_75174_300x250.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_b_75175_320x50.jpg"
            },
            {
               "dimen":"300x50",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_b_75176_300x50.jpg"
            },
            {
               "dimen":"1200x628",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_f_75169_1200x628.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_f_75170_300x250.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_b_75171_320x50.jpg"
            },
            {
               "dimen":"300x50",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_b_75172_300x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_b_75167_320x50.jpg"
            },
            {
               "dimen":"300x50",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_b_75168_300x50.jpg"
            },
            {
               "dimen":"1200x628",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_f_75165_1200x628.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/26827_f_75166_300x250.jpg"
            }
         ],
         "target_countries":"JP",
         "title":"CROSS ME iOS JP (Male monthly purchase)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=26827&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":10,
         "deduction":"▼Among Sub ID-based AND Number of Installs = 10 or more(<- the accumulated number of install per month based on sub ID)\nApplies to any of these below;\n・ CTIT is longer than 24hours = 40％ or above\n・ CTIT is longer than 1hours = 60% or above\n・ CTIT is shorter than 10 seconds = 40% or above\n・ More than 80% of users' CTITs are within a specific 60 seconds.\n・ iOS ver is older than 12.1 (12.1 is OK, 12.0 is NG)  = 50％ or above\n・ Android OS ver is older than 5.1  (5.1 is OK, 5.0 is NG)= 50％ or above\n・ ITET is shorter than standard value = 50％ or above\n - If it is normal, it takes 3 minutes or more from installation to \"Tutorial complete\".\n・ Language setting on the device is not Japanese = 40% or above\n・1d RR(Retention Rate) is less than 10% (1d= next day of install date)\n・Mandatory event(s) is\/are skipped. Timing of fired event(s) discrepant.\n  (Eg. There is no membership registration fired, but some age verifications are fired.)\n・The total daily playing time is 0 seconds. (Applies to sub ID that has 1d retention)\n  (Eg. There are 500 users retaining from 0d to 2d, but each user didn\u2019t have playing time (=0 second of spending time in the app), all the conversions from the same sub ID will be eliminated.\n\n\n▼Among Main ID-based AND Number of Installs = 10 or more(<- the accumulated number of install per month based on sub ID)\nApplies to any of these below;\n・ CTIT is less than 10 seconds or longer than 24hours　= 40％ or above\n・ CTIT is longer than 1hours　= 60% or above\n\n\n\n▼Among users based\n・ CTIT is longer than 8hours\n・ CTIT is shorter than 10 seconds\n・ Language settings other than Japanese\n・ ITET is outlying *Set for each app\n・ Events are fired unrealistically\n(Eg. Purchase occurs even though the tutorial is not completed) *Set for each app\n・ Mandatory events are skipped (not fired). The timing of fired events contradict = 50% or more among all the conversion \n (Eg, The mandatory event is registration.  Registration=0, Age verification=3, and if the outlier is 50% or more among conversions.\nEven if mandatory events are not skipped, if the 1st event is skipped and the 2nd one is fired, or the 1st event is fired after the 2nd event is fired.)",
         "os_type":"iOS",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":26827,
         "target_market":"AppStore",
         "today_remaining":"10",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/www.michinshop.net\/m2\/goods\/view.php?goodsno=40",
         "end_date":"2999-12-31",
         "kpi":"After 10 days from the confirmation of purchase will be recognized as performance.",
         "payout":2.9,
         "creatives":[
            {
               "dimen":"600x340",
               "url":"http:\/\/www.adhooah.com\/creative\/124207_f_64778_600x340.jpg"
            }
         ],
         "target_countries":"All",
         "title":"Cardenbell Sardin Chef Soap 100g",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=124207&pub_id=8522&click_id={transaction_id}&sub_id={sub_id}",
         "daily_cap":0,
         "deduction":"구매취소 건은 정산에서 제외됩니다.",
         "os_type":"Web",
         "pay_type":"CPA",
         "currency":"USD",
         "id":124207,
         "target_market":"Web",
         "today_remaining":"0",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/closers.naddicjapan.com\/event_2020\/20201203\/closers\/index.html",
         "end_date":"2999-12-31",
         "kpi":"Conversion action: Sign up(with e-mail verification)\n*Conversion action flow: \nhttps:\/\/drive.google.com\/drive\/folders\/1VJ9dmLZYgbaEnm0BnDe55pkOU3jHvbMP?usp=sharing",
         "payout":2800.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/drive\/folders\/1VJ9dmLZYgbaEnm0BnDe55pkOU3jHvbMP?usp=sharing"
            }
         ],
         "target_countries":"JP",
         "title":"Closers JP (Sign up)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28753&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":100,
         "deduction":"> Fraud traffic\n> non-targeted GEO \n> Abnormal email addresses (such as missing domains, email addresses that cannot be generated from those domains)\n> Inappropriate e-mail address, phone number\n> All is regarded as ad fraud except to only the below domains(raw-data will be shared by client regularly) @gmail.com @ezweb.ne.jp @docomo.ne.jp @icloud.com",
         "os_type":"Web",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":28753,
         "target_market":"Web",
         "today_remaining":"100",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/apps.apple.com\/kr\/app\/id1481554907",
         "end_date":"2999-12-31",
         "kpi":"Account Opening complete\n(Send a postback when account opening is completed.)",
         "payout":9600.0,
         "creatives":[
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85414_640x100.jpg"
            },
            {
               "dimen":"640x960",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85415_640x960.jpg"
            },
            {
               "dimen":"640x1320",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85416_640x1320.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85417_640x200.jpg"
            },
            {
               "dimen":"640x960",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85418_640x960.jpg"
            },
            {
               "dimen":"960x640",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85419_960x640.jpg"
            },
            {
               "dimen":"627x627",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85420_627x627.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85421_640x100.jpg"
            },
            {
               "dimen":"640x960",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85422_640x960.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85423_640x200.jpg"
            },
            {
               "dimen":"640x1320",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85424_640x1320.jpg"
            },
            {
               "dimen":"960x640",
               "url":"http:\/\/www.adhooah.com\/creative\/27564_f_85425_960x640.jpg"
            }
         ],
         "target_countries":"KR",
         "title":"FOSS(Korea Foss Securitie)(iOS)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=27564&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":0,
         "deduction":"Fraud traffic",
         "os_type":"iOS",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":27564,
         "target_market":"AppStore",
         "today_remaining":"0",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/app.adjust.com\/99h858j",
         "end_date":"2999-12-31",
         "kpi":"*Conversion action: Age authentication\n*Soft KPI:\n・current month ROAS 30%\n・registration rate 50%\n・OS version: iOS12 more",
         "payout":20400.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/drive\/folders\/1O1bW5h-VHugGN58PLnUYZ-1haeMkQCCI?usp=sharing"
            }
         ],
         "target_countries":"JP",
         "title":"Ikukuru iOS JP (Age verification)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28717&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":10,
         "deduction":"・OS version: iOS12 or less\n・the age certifications after the 48 hours from requesting stop\n・the age certifications from fraud registrations by the client system(Only excel data, No screenshot）\n*[[example report]]: https:\/\/drive.google.com\/drive\/folders\/1fL0KDcSNT5Y-4BfldhGlcZ7TGkRxOIYU",
         "os_type":"iOS",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":28717,
         "target_market":"AppStore",
         "today_remaining":"10",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.youmusic.magictiles",
         "end_date":"2999-12-31",
         "kpi":"Retention 50% \/  ROAS",
         "payout":200.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/drive\/folders\/19-2T_9r8bonOOaaUgsf-xqM5H1McSF7R?usp=sharing"
            }
         ],
         "target_countries":"KR",
         "title":"Magic tiles 3",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=27676&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":0,
         "deduction":"- Appsflyer P360 post-attribution detected fraud\n- The additional deduction can be discussed at the end of the campaign, which is suspected to be a fraud. \n- Fraud traffic is discussed separately\nFraud traffic example)\n1) If retention is high but in-app-event do not occur (tutorial or level complete, login, etc.)\n2) Numerous CTIT Less than 10s\n3) Strange SDK\n4) Numerous foreign traffic and overseas devices \/ OS rate, IP\/language\/device\/time-zone mismatch, unauthorized device *unauthorized device cannot be used in Korea(Googleplay not supported  or  Uncertified Device for domestic Use) \n5) Abnormal pattern (abrupt departures in a certain retention period \/ deviated from the certain level section etc.)\n6) Mismatch of mobile carrier (All traffic that does not exactly match KT, LG U+(LG+U%2B), SKTelecom)\n7) UID(User ID) mismatch\n8) Newly discovered new traffic besides the above typess",
         "os_type":"Android",
         "pay_type":"CPI",
         "currency":"KRW",
         "id":27676,
         "target_market":"GooglePlay",
         "today_remaining":"0",
         "event_postback":"af_interstitial_ads_seen, af_purchase, user_subscription, af_video_reward_ads_seen, FullAds_Finish, af_app_opened",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/apps.apple.com\/jp\/app\/id932394711",
         "end_date":"2999-12-31",
         "kpi":"■ Achievement point: af_level_n300　\n*Achieved level 300(Expected to arrive in 1-2 weeks after installation)",
         "payout":6800.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/open?id=1K3kPrF7i_cy1sWO1Wj-yvE5OzlQxNisb"
            }
         ],
         "target_countries":"JP",
         "title":"Nouen Konkatu JP iOS(level 300)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=27010&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":10,
         "deduction":"▼Among Sub ID-based AND Number of Installs = 10 or more(<- the accumulated number of install per month based on sub ID)\nApplies to any of these below;\n・ CTIT is longer than 24hours = 40％ or above\n・ CTIT is longer than 1hours = 60% or above\n・ CTIT is shorter than 10 seconds = 40% or above\n・ More than 80% of users' CTITs are within a specific 60 seconds.\n・ iOS ver is older than 12.1 (12.1 is OK, 12.0 is NG)  = 50％ or above\n・ Android OS ver is older than 5.1  (5.1 is OK, 5.0 is NG)= 50％ or above\n・ ITET is shorter than standard value = 50％ or above\n - If it is normal, it takes 3 minutes or more from installation to \"Tutorial complete\".\n・ Language setting on the device is not Japanese = 40% or above\n・1d RR(Retention Rate) is less than 10% (1d= next day of install date)\n・Mandatory event(s) is\/are skipped. Timing of fired event(s) discrepant.\n  (Eg. There is no membership registration fired, but some age verifications are fired.)\n・The total daily playing time is 0 seconds. (Applies to sub ID that has 1d retention)\n  (Eg. There are 500 users retaining from 0d to 2d, but each user didn\u2019t have playing time (=0 second of spending time in the app), all the conversions from the same sub ID will be eliminated.\n\n\n▼Among Main ID-based AND Number of Installs = 10 or more(<- the accumulated number of install per month based on sub ID)\nApplies to any of these below;\n・ CTIT is less than 10 seconds or longer than 24hours　= 40％ or above\n・ CTIT is longer than 1hours　= 60% or above\n\n\n\n▼Among users based\n・ CTIT is longer than 8hours\n・ CTIT is shorter than 10 seconds\n・ Language settings other than Japanese\n・ ITET is outlying *Set for each app\n・ Events are fired unrealistically\n(Eg. Purchase occurs even though the tutorial is not completed) *Set for each app\n・ Mandatory events are skipped (not fired). The timing of fired events contradict = 50% or more among all the conversion \n (Eg, The mandatory event is registration.  Registration=0, Age verification=3, and if the outlier is 50% or more among conversions.\nEven if mandatory events are not skipped, if the 1st event is skipped and the 2nd one is fired, or the 1st event is fired after the 2nd event is fired.)",
         "os_type":"iOS",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":27010,
         "target_market":"AppStore",
         "today_remaining":"10",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/apps.apple.com\/jp\/app\/id1460368148",
         "end_date":"2999-12-31",
         "kpi":"Conversion action: User billing\n*Flow: App install -> examination > prescription > \"User billing(Conversion action)\" > pills will be delivered",
         "payout":7900.0,
         "creatives":[
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/27671_f_78937_600x500.jpg"
            },
            {
               "dimen":"320x100",
               "url":"http:\/\/www.adhooah.com\/creative\/27671_f_78938_320x100.jpg"
            },
            {
               "dimen":"600x500",
               "url":"http:\/\/www.adhooah.com\/creative\/27671_f_78939_600x500.jpg"
            },
            {
               "dimen":"320x100",
               "url":"http:\/\/www.adhooah.com\/creative\/27671_f_78940_320x100.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/27671_f_78941_640x100.jpg"
            }
         ],
         "target_countries":"JP",
         "title":"Smarna JP iOS(User billing)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=27671&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":10,
         "deduction":"*Don't use ADPATRA \n\n\n(1) Non JP traffic \n- country code : jp only \n- language : ja-JP (ios) \n- carrier : only JP carriers acceptable (KDDI, au, NTT DOCOMO, SoftBank, Y!mobile) \n(2) under ctit 10 sec \n(3) If users login the app with email address, only below domains will be acceptable (raw-data will be shared by client regularly) @gmail.com @ezweb.ne.jp @docomo.ne.jp @icloud.com @yahoo.co.jp @au.com @softbank.ne.jp,",
         "os_type":"iOS",
         "pay_type":"CPI",
         "currency":"KRW",
         "id":27671,
         "target_market":"AppStore",
         "today_remaining":"10",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/www.adhooah.com\/aff\/event.event.main?action=cpatest",
         "end_date":"2999-12-31",
         "kpi":"Click 'Action complete' button",
         "payout":100.0,
         "creatives":[
            
         ],
         "target_countries":"All",
         "title":"TNK NCPA INTERGRATION TEST",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28265&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":0,
         "deduction":"Fraud Traffic",
         "os_type":"Web",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":28265,
         "target_market":"Web",
         "today_remaining":"0",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.tnkfactory.tnkadvertiser",
         "end_date":"2999-12-31",
         "kpi":"ROAS",
         "payout":0.12,
         "creatives":[
            {
               "dimen":"all",
               "url":"http:\/\/www.adhooah.com\/creative\/aaa.zip"
            },
            {
               "dimen":"1008x966",
               "url":"http:\/\/www.adhooah.com\/creative\/5_f_77416_1008x966.jpg"
            }
         ],
         "target_countries":"All",
         "title":"Tnk Advertiser (Intergration Test App)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=5&pub_id=8522&click_id=test_1922&sub_id=10009-22",
         "daily_cap":10,
         "deduction":"- D+1 리텐션(retention) 10% 미만(일간 신규 실행 10건 이상 발생시킨 서브펍 기준)\n- login 10% 미만(일간 신규 실행 10건 이상 발생시킨 서브펍 기준)\nfraud traffic",
         "os_type":"Android",
         "pay_type":"CPI",
         "currency":"USD",
         "id":5,
         "target_market":"GooglePlay",
         "today_remaining":"10",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/apps.apple.com\/jp\/app\/id750823886",
         "end_date":"2999-12-31",
         "kpi":"*Conversion action: Age authentication\n*Soft KPI: current month ROAS 10% or over \/ OS version: iOS12 more",
         "payout":15300.0,
         "creatives":[
            {
               "dimen":"all",
               "url":"https:\/\/drive.google.com\/drive\/folders\/1rSxSdqB_V1fWZ3TTNf06kNC37yNHmz_J?usp=sharing"
            }
         ],
         "target_countries":"JP",
         "title":"Wakuwaku iOS JP(Age authentication)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28716&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":10,
         "deduction":"・OS version: iOS12 or less \n・the Age authentications for out of Japan\n・the Age authentications after the 48 hours(2 bussines)\n・fraud Age authentications by the client system",
         "os_type":"iOS",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":28716,
         "target_market":"AppStore",
         "today_remaining":"10",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.dating.diamatch",
         "end_date":"2999-12-31",
         "kpi":"ROAS 100%",
         "payout":3600.0,
         "creatives":[
            {
               "dimen":"300x300",
               "url":"http:\/\/www.adhooah.com\/creative\/29042_f_85862_300x300.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/29042_f_85863_640x100.jpg"
            },
            {
               "dimen":"627x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29042_f_85864_627x627.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/29042_f_85865_640x200.jpg"
            },
            {
               "dimen":"960x640",
               "url":"http:\/\/www.adhooah.com\/creative\/29042_f_85866_960x640.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29042_f_85867_1200x627.jpg"
            }
         ],
         "target_countries":"KR",
         "title":"diamatch (registration)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=29042&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":0,
         "deduction":"- The additional deduction can be discussed at the end of the campaign, which is suspected to be a fraud. \n- Fraud traffic is discussed separately\nFraud traffic example)\n1) If retention is high but in-app-event do not occur (tutorial or level complete, login, etc.)\n2) Numerous CTIT Less than 10s\n3) Strange SDK\n4) Numerous foreign traffic and overseas devices \/ OS rate, IP\/language\/device\/time-zone mismatch, unauthorized device *unauthorized device cannot be used in Korea(Googleplay not supported  or  Uncertified Device for domestic Use) \n5) Abnormal pattern (abrupt departures in a certain retention period \/ deviated from the certain level section etc.)\n6) Mismatch of mobile carrier (All traffic that does not exactly match KT, LG U+(LG+U%2B), SKTelecom)\n7) UID(User ID) mismatch\n8) Newly discovered new traffic besides the above typess",
         "os_type":"Android",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":29042,
         "target_market":"GooglePlay",
         "today_remaining":"0",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/lineagem.plaync.com\/preorder\/record\/210115\/index?LM=120230",
         "end_date":"2999-12-31",
         "kpi":"Pre-registration complete",
         "payout":1800.0,
         "creatives":[
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85972_640x200.jpg"
            },
            {
               "dimen":"640x960",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85973_640x960.jpg"
            },
            {
               "dimen":"640x1320",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85974_640x1320.jpg"
            },
            {
               "dimen":"720x320",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85975_720x320.jpg"
            },
            {
               "dimen":"960x640",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85976_960x640.jpg"
            },
            {
               "dimen":"1080x1080",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85977_1080x1080.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85978_1200x627.jpg"
            },
            {
               "dimen":"1200x748",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85979_1200x748.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85980_300x250.jpg"
            },
            {
               "dimen":"300x600",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85981_300x600.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85982_320x50.jpg"
            },
            {
               "dimen":"320x480",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85983_320x480.jpg"
            },
            {
               "dimen":"480x320",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85984_480x320.jpg"
            },
            {
               "dimen":"600x300",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85985_600x300.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85986_640x100.jpg"
            },
            {
               "dimen":"640x1320",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85987_640x1320.jpg"
            },
            {
               "dimen":"960x640",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85988_960x640.jpg"
            },
            {
               "dimen":"1200x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85989_1200x627.jpg"
            },
            {
               "dimen":"1200x748",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85990_1200x748.jpg"
            },
            {
               "dimen":"250x250",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85991_250x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85992_300x250.jpg"
            },
            {
               "dimen":"300x600",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85993_300x600.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85994_320x50.jpg"
            },
            {
               "dimen":"320x480",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85995_320x480.jpg"
            },
            {
               "dimen":"480x320",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85996_480x320.jpg"
            },
            {
               "dimen":"600x300",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85997_600x300.jpg"
            },
            {
               "dimen":"627x627",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85998_627x627.jpg"
            },
            {
               "dimen":"640x100",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_85999_640x100.jpg"
            },
            {
               "dimen":"640x200",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_86000_640x200.jpg"
            },
            {
               "dimen":"640x960",
               "url":"http:\/\/www.adhooah.com\/creative\/29059_f_86001_640x960.jpg"
            }
         ],
         "target_countries":"KR",
         "title":"lineagem Pre-registration",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=29059&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":0,
         "deduction":"Fraud traffic",
         "os_type":"Web",
         "pay_type":"CPA",
         "currency":"KRW",
         "id":29059,
         "target_market":"Web",
         "today_remaining":"0",
         "event_postback":"",
         "status":"Live",
         "traffic":"Non-Incent"
      },
      {
         "preview":"https:\/\/apps.apple.com\/jp\/app\/id1321349856",
         "end_date":"2999-12-31",
         "kpi":"Conversion action: the number of men paying members",
         "payout":45000.0,
         "creatives":[
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83513_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83514_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83515_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83516_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83517_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83518_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83519_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83520_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83521_300x250.jpg"
            },
            {
               "dimen":"300x250",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83522_300x250.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83523_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83524_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83525_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83526_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83527_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83528_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83529_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83530_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83531_320x50.jpg"
            },
            {
               "dimen":"320x50",
               "url":"http:\/\/www.adhooah.com\/creative\/28504_f_83532_320x50.jpg"
            }
         ],
         "target_countries":"JP",
         "title":"paddy67 iOS JP(Men paid membership registration)",
         "url":"https:\/\/api.adhooah.com\/aff\/api.click.main?campn_id=28504&pub_id=8522&click_id=dummy_click_id_123&sub_id=1004",
         "daily_cap":10,
         "deduction":"If there is a fraud doubt survey",
         "os_type":"iOS",
         "pay_type":"CPI",
         "currency":"KRW",
         "id":28504,
         "target_market":"AppStore",
         "today_remaining":"10",
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
```
https://www.adhooah.com/aff/api/v2/approvalrequest?pid=7c9704d674ec0156782e123e92c3d2a3&campaign_id=20625
```
*output
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
*your event postback url (optional)
```
http://YOUR_EVENT_POSTBACK_URL?click_id={click_id}&sub_id={sub_id}&device_id={adid_or_ifa}&ip={ipaddr}&event={event_nm}
```
  
  

* If you need support, please email to performance@tnkfactory.com



