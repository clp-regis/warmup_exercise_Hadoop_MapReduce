# warmup_exercise_Hadoop_MapReduce
A simple example of Hadoop MapReduce in Python.

Adapted from [here](http://rare-chiller-615.appspot.com/mr1.html).


If you want to test that the mapper is working, you can do something like this:

`python mapper.py < nchs_causes_of_deaths.csv | tail`

This takes the file shakespeare.txt as input for mapper.py and shows the last few lines of output.

Similarly, you can see if the reducer is working like so:

`python mapper.py < nchs_causes_of_deaths.csv > map_output.txt`
`python reducer.py < map_output.txt`

This creates the file `map_output.txt` by processing shakespeare.txt with mapper.py, and then uses reducer.py to process the map_output.txt file. 

The dataset provided, nchs_causes_of_deaths.csv, was adapted from this [dataset](https://data.cdc.gov/NCHS/NCHS-Leading-Causes-of-Death-United-States/bi63-dtpu/data). 

Testing the files in this way is much easier than trying to debug the errors from Hadoop streaming.  The errors from using Python above will be Python errors and easier to read than the complex Hadoop Java errors.
