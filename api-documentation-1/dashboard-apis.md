# Dashboard APIs

{% api-method method="post" host="https://market-mfund-development.herokuapp.com/" path="api/admin/authentication/login/" %}
{% api-method-summary %}
Login Admin
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows user to login and get JWT tokens from Node Server. Before making this request, firebase authentication must be made from admin app and Firebase JWT token is send in body for verification.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=true %}
Password of the respective admin
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Email Id of the admin
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
On Successful Login
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "access_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MzcsImVtYWlsIjoidmlyYWxzQGdlZWt5YW50cy5jb20iLCJpc0FkbWluIjp0cnVlLCJpYXQiOjE2MDg3MjAzNDQsImV4cCI6MTYwODgwNjc0NCwiYXVkIjoibWFya2V0LW1mdW5kLXVzZXJzIiwiaXNzIjoiZ2Vla3lhbnRzIn0.mxZ52tCdBPZyi567mkp68dwouI_hEjOMP40ym0nawmkrxp5mgdzMrD83as_inp5suqhopcoGVDhKZc3wEXTpmAkVHYownl19vqzqXLVe8tb8x_mWQrMtp_SNRifKYseanriLW6_LotXaQarfehZ-__-1GHGLbmWSbZjFmE6zUSvdJUxSiGtZd0K6CIKMZoBwQKTHCoYqRUAAyUlVue5Q4EZJFC8BU2NBKY_RrcvTlh9qRewwRiCfha4dZBbb22vbQNsON0OITLdvNIPsEavHYh54J8NvItFfuReNP9gJQkjSVbUZwImldQBbmTwEynMaR8bGDxboRQ14ktq-47mvIY0dYAUwiyDLjK_Tyg1EvswYDLOweUpW6KWWnTJh3xM2VhZPMkmeyjnYa_vUyuwNdc3uP28i9VEhr4uyTkCfzlCJJ_rZx-1h-lq1bNWNpDkW6ZItO0m_rD-OWP8svjqpuKjwc7S2xWsxMJlr6sfyBKQHPqMr7BDlWilp7PRLUBt_FXj-7_Fnk8Df9zBIC8oWvg-WwbMo6ES9zD6vt7fHag91fPuwFpALcwqp2N2qrrZGtTCowowYHgP6SmDo-P0Z_CCCyh3plZqB5e8eFNQVhSulRuZnv_o8ylF_kJCEdBr7cecPrCBF-YF9_wIPVg8BApJL5iHBgk6dXxPOdtUVbrE",
    "refresh_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MzcsImVtYWlsIjoidmlyYWxzQGdlZWt5YW50cy5jb20iLCJpc0FkbWluIjp0cnVlLCJpc1JlZnJlc2hUb2tlbiI6dHJ1ZSwiaWF0IjoxNjA4NzIwMzQ0LCJleHAiOjE2MDkzMjUxNDQsImF1ZCI6Im1hcmtldC1tZnVuZC11c2VycyIsImlzcyI6ImdlZWt5YW50cyJ9.xqrYvwui25QKLdr0s6iWMM0h3xuQmden5Aa_iZvZGM5IG0dxOV59_GNF9geRvpZ7Hjqy7bn0V8vcCqTpH9f4WJGJxN53kawpuzbehH_PxMVMHe8GpuSdCm4tW_LnPQiJ6Y0w8vYrUf5aYzlXWn4p-2YLqEKWEVoEvov_RDzddZAGxVoaSHNOF9rcDDgLyPmxCHd8L2DnyrFkhclYXQ5bu7YEgaiQiVcbllEjWWUH94nyzX3x_TyB-odnIXLEGoJZdkZuaFG3iTlB46W8muZgzU5ey6QaT0V3ZiiQDjfUPlXbR2Hx0trbXMtUAXZnXnlXmB6eKPKqGoC23hLfUsrtiatwAqH5qMuFavHL4tCMfEofKwdiJcL3msVw3sD9eBxrTtdYCiLo1JTyAm7gFhJpflwVIEYwGLSBxBWCMctB_eO9j_v4CM3s6QSra-XVzOe_EjBbwjFWPwUcbY9E1WcttbHnAtLLc8Q2AoaQv5A72LqTkPMV6hjzULmfRhPLMHIxJHlpmVXG9zxfl5biM1AFPjyRmW6O2Y3vdP7XuVpmloNpqYQmx4FtH-elKdkS8HdxCFjQ20wWrcHiF08-R-gdoqKgRB5f4cqlKmsl0DZLEkPyaUVCzyGkAjfT0IIIMR62WqEjYtrBY5bpnVtXqUl0Ro3B-xs3HiPtE-Kz3BnPl5s"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://market-mfund-development.herokuapp.com/" path="api/admin/authentication/add\_admin/" %}
{% api-method-summary %}
Add Admin
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows to create an admin in the postgreSQL database . This API requires JWT access token which is retrieved from Login Admin API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer eyjhbg.....
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=true %}
Password to be associated with the respective admin
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Email Id to be registered
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Admin has been created successfully.
{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://market-mfund-development.herokuapp.com/" path="api/admin/change\_password" %}
{% api-method-summary %}
Change Password
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows admin to change his/her current password. This API requires JWT access token which is retrieved from Login Admin API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer ejhyzn...
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="newPassword" type="string" required=true %}
New Password for admin
{% endapi-method-parameter %}

