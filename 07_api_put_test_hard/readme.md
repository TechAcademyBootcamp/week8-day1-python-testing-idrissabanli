Test the blogger functionality using the provided API documentation.
### API DOCS:
1. http://35.225.243.133/api-documentation/
2. http://35.225.243.133/redoc/
### Test Case 1:
url: http://35.225.243.133/bloggers/1/
PUT VALID DATA:
```
{
    full_name: "Idris Blogger"
}
```
Expected status code: 200
Expected response:
```
{
    id:	integer
    full_name:	"Idris Blogger"
    created_at	($date-time)
    updated_at ($date-time)
}
```
1. Check Status code is `200`
2. Check `full_name` is `"Idris Blogger"` from response
### Test Case 2:
url: http://35.225.243.133/bloggers/1/
PUT INVALID DATA:
```
{
    full_name: "abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd abcd "
}
```
Expected status code: 400
Expected response:
```
{
  "full_name": ["Ensure this field has no more than 180 characters."]
}
```
1. Check Status code is `400`
2. Check `full_name` is `["Ensure this field has no more than 180 characters."]` from response
### Test Case 3:
url: http://35.225.243.133/bloggers/1/
PUT INVALID DATA:
```
{}
```
Expected status code: 400
Expected response:
```
{
  "full_name": ["This field is required."]
}
```
1. Check Status code is `400`
2. Check `full_name` is `["This field is required."]` from response
### Test Case 4:
url: http://35.225.243.133/bloggers/1/
PUT INVALID DATA:
```
{
"id": 1223
}
```
Expected status code: 400
Expected response:
```
{
  "full_name": ["This field is required."]
}
```
1. Check Status code is `400`
2. Check `full_name` is `["This field is required."]` from response