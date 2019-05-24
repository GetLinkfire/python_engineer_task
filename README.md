# python_engineer_task

Welcome! We have prepared a little implementing exercise for you.

The task is to build a miniature data pipeline: In lack of a streaming source,
pull a sample data set per http,
do some basice validation and transformation on the data, and write to disk.


In more detail, the program should do the following, not necessarily in that order:

 - Download our zipped line-json file with sample data from [here](https://tba)
 - Process one line at a time
 - Split records by values in the `type` field and create one output file for each `type`
 - Whenever there is a `convValue`, convert to USD in `convUsdValue` using [rates.json](https://tba) and `convValueUnit`
 - Validate that the `linkid` is a valid UUID using standard library
 - Append non-valid records to a separate output file
 - Output line json files again




link to files in the repo:
https://raw.githubusercontent.com/python/black/master/CONTRIBUTING.md

