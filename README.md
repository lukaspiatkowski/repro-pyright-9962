Steps to repro reanalizing kicking in after saving a file:
1. clone repo
2. `cd` inside
3. `code .`
4. Make sure that `"python.analysis.diagnosticMode": "workspace"` is set (although reanalizing happens also with "openFilesOnly", but it will be easier to notice with "workspace")
5. Open file `src/example/a.py`
6. Add a comment to the file, but don't save it yet
7. Open Python Language Server logs, wait for them to finish being ouputed
8. Save the file

Expected behaviour:
at most file a.py is analyzed

Actual behaviour:
a.py, b.py and c.py are analyzed
