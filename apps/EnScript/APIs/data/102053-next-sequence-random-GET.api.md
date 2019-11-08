# Get next random value for a seqence


en.data.nextSequenceRandom results sequenceName randomRange


Name            | Description
----------------|-------------
results         | This APIs results will be returned here.
sequenceName    | Name of the sequence
random range    | Random Range (optional) ex: 20, default: 10


<% en.data.nextSequenceRandom resultsCustomerId 'customerId' %>
<% return 'resultsCustomerId' resultsCustomerId %>

<% en.data.nextSequenceRandom resultsOrderId 'orderId' %>
<% return 'resultsOrderId' resultsOrderId %>