{% api-method-parameter name="oldPassword" type="string" required=true %}
Current password of admin
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://market-mfund-development.herokuapp.com/" path="api/admin/home/" %}
{% api-method-summary %}
Home API
{% endapi-method-summary %}

{% api-method-description %}
This Api will retrieve all the information displayed on the home page of admin app. This API requires JWT access token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer eyjhbg....
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Will get the total number of investors and the total investment
{% endapi-method-response-example-description %}

```
{
    "userCount": 6,
    "totalInvestments": 17000
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://market-mfund-development.herokuapp.com/" path="api/admin/home/organisations" %}
{% api-method-summary %}
Organisations API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve all the information about organisations. This API requires JWT access token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer eyjhbg...
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Details of all the organisations
{% endapi-method-response-example-description %}

```
[
    {
        "name": "Axis Bluechip Fund Direct Plan Growth",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FAxis.png?alt=media&token=70443f42-43aa-463b-9762-a33aa25eb8aa",
        "xirr": "10%",
        "currentValue": 489,
        "returns": "123",
        "currentValueChange": "+0.54%",
        "returnsChange": "-0.54%",
        "rating": 3.5
    },
    {
        "name": "Reliance Small Cap Fund Direct Growth",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FReliance.png?alt=media&token=432ad8b7-6825-42c4-affc-9943e813a7ef",
        "xirr": "20%",
        "currentValue": 758,
        "returns": "657",
        "currentValueChange": "+0.54%",
        "returnsChange": "-0.54%",
        "rating": 4
    },
    {
        "name": "Icici Prudential Bluechip Fund Direct Growth",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2Ficici_logo.png?alt=media&token=762fe9a2-7308-413e-a956-d23b6bae9f03",
        "xirr": "15%",
        "currentValue": 882,
        "returns": "455",
        "currentValueChange": "+0.54%",
        "returnsChange": "-0.54%",
        "rating": 2.5
    },
    {
        "name": "Tesla",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FAxis.png?alt=media&token=70443f42-43aa-463b-9762-a33aa25eb8aa",
        "xirr": "12%",
        "currentValue": 2345,
        "returns": "456",
        "currentValueChange": "+0.54%",
        "returnsChange": "-0.54%",
        "rating": 3.5
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://market-mfund-development.herokuapp.com/" path="api/admin/notifications" %}
{% api-method-summary %}
Notification API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve all the Notifications. This API requires JWT access token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer eyjhbg...
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
All the notifications of a specific admin.
{% endapi-method-response-example-description %}

```
[
    {
        "id": 25,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:06 AM"
    },
    {
        "id": 26,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:08 AM"
    },
    {
        "id": 27,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:10 AM"
    },
    {
        "id": 28,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:13 AM"
    },
    {
        "id": 29,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:16 AM"
    },
    {
        "id": 30,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:33 AM"
    },
    {
        "id": 31,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:38 AM"
    },
    {
        "id": 32,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 12:40 AM"
    },
    {
        "id": 33,
        "title": "New organisation created",
        "description": "New organisation has been successfully created.",
        "badge": "New organisation",
        "createdAt": "22 Dec 2020 1:04 PM"
    },
    {
        "id": 34,
        "title": "New admin created",
        "description": "New admin has been successfully created.",
        "badge": "New admin",
        "createdAt": "23 Dec 2020 12:17 AM"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://market-mfund-development.herokuapp.com/" path="api/admin/notifications" %}
{% api-method-summary %}
Notifications API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will delete all the notifications associated with a specific admin.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer eyjhbg...
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Success as all notifications are deleted.
{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://market-mfund-development.herokuapp.com/" path="api/admin/add\_new\_organisation" %}
{% api-method-summary %}
Add Organisation API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows an admin to add organisations in the database.This API requires JWT token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="returns" type="string" required=true %}
returns of the organisation
{% endapi-method-parameter %}

{% api-method-parameter name="currentValue" type="string" required=true %}
current value of organisation
{% endapi-method-parameter %}

{% api-method-parameter name="xirr" type="string" required=true %}
xirr of organisation
{% endapi-method-parameter %}

{% api-method-parameter name="schemeName" type="string" required=true %}
Name of the organisation to be added
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully added an organisation.
{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://market-mfund-development.herokuapp.com/" path="api/admin/balances" %}
{% api-method-summary %}
Balances API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve all the balances of the organisations. This API requires JWT token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved all the balance amount.
{% endapi-method-response-example-description %}

```
[
    {
        "schemeName": "Axis Bluechip Fund Direct Plan Growth",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FAxis.png?alt=media&token=70443f42-43aa-463b-9762-a33aa25eb8aa",
        "amount": "$6000"
    },
    {
        "schemeName": "Reliance Small Cap Fund Direct Growth",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FReliance.png?alt=media&token=432ad8b7-6825-42c4-affc-9943e813a7ef",
        "amount": "$11000"
    },
    {
        "schemeName": "Icici Prudential Bluechip Fund Direct Growth",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2Ficici_logo.png?alt=media&token=762fe9a2-7308-413e-a956-d23b6bae9f03",
        "amount": "$0"
    },
    {
        "schemeName": "Tesla",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FAxis.png?alt=media&token=70443f42-43aa-463b-9762-a33aa25eb8aa",
        "amount": "$0"
    },
    {
        "schemeName": "Amazon",
        "image": "https://firebasestorage.googleapis.com/v0/b/market-mfund-development.appspot.com/o/Organization-logo-image%2FAxis.png?alt=media&token=70443f42-43aa-463b-9762-a33aa25eb8aa",
        "amount": "$0"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://market-mfund-development.herokuapp.com/" path="api/admin/transaction\_details" %}
{% api-method-summary %}
Transactions API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve the transaction details made by a specific user. This API requires JWT token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved Transactions.
{% endapi-method-response-example-description %}

```
[
    {
        "userFullName": "Testing",
        "schemeName": "Axis Bluechip Fund Direct Plan Growth",
        "amount": "1000",
        "paymentMode": "net_banking",
        "dateOfInvestments": "365 Days",
        "status": "3 Dec 2020 3:53 AM"
    },
    {
        "userFullName": "Madhav Bansal",
        "schemeName": "Axis Bluechip Fund Direct Plan Growth",
        "amount": "5000",
        "paymentMode": "Debit card",
        "dateOfInvestments": "1095 Days",
        "status": "7 Dec 2020 5:42 AM"
    },
    {
        "userFullName": "Devanshi Garg",
        "schemeName": "Reliance Small Cap Fund Direct Growth",
        "amount": "10000",
        "paymentMode": "DebitCard",
        "dateOfInvestments": "1095 Days",
        "status": "30 Nov 2020 6:27 AM"
    },
    {
        "userFullName": "Devanshi Garg",
        "schemeName": "Reliance Small Cap Fund Direct Growth",
        "amount": "1000",
        "paymentMode": "DebitCard",
        "dateOfInvestments": "1825 Days",
        "status": "30 Nov 2020 6:42 AM"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://market-mfund-development.herokuapp.com/" path="api/admin/investors" %}
{% api-method-summary %}
Investors API
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will retrieve the Investors details. This API requires JWT token which is retrieved from Login API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved Investors.
{% endapi-method-response-example-description %}

```
[
    {
        "userFullName": "Testing",
        "schemeName": "Axis Bluechip Fund Direct Plan Growth",
        "currentValue": "$489",
        "returns": "$4405.56",
        "currentValueRate": "+0.54%",
        "returnsRate": "-0.54%",
        "duration": "365 Days",
        "status": "Running"
    },
    {
        "userFullName": "Madhav Bansal",
        "schemeName": "Axis Bluechip Fund Direct Plan Growth",
        "currentValue": "$489",
        "returns": "$4405.56",
        "currentValueRate": "+0.54%",
        "returnsRate": "-0.54%",
        "duration": "1095 Days",
        "status": "Running"
    },
    {
        "userFullName": "Devanshi Garg",
        "schemeName": "Reliance Small Cap Fund Direct Growth",
        "currentValue": "$758",
        "returns": "$4405.56",
        "currentValueRate": "+0.54%",
        "returnsRate": "-0.54%",
        "duration": "1095 Days",
        "status": "Running"
    },
    {
        "userFullName": "Devanshi Garg",
        "schemeName": "Reliance Small Cap Fund Direct Growth",
        "currentValue": "$758",
        "returns": "$4405.56",
        "currentValueRate": "+0.54%",
        "returnsRate": "-0.54%",
        "duration": "1825 Days",
        "status": "Running"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

