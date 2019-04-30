# Nearby Count search

In order for nearby search to work, the following conditions must be met:
- Dataset must have a geometry field
- Geometry field must be geo indexed



queryParams.datasetId  (mandatory)
queryParams.lat - center point latitude (mandatory)
queryParams.long - center point longitude (mandatory)
queryParams.filterQuery - Query Object (opt.) default: none
queryParams.minDistance - Min Distance (opt.)
queryParams.maxDistance - Max Distance (opt.)
queryParams.limit - Size per page (opt.) default: 100
queryParams.page - current page (opt.) default: 1
queryParams.distanceField - calculated distance from center point (opt.) default: "distance"
<% rem en.query.nearby results queryParams %>

<% assign queryParams.datasetId = "fd-drivers" %>
<% assign queryParams.lat = en.params.lat %>
<% assign queryParams.long = en.params.long %>
<% rem assign queryParams.filterQuery.category = "Automotive"  %>
<% rem assign queryParams.minDistance  %>
<% assign queryParams.maxDistance = 100000 %>
<% assign queryParams.limit = 50 %>
<% rem assign queryParams.size  %>
<% rem assign queryParams.page  %>
<% rem assign queryParams.distanceField  %>

<% en.data.nearby results queryParams %>
<% return 'results1' results %>

<% assign queryParams.limit = 50000 %>
<% en.data.nearbycount results2 queryParams %>
<% return 'results1' results2 %>
