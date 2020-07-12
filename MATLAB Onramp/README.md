# MATLAB Onramp Projects

[MATLAB Onramp](https://matlabacademy.mathworks.com/) is a 1-2hr interactive introduction to MATLAB programming.

I am currently on week 2 of the [Machine Learning course](https://www.coursera.org/learn/machine-learning/home/welcome) by Stanford university on coursera. This section is titled "More Octave/MATLAB resources" and MATLAB OnRamp was recommended for a quick refresh.

I have previously used MATLAB for a linear algebra course at UCSD ([MATH 18 MATLAB](https://www.math.ucsd.edu/~math18/)), so I decided to just refresh my memory by completing this learning module.

Project topics:
- Electricity Usage
- Audio Frequency
- Stellar Motion

## Project 1 - Electricity usage
DESCRIPTION

Load the MAT-file into MATLAB and use **usage** display the matrix
```bash
load electricity.mat 
usage
```

The first column is the data for electricity usage in residential areas. Store that info in a variable called *res*. The second column is commercial, while the third is industrial; store those volumns as vectors in the variables *comm* and *ind* respectively.
```bash
res = usage(:,1)
comm = usage(:,2)
ind = usage(:,3)
```

The data  was colected annually from 1991 to 2013. Create a vector named *yrs* that represents the years.
```
yrs = (1991:2013)'
```

Create a plot with all three columns, using these descriptions:
- *yrs* : the x-data
- *res*: blue(b) dashed line(--)
- *comm*: black(k) dotted line(:)
- *ind*: magenta(m) dash-dot line(-.)
- title: July Electricity Usage
- Legend: res, comm, ind
```
plot(yrs,res,"b--")
hold on
plot(yrs,comm,"k:")
plot(yrs,ind,"m-.")
hold off
title("July Electricity Usage")
legend("res","comm","ind")
```
[Plot](electricityusage.JPG)

## Project 2 - Audio Frequency

## Project 3 - Stellar Motion
