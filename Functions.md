# MP3Tag Built IN Functions

This is a self discovery document as I am reverse engineering what already exists rater than look at the MP3Tag documents - **use at your on risk**. Feel free to comment where problems are noted.

## Built In Function
| Function|Description |  
| --- | --- |
| $add()| |  
| $eql()|??? |  
| $if((F),(I),' ')| |  
| $left(\<String>,\<CharCount>)|Cut the left CharCount characters from the string |  
| $mid(\<String>,\<StartPosition>, \<CharCount>)|Midstring |  
| $num(\<FieldName>,\<MinimumDigits>)| Causes the number values to be the minimum number of  digits by adding leading zeros for a uniform file name or field look. |  
| $strchr()| |  
| $strstr(\<String>,\<TestValue>)|??? |  
| \$sub($)| |  
| &|Concatenate |  

## Prepared Functions

| Action | Function |  
| --- | --- |  
| Remove trailing spaces in File Name | $trim(%_filename%) |  

