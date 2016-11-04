---
title: API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='http://howfintech.com'>Powered by HowFintech</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the 好好投資 API! You can use our API to access fund API endpoints, which can get information on various funds.

endpoints: `http://howfintech.com/api/v0`

If you have any question, please feel free to contact wilson@howfintech.com.

# Authentication

> Make sure to replace `2c0a50b4a76d83d77cae1f859a40de55c0b07877` with your API key.

好好投資 uses API keys to allow access to the API. You can use public alpha API key: 2c0a50b4a76d83d77cae1f859a40de55c0b07877

好好投資 expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: 2c0a50b4a76d83d77cae1f859a40de55c0b07877`

<aside class="notice">
You must replace 2c0a50b4a76d83d77cae1f859a40de55c0b07877 with your personal API key.
</aside>

# Fund

## list

> The above command returns JSON structured like this:

```json
[
  "保德信中國好時平衡證券投資信託基金－人民幣月配息型",
  "保德信中國好時平衡證券投資信託基金－美元月配息型",
  "元大全球不動產證券化證券投資信託基金-人民幣",
  "元大美元傘型證券投資信託基金之元大全球美元公司債券證券投資信託基金-美元(A)不配息",
  "安本環球日本小型公司基金X - 2 類",
  "安本環球日本股票基金X - 2 類",
  "安本環球拉丁美洲股票基金X - 2 類",
  "安本環球歐元高收益債券基金X - 1 類",
  "安本環球澳洲股票基金X - 2 類",
  "永豐標普東南亞指數證券投資信託基金美元",
  "安本環球新興市場公司債券基金X - 2 類",
  "安本環球新興市場當地貨幣債券基金X - 1 類",
  "安本環球新興市場當地貨幣債券基金X - 2 類"
]
```

This endpoint retrieves all funds Chinese name list.

### HTTP Request

`GET http://howfintech.com/api/v0/fund/list`

### Query Parameters

Parameter | Type | Required | Description | Example
--------- | ---- | -------- | ----------- | -------
N/A       | N/A  | N/A      | N/A         | N/A

<aside class="success">
Remember to put your API key in header!
</aside>

## detail

> The above command returns JSON structured like this:

```json
{
  "fundChineseName": "瀚亞亞太豐收平衡基金A類型-人民幣",
  "agentChineseName": "---",
  "fundManager": "---",
  "latestNavDate": "---",
  "latestNav": "---",
  "highestInYearNav": "---",
  "lowestInYearNav": "---",
  "returnRateDate": "---",
  "returnRateFromM": 0.82671,
  "returnRateFromQ": 5.99944,
  "returnRateFromY": 11.81737,
  "category": "---",
  "initialAsset": "---",
  "riskLevel": "---",
  "foundDate": "20141208",
  "region": "---",
  "netAsset": 585715564.2,
  "totalAssetDate": "---",
  "managementFee": 1.6,
  "costodianFee": "---",
  "otherCurrencyType": [
    "---"
  ],
  "fundShareholding": [
    "---"
  ],
  "graph": {
    "3M": [],
    "6M": [],
    "1Y": [],
    "2Y": [],
    "3Y": []
  },
  "documentDownload": "---",
  "bemchmark": "---",
  "investmentStrategy": "原則上,本基金自成立日起屆滿三個月後,投資於股票(含承銷股票),存託憑證,債券及其他固定收益證券之總金額應達本基金淨資產價值之百分之七十以上;投資於國內外股票(含承銷股票)及存託憑證之總金額不得高於本基金淨資產價值之百分之九十(含)且不得低於百分之十(含);投資於外國有價證券之總金額不得低於本基金淨資產價值之百分之六十(含);投資於前述亞太國家或地區之有價證券總金額不得低於本基金淨資產價值之百分之六十(含);投資所在國或地區之國家主權評等未達公開說明書所列信用評等機構評定等級者,投資該國或地區之政府債券及其他債券總金額,不得超過本基金淨資產價值之百分之三十.",
  "service": "---"
}
```

This endpoint retrieves a specific fund detail.

### HTTP Request

`GET http://howfintech.com/api/v0/fund/detail`

### URL Parameters

Parameter | Type    | Required | Description | Example
--------- | ------- | -------- | ----------- | -------
name      | string  | required | Full name you want to find. | 瀚亞亞太豐收平衡基金A類型-人民幣
