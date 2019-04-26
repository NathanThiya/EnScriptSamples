# Create a field on the dataset

When field dataType and uiType specified, it has to be valid item from the list below.
For each dataType only certain uiType is valid. EnMobi does not enforce this at this time.


```
<% assign datasetId = 'test1000' %>                      // Mandatory
```

## New Field Information

```
<% assign field.id          = 'firstName' %>                // Mandatory
<% assign field.name        = 'First Name' %>               // Mandatory
<% assign field.dataType    = 'STRING' %>                   // Optional, default:STRING
<% assign field.uiType      = 'TEXTBOX' %>                  // Optional, default:TEXTBOX
```

## Create field on specified dataset

```
<% en.data.sets.createField results datasetId field %>
<% return 'test1000-createField' results %>
```
## Valid Data Types and UI Types

Data Type | UI Type
----------|---------
INTEGER     | INTEGER
DOUBLE      | DOUBLE
TEXT        | TEXTBOX, TEXTAREA, RICHTEXT, MARKDOWN, CODE-EDITOR, LIST, LIST-WITH-COLORS, LOOKUP
STRING      | TEXTBOX, TEXTAREA, RICHTEXT, MARKDOWN, CODE-EDITOR, LIST, LIST-WITH-COLORS, LOOKUP
DATE        | DATE
DATETIME    | DATETIME
TIME        | TIME
CURRENCY    | CURRENCY
URI         | URI
URL         | URL
PERCENT     | PERCENT
EMAIL       | EMAIL
FILE        | FILEUPLOAD
IMAGE       | IMAGEUPLOAD
BOOLEAN     | CHECKBOX
GEOMETRY    | GEOMETRY
PHONE       | PHONE
ADDRESS     | ADDRESS
AUTONUMBER  | LABEL
JSON        | TEXTAREA, CODE-EDITOR



RELATED - Future Data Type to establish relationship between 2 datasets.

