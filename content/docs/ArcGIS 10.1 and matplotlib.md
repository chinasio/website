## ArcGIS 10.1 and matplotlib
Graphing at 10.1 is now easier because ArcGIS comes with matplotlib.  To me, this is an exciting enhancement that broadens what python developers can do when it comes to visualization of data in ArcGIS.

A simple example of this is the basic X/Y plot but instead of using random number, assume we have a table and the X/Y (distance/elevation) is in your table.

Example:
```python code
import arcpy
import os
import matplotlib.pyplot as plt
x = []
y = []
elevPNG = env.scratchFolder + os.sep + "elev.png"
fig = plt.figure()
table = r"C:\temp\scratch.gdb\data"
fields = ["FIRST_DIST", "FIRST_Z"]
with arcpy.da.SearchCursor(table, fields) as rows:
    for row in rows:
        x.append(row[0])
        y.append(row[1])
plt.plot(x,y, color='r')
plt.xlabel('Distance From Start Location')
plt.ylabel('Elevation')
plt.title('Landscape Profile')
fig.savefig(elevPNG, dpi=fig.dpi) 
```

So what has happened, is that the x and y information is stored in a 1:1 fashion in list objects.  The figure is created and lists populated using a simple search cursor.  The line graph is shown using the plot() and labels are added to make the graph easier to read.

The results is something like this:
