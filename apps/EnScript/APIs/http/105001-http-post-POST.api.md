# HTTP Post method call

## en.http.post

### Warning: DO NOT CALL THIS API MORE THAN ONCE IN ONE API. IF YOUR API takes more than 20 seconds, your API could be disabled as unstable API by EnMobi.



Name            | Description
----------------|-------------
results         | Results variable where the results are stored
url             | The URL to post a request
queryString     | (Optional) A JSON object with key value to be posted. The values has to basic data types like String, Long, Integer, Double. This will be added as query string to the URL.
formFields       | (Optional) A JSON object with key value to be posted. The values has to basic data types like String, Long, Integer, Double.
body            | (Optional) Body can be a JSON object or a String. If String, it will be directly submitted. If the body is JSON object, it will be converted to JSON string and submitted.
header          | (Optional) A JSON object with key value to be posted. The values has to basic data types like String, Long, Integer, Double. All header values will be posted as String data type.
basicAuth       | (Optional) A JSON object that contains 'user' and 'password' attributes with values. Both user and password must be existing in order for auth to be used.
fileContent     | (Optional) An EnMobi Attachment Object or  or Attachment binary


All optional parameters can be null.


## Example 1: Post

```
<% assign url  = "https://postman-echo.com/post" %>

<% assign queryString.firstName = 'John' %>
<% assign queryString.lastName  = 'Doe' %>

<% assign formFields.field1  = 'Field 1 Value' %>
<% assign formFields.field2  = 2000 %>
<% assign formFields.field3  = 200.55 %>

<% assign bodyString  = "This is body string" %>

<% assign header.header1  = 'Header 1 Value' %>
<% assign header.header2  = 3000 %>
<% assign header.header3  = 3000.55 %>

basicAuth - is a null object
<% en.http.post results1 url queryString formFields bodyString header basicAuth  %>
<% return 'results1' results1 %>
```


## Example 2: post with file

```
<% assign query.name = 'test1001' %>

<% en.data.findOne rowResults 'test1000' query %>

<% return 'rowResults' rowResults %>

<% assign row = rowResults.row %>
<% assign rowId = rowResults.row._id %>
<% assign fileId = rowResults.row.publicfile._id %>
<% en.data.getFile fileResults 'test1000' 'publicfile' rowId fileId %>
<% return 'fileResults' fileResults %>
<% return 'rowId' rowId %>
<% return 'fileId' fileId %>

<% assign attachment = fileResults.attachment %>
<% return 'attachment' attachment %>

All parameters are same as previous example, except this request also has a file submitted.
basicAuth - is a null object
<% en.http.post results2 url queryString formFields bodyString header basicAuth attachment   %>
<% return 'results2' results2 %>

<% en.http.post results3 url queryString formFields bodyString header basicAuth attachment.bin   %>
<% return 'results3' results3 %>


```



