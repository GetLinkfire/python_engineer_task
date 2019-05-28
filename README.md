# Python Engineer Exercise

Welcome! We have prepared a little exercise for you.

The task is to build a miniature data pipeline: In lack of a streaming source,
pull the [sample data set](https://raw.githubusercontent.com/GetLinkfire/python_engineer_task/master/data.json.gz) via https,
do some simplified validation, transformation, and splitting of the data, and write the output to disk.


In more detail, the program should do the following, not necessarily in that order:

 - Fetch our zipped line-json file with sample data from [here](https://raw.githubusercontent.com/GetLinkfire/python_engineer_task/master/data.json.gz).
 - Output (not gzipped) line-json files again.
 - Process one line at a time, pretending that you're processing a stream.
 - Whenever there is a `convvalue`, use the [rates.json](https://raw.githubusercontent.com/GetLinkfire/python_engineer_task/master/rates.json) and `convvalueunit` to convert the value to USD. Write that value to a new field `convusdvalue`.
 - Split records by values in the `type` field and create one output file for each `type`.
 - Validate that the `linkid` is a valid UUID, using the standard library. Invalid records must go to their own output file, e.g. "deadletters.json.gz".
