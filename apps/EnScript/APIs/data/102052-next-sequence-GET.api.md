# Get next value for a seqence


en.data.nextSequence results sequenceName incrementBy


Name            | Description
----------------|-------------
results         | This APIs results will be returned here.
sequenceName    | Name of the sequence
incrementBy     | increment by (optional) default:1 eg: 5


<% en.data.nextSequence resultsCustomerId 'customerId' %>
<% return 'resultsCustomerId' resultsCustomerId %>

<% en.data.nextSequence resultsOrderId 'orderId' %>
<% return 'resultsOrderId' resultsOrderId %>

