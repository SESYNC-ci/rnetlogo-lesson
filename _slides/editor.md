---
---

## The Editor

The **console** is for evaluating commands you don't intend to keep or reuse. It's useful for testing commands and poking around.

The **editor** is where you compose scripts that will process data, perform analyses, code up visualizations, and even write reports.

These work together in RStudio, which has multiple ways to send parts of the script you are editing to the console for immediate evaluation. Alternatively you can "source" the entire script.

<!--split-->

Open up "lesson-1.R" in the editor, and follow along by replacing the `...` placeholders with the code here. Then evalute just this line (Ctrl R on Windows, ⌘ R on Mac OS).


~~~r
vals <- seq(1, 100)
~~~
{:.text-document title="lesson-1.R"}

<!--split-->

The elements of this statement, from right to left are:

- `)` is the closing paren of a function call
- `1` and `100` are both arguments, or parameters, to the function
- `(` is the opening paren of the function call
- `seq` is the name of the function
- ` <- ` is an operator that assigns what's named on the left to equal the result of the expression on the right
- `vals` is the name of a variable

<!--split-->

Question
: Why call `vals` a "variable" and `seq` a "function"?

Answer
: {:.fragment} It is true they are both names of objects known to R, and could be called variables. But `seq` has the important distinguishing feature of being **callable**, which is indicated in documentation by writing the function name with empty parens, as in `seq()`.

<!--split-->

Our call to the function `seq` could have been much more explicit. We could give the arguments by the names that `seq` is expecting.


~~~r
vals <- seq(from = 1,
            to = 100)
~~~
{:.text-document title="lesson-1.R"}

Run this code either line-by-line, or highlight the section to run (optionally with keyboard shortcut Ctrl-Return or ⌘ Return).

<!--split-->

Question
: What's an advantage of naming arguments?

Answer
: {:.fragment} One advantage is that you can put them in any order. A related advantage is that you can then skip some arguments, which is fine to do if each skipped argument has a default value.

<!--split-->

How would you get to know the names of a function's arguments?


~~~r
?seq
~~~
{:.input}

How would you even know what function to call?


~~~r
??sequence
~~~
{:.input}

<!--split-->

Going the other direction, a shorthand form of the `seq()` function is:


~~~r
1:100
~~~
{:.input}

~~~
  [1]   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15  16  17
 [18]  18  19  20  21  22  23  24  25  26  27  28  29  30  31  32  33  34
 [35]  35  36  37  38  39  40  41  42  43  44  45  46  47  48  49  50  51
 [52]  52  53  54  55  56  57  58  59  60  61  62  63  64  65  66  67  68
 [69]  69  70  71  72  73  74  75  76  77  78  79  80  81  82  83  84  85
 [86]  86  87  88  89  90  91  92  93  94  95  96  97  98  99 100
~~~
{:.output}

This shorthand is most commonly used while accessing parts of objects, as we'll see below.

<!--split-->

## Save your work

Do save the "lesson-1.R" file.

But I mean *really* save your work, by commiting it to your project and syncing up to a GitHub repository.

1. Go to the `git` tab in RStudio
1. Select `commit` to open the "Review Changes" window
1. Select the file(s) you want to commit.
1. Enter a descriptive message about the commit.
1. Commit!
1. Push!

<!--split-->