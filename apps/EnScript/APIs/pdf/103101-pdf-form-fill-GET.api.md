# Get form fields from a PDF form

en.pdf.fillForm results pdfForm fields

Use PDFScape or Acrobat PDF DC to create PDF form.
https://www.pdfescape.com/

```
<% assign query.name = 'form-810' %>
<% en.data.findOne results 'test' query %>
<<results>><br/>
<br/><br/><br/>
<% assign row = results.row %>
<% assign rowId = results.row._id %>
<% assign fileId = results.row.pdfform._id %>
<% en.data.getFile results 'test' 'pdfform' rowId fileId %>
<<results>><br/>
<br/><br/><br/>
results.attachment.bin:<<results.attachment.bin>><br/><br/>

<% assign pdfForm = results.attachment.bin %>
pdfForm:<<pdfForm>><br/><br/>
<% en.pdf.getFormFields results pdfForm %>

getFormFields:<<results>><br/><br/><br/>

<% rem assign field1.name = 'buyers' %>
<% assign field1.name = 'brokerage' %>
<% assign field1.type = 'text' %>
<% assign field1.value = row.buyers %>

<% assign fileId = row.buyerSignature._id %>
<% en.data.getFile results 'test' 'buyerSignature' rowId fileId %>
<% assign buyerSignature1 = results.attachment.bin %>
buyerSignature1:<<results.attachment>><br/><br/><br/>

<% rem assign field2.name = 'buyerSignature1' %>
<% assign field2.name = 'buyerAckSignature1' %>
<% assign field2.type = 'image' %>
<% assign field2.image = buyerSignature1 %>

<% assign fields = [field1, field2] %>

<% en.pdf.fillForm results pdfForm fields %>

fillForm:<<results>><br/><br/><br/>
<% if results.bin %>
    Yes form filled successfully<br/><br/>
<% else %>
    No form not filled successfully<br/><br/>
<% endif %>

<% assign singnedFile.name = 'signed-file.pdf' %>
<% assign singnedFile.contentType = 'application/pdf' %>
<% assign singnedFile.bin = results.bin %>
<% assign isPrivate = false %>

<% en.data.attachFile results 'test' 'signedForm' rowId isPrivate singnedFile %>

results: <<results>><br/><br/>
```
