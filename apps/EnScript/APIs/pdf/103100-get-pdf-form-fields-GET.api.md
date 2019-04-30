# Get form fields from a PDF form

en.pdf.getFields results PDFBinary



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
```
