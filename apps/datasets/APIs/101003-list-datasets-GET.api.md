# List datasets

List datasets allows querying and list pagination


# Search for text within name or description
<% assign searchText = 'test 10' %>

<% assign nameQuery.name.$regex = searchText %>
<% assign nameQuery.name.$options = '$i' %>
<% assign descQuery.description.$regex = searchText %>
<% assign descQuery.description.$options = '$i' %>
<% assign query.$or = [nameQuery, descQuery] %>

<% return 'query' query %>
<% en.data.sets.list results size page query %>

size    - Page size default:500
page    - Requested page number
query   - Query Object (Mongo Query)

<% return 'list-results' results %>        
