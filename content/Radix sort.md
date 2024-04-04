---
aliases: "202404031822"
tags: 
date: 2024-04-03
created: 2024-04-03T18:22
updated: 2024-04-03T18:45
---
# [[Radix sort]]

Brief process:
1. Sorts by rightmost digit first
2. Then by middle digit
3. Lastly, by leftmost digit

Notes:
- Does not use comparison.
- Treats arrays like Strings with the same length.
	- Group integers according to their rightmost character (digit) into “buckets”
	- Repeat with next character (digit), etc.