# Test datasets

One row per way the analysis could be wrong, and the small dataset that would reveal it. The
first row is an example.

| Potential analysis error | Description of artificial dataset |
| --- | --- |
| Task 1's "at least 50 ratings" filter could be implemented incorrectly as *more than 50*, rather than *50 or more*. So a movie with exactly 50 ratings is dropped instead of kept. | Three movies. Every rating in the file is 5.0, so all three have identical averages and the filter is the only thing that can change the answer. One movie has 49 ratings, one has exactly 50, one has 51. The correct result lists the 50 and the 51, but omits the 49. |
| | |
| | |
| | |

When you asked the agent to create the artificial datasets and run tests, did it find any errors in the analysis you had previously run? How quickly was it able to correct them?
