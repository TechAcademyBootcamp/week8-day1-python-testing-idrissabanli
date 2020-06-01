# 404 requests

Ask the user to enter a link. Check for such a page by sending a request with `requests` to the incoming link. 
If the page exists, print `200 success`, if not, print `404 not found`.

## Input 1:
`http://python.org/`
## Output 1
`200 success`

## Input 2:
`https://www.python.org/abc`
## Output 2
`404 not found`