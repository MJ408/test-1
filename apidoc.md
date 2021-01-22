<div class="ui segment">
		<h2>1.Campaign List</h2>
		<p>&nbsp;</p>
		<p>1.1 get available campaigns</p>
		<p>https://www.adhooah.com/aff/api/v2/availablecampaigns?pid=&lt;API_KEY&gt;</p>
		<p>- &lt;API_KEY&gt; : &nbsp;Your API Key.</p>
		<p>
			<br>
			<br>
		</p>
		<p>1.2 get my live campaigns</p>
		<p>https://www.adhooah.com/aff/api/v2/mycampaigns?pid=&lt;API_KEY&gt;</p>
		<p>- &lt;API_KEY&gt; : &nbsp;Your API Key.</p>
		<p>&nbsp;</p>
		<p>1.3 json result</p>
		<p>{"return": result code, &nbsp;"campaigns":[list]}</p>
		<p>&nbsp;</p>
		<table>
			<tbody>
				<tr>
					<td>
						<p>result code</p>
					</td>
					<td>
						<p>Description</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>0</p>
					</td>
					<td>
						<p>success</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>2</p>
					</td>
					<td>
						<p>no campaigns</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>4</p>
					</td>
					<td>
						<p>wrong api key</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>9</p>
					</td>
					<td>
						<p>system error</p>
					</td>
				</tr>
			</tbody>
		</table>
		<p>
			<br>
			<br>
		</p>
		<p>campaigns [list]</p>
		<p>&nbsp;</p>
		<table>
			<tbody>
				<tr>
					<td>
						<p>Column</p>
					</td>
					<td>
						<p>Description</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>title</p>
					</td>
					<td>
						<p>campaign title</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>id</p>
					</td>
					<td>
						<p>campaign ID</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>url</p>
					</td>
					<td>
						<p>campaign URL</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>pay_type</p>
					</td>
					<td>
						<p>CPI or CPA</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>payout</p>
					</td>
					<td>
						<p>payout</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>daily_cap</p>
					</td>
					<td>
						<p>daily cap</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>status</p>
					</td>
					<td>
						<p>campaign status (ex, Live, Stop, Available)</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>currency</p>
					</td>
					<td>
						<p>payout currency</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>preview</p>
					</td>
					<td>
						<p>campaign preview</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>traffic</p>
					</td>
					<td>
						<p>Incentive or Non-Incentive</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>kpi</p>
					</td>
					<td>
						<p>campaign KPI</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>end_date</p>
					</td>
					<td>
						<p>campaign end date</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>today_remaining</p>
					</td>
					<td>
						<p>number lef today</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>deduction</p>
					</td>
					<td>
						<p>deduction condition</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>os_type</p>
					</td>
					<td>
						<p>Andorid or IOS or mobile Web</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>target_countries</p>
					</td>
					<td>
						<p>targeted countries (ex, KR, US, …)</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>target_market</p>
					</td>
					<td>
						<p>targeted market (ex, GooglePlay, AppStore, Web)</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>event_postback</p>
					</td>
					<td>
						<p>event postback name. (ex, login, level_3, purchae, …
							)</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>creatives</p>
					</td>
					<td>
						<p>[list] {dimen, url}</p>
					</td>
				</tr>
			</tbody>
		</table>
		<p>
			<br>
			<br>
			<br>
		</p>
		<p>(example)</p>
		<p>*request</p>
		<p>https://www.adhooah.com/aff/api/v2/mycampaigns?pid=1ab17f073f4ffd28f8646a784e3a36e5</p>
		<p>&nbsp;</p>
		<p>*output</p>
		<p>{"return":0,
			"campaigns":[{"preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.webzen.muorigin2.google","end_date":"2999-12-31","kpi":"Login
			60%
			more","payout":3.0,"creatives":[{"dimen":"640x1320","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_30077_1.jpg"},{"dimen":"1040x585","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_30077_2.jpg"},{"dimen":"640x640","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_30077_3.jpg"}],"target_countries":"KR","title":"MU
			Origin2","url":"http:\/\/tnkd.tnkfactory.com\/tnk\/api\/ref\/c3\/21009\/22727\/c030e0b0-4001-847c-c748-1004090c0f02\/{transaction_id}?sub_id={sub_id}","daily_cap":500,"deduction":"
			based on 1 more install sub_id\/daily&lt;br&gt; D+1 Retention 50%
			more = 100% payout&lt;br&gt; D+1 Retention 30%~50% = 90%
			payout&lt;br&gt; D+1 Retention 10%~30% = 70% payout&lt;br&gt; D+1
			Retention 10% less = no
			payout","os_type":"Android","pay_type":"CPI","currency":"USD","id":21009,"target_market":"GooglePlay","today_remaining":"500","event_postback":"","status":"Live","traffic":"Non-Incent"},{"preview":"https:\/\/play.google.com\/store\/apps\/details?id=com.efunkr.ql.google","end_date":"2999-12-31","kpi":"","payout":4000.0,"creatives":[{"dimen":"640x1320","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_22690_1.jpg"},{"dimen":"1040x585","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_22690_2.jpg"},{"dimen":"640x640","url":"http:\/\/cdn3.tnkfactory.com\/fad\/ci_22690_3.jpg"}],"target_countries":"KR","title":"The
			Rulers","url":"http:\/\/tnkd.tnkfactory.com\/tnk\/api\/ref\/c3\/18113\/22259\/c030e0b0-4001-847c-c748-1004090c0f02\/{transaction_id}?sub_id={sub_id}","daily_cap":10,"deduction":"","os_type":"Android","pay_type":"CPI","currency":"KRW","id":18113,"target_market":"GooglePlay","today_remaining":"10","event_postback":"","status":"Live","traffic":"Non-Incent"}]}</p>
		<p>
			<br>
			<br>
			<br>
		</p>
		<p>1.4 campaign approval request</p>
		<p>https://www.adhooah.com/aff/api/v2/approvalrequest?pid=&lt;API_KEY&gt;&amp;campaign_id=&lt;CAMPAIGN_ID&gt;</p>
		<p>- &lt;API_KEY&gt; : &nbsp;Your API Key.</p>
		<p>- &lt;CAMPAIGN_ID &gt; : campaign id</p>
		<p>&nbsp;</p>
		<p>{"return": result code}</p>
		<p>&nbsp;</p>
		<table>
			<tbody>
				<tr>
					<td>
						<p>result code</p>
					</td>
					<td>
						<p>Description</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>0</p>
					</td>
					<td>
						<p>success</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>2</p>
					</td>
					<td>
						<p>campaign id or campaign state is wrong.(not available)</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>4</p>
					</td>
					<td>
						<p>wrong api key</p>
					</td>
				</tr>
				<tr>
					<td>
						<p>9</p>
					</td>
					<td>
						<p>system error</p>
					</td>
				</tr>
			</tbody>
		</table>
		<p>
			<br>
			<br>
		</p>
		<p>(example)</p>
		<p>https://www.adhooah.com/aff/api/v2/approvalrequest?pid=7c9704d674ec0156782e123e92c3d2a3&amp;campaign_id=20625</p>
		<p>&nbsp;</p>
		<p>*output</p>
		<p>{"return": 0}</p>
		<p>
			<br>
			<br>
			<br>
			<br>
			<br>
		</p>





</div>
