# LAT-Invest<sup>&reg;</sup> (LTI2.0): API Documentation for Institutional Investors
**Warning**: LAT-Invest (LTI 2.0) is a trading algorithm developed by LateralCoin (Singapore) for INSTITUTIONAL use ONLY. **LAT-Invest is NOT for sale**. Beware of scams using the name of our company / algorithms. 
<hr />

## Rest API for LAT-Invest<sup>&reg;</sup> LTI2.0 (2021-01-29)

### General API Information
* The base endpoint is: **https://api-server0.lateralcoin.com/**
* If there are performance issues with the endpoint above, these API clusters are also available:
  * **https://api-server1.lateralcoin.com/**
  * **https://api-server2.lateralcoin.com/**
* All endpoints return either a JSON object or array.

### HTTP Return Codes

* HTTP `4XX` return codes are used for malformed requests;
  the issue is on the sender's side.
* HTTP `403` return code is used when the WAF Limit (Web Application Firewall) has been violated.
* HTTP `429` return code is used when breaking a request rate limit.
* HTTP `418` return code is used when an IP has been auto-banned for continuing to send requests after receiving `429` codes.
* HTTP `5XX` return codes are used for internal errors; the issue is on
  LateralCoin's side.
  
## General Information on Endpoints
* For `GET` endpoints, parameters must be sent as a `query string`.
* For `POST`, `PUT`, and `DELETE` endpoints, the parameters may be sent as a
  `query string` or in the `request body` with content type
  `application/x-www-form-urlencoded`. You may mix parameters between both the
  `query string` and `request body` if you wish to do so.
* Parameters may be sent in any order.
* If a parameter sent in both the `query string` and `request body`, the
  `query string` parameter will be used.
  
  
