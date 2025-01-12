# Unpredictable Iteration Order in Recursive Function Using pairs

This repository demonstrates a potential issue with Lua's `pairs` iterator when used in recursive functions.  The `pairs` iterator does not guarantee a specific iteration order, which can lead to unexpected results if the order is assumed.  The bug example shows a recursive function that processes nested tables. The order in which the nested tables are processed is not consistent, potentially leading to errors or incorrect results.

## Bug
The `bug.lua` file contains a Lua function `foo` that recursively traverses a nested table. The iteration order using `pairs` is not deterministic, leading to unpredictable output. This can be particularly problematic if the order of processing is crucial for the logic of the recursive function.  This is a subtle but important error that can be difficult to debug.

## Solution
The `bugSolution.lua` file provides a solution that addresses the problem by using a different iteration method. By employing a different approach, the solution ensures predictable and consistent processing of nested tables.