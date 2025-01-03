# Unexpected Null Handling in Addition Function

This repository demonstrates a potential bug in a JavaScript function that handles null values. The `foo` function adds two numbers, but its null check might produce unexpected results for falsy values other than null. 

## Bug Description
The function uses strict equality (`===`) to check for null values before performing addition. While this works correctly for explicitly null values, it fails to handle other falsy values (0, false, "", etc.) that might be considered 'null-like' in some contexts. This could lead to unexpected behavior and incorrect results depending on the inputs.

## Solution
The improved version uses a more robust check that handles falsy values as well as strict null checks.