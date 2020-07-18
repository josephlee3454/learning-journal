# Relating vars w/ scatter plots
* The scatter plot is a mainstay of statistical visualization. It depicts the joint distribution of two variables using a cloud of points, where each point represents an observation in the dataset. This depiction allows the eye to infer a substantial amount of information about whether there is any meaningful relationship between them.

# Aggregation and representing uncertainty
*  The default behavior in seaborn is to aggregate the multiple measurements at each x value by plotting the mean and the 95% confidence interval around the mean:

### fmri = sns.load_dataset("fmri")
### sns.relplot(x="timepoint", y="signal", kind="line", data=fmri);

# Plotting subsets of data with semantic mappings 
* The lineplot() function has the same flexibility as scatterplot(): it can show up to three additional variables by modifying the hue, size, and style of the plot elements. It does so using the same API as scatterplot(), meaning that we don’t need to stop and think about the parameters that control the look of lines vs. points in matplotlib.
### sns.relplot(x="timepoint", y="signal", hue="event", kind="line", data=fmri);