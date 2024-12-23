# Incorrect usage of $inc operator in MongoDB aggregation pipeline
This example demonstrates a common error when using the `$inc` operator within the `$project` stage of a MongoDB aggregation pipeline.  The `$inc` operator is designed to increment existing numeric fields; it does not work as expected when trying to create a new field with an incremented value in the `$project` stage.

## Bug
The provided code attempts to increment the `count` field by 1 and store the result in a new field called `incrementedCount`. However, this will not increment. Instead, a new field with the original value is added. 

## Solution
The solution involves using the `$add` operator to add 1 to the `count` field, creating the new `incrementedCount` field with the correct incremented value.  See the solution file for the corrected code.
