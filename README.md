# databrowseS
MATLAB scripts to visualize and explore matrices of data

# Using Databrowse function
In the UndergradRemoteProjects folder on the shared drive, we have provided a MATLAB function file that allows exploration of data with the ability to group by user-defined arrays.

* Add the 'matlab' folder to the MATLAB path (see "set path" icon on home screen of matlab).

Here's an example of how this function works.  Run the following code in MATLABto create an example data file:

```matlab
x = linspace(0,1,100);
y = x.^2;
mat = [y;y.*0.97;y.*1.005;y.*1.07;y.*0.94;y.*0.67;y.*0.65;...
  y.*0.77;y.*0.31;y.*0.3275;y.*0.41;y.*0.397885].*rand(12,100);
plot(mat')
```

When you run this code, you will notice that the output is a jumbled mess of lines, each with their own color.  Databrowse allows you to plot this data as a heatmap, see averages across groups, and plot with SD/SEM among other tasks.

Try and run the following line of code to see what happens:

```matlab
help databrowseS;
databrowseS(mat');
```

You will notice a figure window appears that you can interact with, showing the data and other useful options to plot/examine.

Now try running the following code lines to see how the behavior of the program changes.

```matlab
groups = [1,1,1,1,1,2,2,2,3,3,3,3];
databrowseS(mat',[],groups);
```

You should be seeing that the groups have ben applied and now three mean plots appear on the bottom.  You can still show individual data traces, plot mean/SD/SEM and short the above heatmap by the groupings you defined.
