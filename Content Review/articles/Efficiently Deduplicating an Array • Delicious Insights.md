Notes for Efficiently Deduplicating an Array • Delicious Insights

## Source:
Author: delicious-insights.com
Category: articles
Updated: 04/09/2021 04:13 PM
Highlights URL: https://readwise.io/bookreview/8584405
SourceUrl: https://delicious-insights.com/en/posts/js-array-deduplication/


#### Extras:
Notes on using Set - **working with Sets in Javascript**


 
-----
 ## Highlights:

### Sure, if we have advanced needs (custom comparator, computed...
>Sure, if we have advanced needs (custom comparator, computed keys, etc.) we’ll need Lodash or some other help. But for the common case: deduplicating raw values, the trick, since ES2015, is to use a Set ^rw165893394hl


Highlighted: 04/09/2021 03:46 PM
Updated: 04/09/2021 03:46 PM


#### Extras:



------

### Set compares values using the SameValueZero pseudo-algorithm...
>Set compares values using the SameValueZero pseudo-algorithm laid out in the JavaScript specification ^rw165893546hl


Highlighted: 04/09/2021 03:47 PM
Updated: 04/09/2021 03:47 PM


#### Extras:



------

### We consume the entire iterable, which means an O(n) run, for...
>We consume the entire iterable, which means an O(n) run, for a total cost around O(2n log(n)), which is very, very much better than O(n²). Here’s a small comparative table, assuming 10ns for the SameValueZero comparison, which is quite reasonable ^rw165899264hl

Comment: if you want to dedupe an array of a million items before Set, you are looking at a 3 hour job vs 120ms converting to a Set and back. ^rw165899264comment

Highlighted: 04/09/2021 04:13 PM
Updated: 04/09/2021 04:13 PM


#### Extras:



------

