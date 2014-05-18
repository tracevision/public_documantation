### Standard Response JSON
Successful response with array for data
```javascript
{
	success: true,
	data: [{},{},{}]
}
```
And response code HTTP 200

Successful response with dictionary for data
```javascript
{
	success: true,
	data: { prop: val, prop1: val}
}
```
And response code HTTP 200

Failure response
```javascript
{
	success: false,
	error: { id: “invalid_api_key”, message: “Invalid API key” }
}
```
And response code HTTP 3xx, 4xx, 5xx

### Support of different sport types
Each sport type will have it’s own base address, e.g., alpinereplay.com and bikereplay.com, or alpine.activereplay.com and surf.activereplay.com.

### Base For Calls
/api/v1/
