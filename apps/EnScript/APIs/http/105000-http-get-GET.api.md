# HTTP GET

<% assign url = 'https://postman-echo.com/get?foo1=bar1&foo2=bar2' %>

<% en.http.get results url %>
results: <<results>>
<% return 'getResults' results %>

<% json response %>
<<results.response>>
<% endjson %>

<% return 'response' response %>

