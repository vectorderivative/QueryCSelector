QueryCSelector
==============

Simple implementation for a querySelector function for XML documents.

```C#
QuerySelector QS = New QuerySelector();
  QS.CreateFromFile("GetMemberResponse.xml");
  //Use Xpath expressions
  QS.Select("vouchersList/voucher/productId").GetElement(2).Text("test");
  Console.WriteLine(QS.Render());
```
#### Methods
`Create` loads the XML string, XElement or XElements object
`Select` executes an XPath expression to query the document.
`GetElement(i)` gets the QuerySelector object for the i node from a collection of nodes result of a previous selection
`Length` gets the number of nodes resulting from a selection
`Text` same as JQuery function
`Attr` gets or sets attributes.

#### Additional info
This is just an alpha proof of concept to get simple things done quick (get node values and attributes)
