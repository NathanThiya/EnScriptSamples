# Set a value for a seqence


en.data.setSequence results sequenceName


Name            | Description
----------------|-------------
results         | This APIs results will be returned here.
sequenceName    | Name of the sequence


<% en.data.setSequence resultsCustomerId 'customerId' 21000000 %>
<% return 'resultsCustomerId' resultsCustomerId %>

<% en.data.setSequenceValue resultsOrderId 'orderId' 11000000 %>
<% return 'resultsOrderId' resultsOrderId %>

