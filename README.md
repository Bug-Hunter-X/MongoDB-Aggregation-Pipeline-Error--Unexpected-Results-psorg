# MongoDB Aggregation Pipeline Error: Unexpected Results

This repository demonstrates a common error in MongoDB aggregation pipelines that leads to unexpected results. The issue occurs when attempting to group and sort documents based on a field that may not exist in all documents. 

## Bug Description
The provided aggregation pipeline attempts to group documents based on a field and then sort and limit the results. However, if some documents lack the field, the pipeline produces unexpected counts and sorting behavior. 

## Solution
The solution involves adding a `$project` stage to explicitly define the field and handle cases where the field is missing. By adding a conditional expression, we ensure the field's value exists before attempting to group or sort.