---
icon: book-open
---

# Data Dictionary

Finally, we need to know what data our system is actually going to store. This could be in a Pandas dataframe, a dictionary, or just whatever format it comes in from your API. We need to know this before we start programming because we need a sense of what rules the data will need to follow.&#x20;

Otherwise, your shall we say... less than tech savvy users will cause error after error after error. Never underestimate an end user - they can and will break the rules!&#x20;

So, let's be specific with the data types and validation so we know how to stop this.&#x20;

## Example

Here's a **data dictionary** for storing rock data in the Rock Collection Program:

<table data-full-width="true"><thead><tr><th width="116">Variable</th><th>Data Type</th><th>Format for Display</th><th width="105">Size in Bytes</th><th>Size for Display</th><th>Description</th><th>Example</th><th>Validation</th></tr></thead><tbody><tr><td>name</td><td>String</td><td>Text</td><td>50</td><td>50</td><td>The name of the rock/mineral</td><td>"Granite"</td><td>Must be a non-empty string</td></tr><tr><td>hardness</td><td>Integer</td><td>Whole number</td><td>4</td><td>2</td><td>hardness scale value</td><td>6</td><td>1 ≤ hardness ≤ 10</td></tr><tr><td>composition</td><td>String</td><td>Text</td><td>100</td><td>100</td><td>Main mineral components</td><td>"Quartz, Feldspar"</td><td>Must be a valid string</td></tr><tr><td>colour</td><td>String</td><td>Text</td><td>20</td><td>20</td><td>Common rock colors</td><td>"Grey"</td><td>Must be a valid colour name</td></tr><tr><td>location_found</td><td>String</td><td>Text</td><td>20</td><td>100</td><td>Place where the rock was found</td><td>"Yosemite, USA"</td><td>Must be a valid location</td></tr></tbody></table>

## Need More Information?

{% content-ref url="../../../charts-and-algorithms/data-dictionaries/" %}
[data-dictionaries](../../../charts-and-algorithms/data-dictionaries/)
{% endcontent-ref %}



