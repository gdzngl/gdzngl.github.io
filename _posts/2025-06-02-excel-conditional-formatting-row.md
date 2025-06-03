---
layout: post
title:  "Conditional Formatting Entire Row"
description: "How to apply conditional formatting to an entire row in Excel"
tags: excel howto
---

# Formula Only

Assuming you want to highlight rows where column A is "Gretchen" enter this formula `=$A2="Gretchen"`

The formula breaks down like this:

`=` because it's a formula  
`$A` forces the formula to always look at column A, not the current column  
`2` the first row, this will evaluate to the current row because we do not have the `$`  
`="Gretchen"` the string we want to match in column A.  To match a number you could also have `=1` or `>2`


# Step By Step Demo

To demo this, I created a table with a name column and a random column.  We can sort the table by the random column to force the lines to move and prove the conditional formatting is working. Here's a table you can copy and paste into Excel if you want to try.

| Name | Random |
| Alpha | =RAND() |
| Alpha | =RAND() |
| Gretchen | =RAND() |
| Gretchen | =RAND() |
| Romeo | =RAND() |
| Romeo | =RAND() |
| Sierra | =RAND() |
| Sierra | =RAND() |
| Tango | =RAND() |
| Tango | =RAND() |

To set up the conditional formatting, select the table without the headers.

![select cells](/assets/2025-06/select-cells.png)

Open Conditional Formatting and pick New Rule.  Select "Use formula to determine which cells to format"

In the formula box enter `=$A2="Gretchen"`

![enter formula](/assets/2025-06/conditional-formula.png)

Make sure you update the format or you will think it didn't work when there is no format applied.

Sort by Random to see the conditional formatting work!

![formatted rows](/assets/2025-06/formatted-rows.png)

# Possible issues

## Missing the absolute reference to the column

If your entire row does not highlight, you may have missed the `$` in the column part of the cell reference.  

![missing absolute column](/assets/2025-06/missing-absolute-column.png)

## Wrong top row number

If the highlighting is always one row off, you might have the wrong row number for your top row.

![wrong row number](/assets/2025-06/wrong-row-number.png)

In this example, the conditional formatting range is `=$A$1:$B$11` but the formula has `$A2` as the first row.  This is a common mistake when a table has headers.