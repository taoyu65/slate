---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the USYNO API!


This example API documentation page was created with [Slate](https://github.com/lord/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Admin

## Reference

```shell
curl "https://us-central1-currencyclub-demo.cloudfunctions.net/"
```

```javascript

```

> The above command returns JSON structured like this:

```json
[
  {
    "code": "EXAMPLE",
    "title": "This is example",
    "amount": 100,
    "createdAt": 12312312
  }
]
```

### HTTP Response

Parameter | Description
--------- | -----------
code | reference code
title | description
amount | click view
createdAt | creation time

### HTTP Request

`GET https://us-central1-currencyclub-demo.cloudfunctions.net/api/reference`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
null|null|null

<aside class="success">
This API is for getting all reference
</aside>

# User

## User LogIn

```shell
curl "http://airswapnodejs.us-east-1.elasticbeanstalk.com/api/userSignin"
  # -H "Authorization: meowmeowmeow"
```

```javascript

```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  }
]
```

### HTTP Request

`POST http://airswapnodejs.us-east-1.elasticbeanstalk.com/api/userSignin`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
email | null | Email for user login.
password | null | Password cannot be empty.

<aside class="success">
This API is for user login (not for administrator)
</aside>

## Get User Info

```shell
curl "http://airswapnodejs.us-east-1.elasticbeanstalk.com/api/userSignin"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

