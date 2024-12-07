# CSS Calc() Issue in Media Queries

This repository demonstrates a problem with using CSS `calc()` within media queries when the calculation could result in a negative value.  The `bug.css` file contains the problematic code, and `bugSolution.css` offers a solution.

The problem arises because  `calc(100vw - 100px)` can produce a negative value if the viewport width is less than 100px.  This unexpected result may lead to unexpected layout shifts or media query misbehavior.

The solution involves adding a `max()` function to ensure the calculation never results in a negative value.