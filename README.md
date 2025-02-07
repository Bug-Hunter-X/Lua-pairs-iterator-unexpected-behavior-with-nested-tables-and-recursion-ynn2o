# Lua pairs iterator unexpected behavior with nested tables and recursion

This repository demonstrates a potential issue with Lua's `pairs` iterator when used with nested tables and recursive functions. The bug arises when a nested table is modified during iteration, potentially leading to unexpected behavior or skipped elements.

## Bug Description
The `pairs` iterator iterates over a table's key-value pairs.  However, if the table is modified during iteration (e.g., by adding or removing elements), the iterator's behavior becomes undefined. This is particularly problematic when working with deeply nested tables and recursive functions.

## Bug Reproduction
The `bug.lua` file contains a simple example that reproduces the issue.  Running this code might not always produce the same output, highlighting the non-deterministic nature of the problem.

## Solution
The `bugSolution.lua` file demonstrates a potential solution to the problem, providing a more robust way to iterate over and process nested tables.