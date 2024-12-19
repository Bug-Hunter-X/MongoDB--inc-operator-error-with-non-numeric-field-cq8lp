# MongoDB $inc Operator Error
This example demonstrates an error that can occur when using the `$inc` operator in MongoDB update operations. The `$inc` operator is used to increment or decrement a numeric field.  Attempting to use it with a non-numeric field will result in an error.

## Bug
The bug lies in the incorrect usage of the `$inc` operator. The provided code tries to increment a field ('field') with a string value ('abc'), which is not a number, causing the operation to fail.

## Solution
The solution ensures that the field being incremented is of numeric type. If the field is not yet initialized, it's first set to 0 before incrementing.