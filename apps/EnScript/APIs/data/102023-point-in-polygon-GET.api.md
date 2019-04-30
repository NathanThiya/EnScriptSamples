# PointInPolygon to find a point with in a polygon on the dataset.

This API allows user to find datarows that contains a Polygon which has the specified lat, long.


<% assign query11.$and[0].timeStart.$gte = 10 %>
<% assign query11.$and[1].timeStart.$lte = 15 %>
<% assign query21.$and[0].timeStart.$gte = 10 %>
<% assign query21.$and[1].timeStart.$lte = 15 %>
<% assign query31.$and[0].timeStart.$gte = 10 %>
<% assign query31.$and[1].timeStart.$lte = 15 %>
query31:<<query31>>
<% assign query.$or = [query11,query21,query31] %>
query:<<query>>

<% assign queryParams.datasetId = 'fd-regions' %>    queryParams.datasetId  (mandatory)
<% assign queryParams.attribute = 'geometry' %>        queryParams.attribute  (Opt.) default: "geometry"
<% assign queryParams.lat = en.params.lat %>
<% assign queryParams.long = en.params.long %>
<% assign queryParams.fields = "name" %>     queryParams.fields - Comma separated fields (opt.) default: all
<% rem assign queryParams.filterQuery = NULL %>     queryParams.filterQuery - Query Object (opt.) default: none
<% assign queryParams.size = 10 %>     queryParams.size - Size per page (opt.) default: 10
<% assign queryParams.page = 1 %>     queryParams.page - current page (opt.) default: 1
<% en.data.pointInPolygon results queryParams %>
<% return 'queryParams' queryParams %>
<% return 'results' results %>


