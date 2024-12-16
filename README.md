# CSS Calc() and Border Width Issue

This repository demonstrates a subtle issue involving the CSS `calc()` function and border widths. The example shows how the order of operations in CSS can lead to unexpected results when combining `calc()` with `border` properties.

## Problem

The `bug.css` file contains a CSS rule that attempts to set the width of a `div` element to 100% of its container, minus a 20px border.  However, because the border's width is added *after* the `calc()` function computes the width, the final rendered width is incorrect.

## Solution

The `bugSolution.css` file provides a corrected version. To fix it, either include the border width in the `calc()` calculation, or use the `box-sizing` property to include the padding and border in the element's total width.