CHAPTER 2

The distinction between exploratory data analysis and confirmatory data analysis comes down to us from the famous John Tukey,1 who emphasized the importance of designing simple tools for practical data analysis.

In Tukey’s mind, the exploratory steps in data analysis involve using summary tables and basic visualizations to search for hidden patterns in your data.

But before you start searching through your first data set, we should warn you about a real danger that’s present whenever you explore data: you’re likely to find patterns that aren’t really there.

Think of confirmatory data analysis as a sort of mental hygiene routine that we use to clean off our beliefs about the world after we’ve gone slogging through the messy —and sometimes lawless— world of exploratory data visualization.

Confirmatory data analysis usually employs two tools: • Testing a formal model of the pattern that you think you’ve found on a new data set that you didn’t use to find the pattern. • Using probability theory to test whether the patterns you’ve found in your original data set could reasonably have been produced by chance.

Often the only way to separate causation from correlation is to know whether the data you’re working with was generated experimentally or was only observationally recorded because experimental data wasn’t available.

For our purposes, the subtler philosophical issues of data analysis are going to be treated as if they were perfectly separable from the sorts of prediction problems for which we’re going to use machine learning techniques.

In the interest of pragmatism, we’re therefore going to use the following definition throughout the rest of this book: a “data set” is

nothing more than a big table of numbers and strings in which every row describes a single observation of the real world and every column describes a single attribute that was measured for each of the observations represented by the rows.

Replacing many columns in your data set with a few columns or even just one is called dimensionality reduction, which we’ll describe in Chapter 8.

Before you do anything else with a new data set, you should try to find out what each column in your current table represents. Some people like to call this information a data dictionary, by which they mean that you might be handed a short verbal descrip- tion of every column in the data set.

Many variables that really work like labels or categories are encoded mathematically as 0 and 1.

Factors in R can be thought of as labels, but the labels are actually en- coded numerically in the background: when the programmer accesses the label, the numeric values are translated into the character labels specified in an indexed array of character strings.

In other words, the definition of range based on min and max effectively depends on only two of your data points, regardless of whether you have two data points or two million data points.

Visualizing your data is often a more effective way to discover patterns in it.

These idealized shapes, also called distributions, are standard patterns that statisticians have studied over the years.

Even when you think the shape you see is only a vague approximation to your data, the standard distributional shapes can provide you with building blocks that you can use to construct more complex shapes that match your data more closely.

This is something you should always keep in mind when working with histograms: the binwidths you use impose external structure on your data at the same time that they reveal internal struc- ture in your data.

This is called

oversmoothing. And the opposite problem, called undersmoothing, is just as danger- ous.

Because setting bindwidths can be tedious and because even the best histogram is too jagged for our taste, we prefer an alternative to histograms called kernel density esti- mates (KDE) or density plots.

Additionally, density plots have some theoretical superiority over histograms: in theory, using a den- sity plot should require fewer data points to reveal the underlying shape of your data than a histogram.

it’s a mixture model in which two standard distributions have been mixed to produce a nonstandard distribution.

When we talk about the number of modes that we see in our data, we’ll use the following terms: a distribution with one mode is unimodal, a distribution with two modes is bimodal, and a distribution with two or more modes is multimodal.

In contrast, the second graph, which is called the gamma distribution, is skewed to the right, which means you’re much more likely to see extreme values to the right of the mode than you are to see extreme values to the left of the mode.

The last qualitative distinction we’ll make is between data that’s thin-tailed and data that’s heavy-tailed.

A thin- tailed distribution usually produces values that are not far from the mean; let’s say that it does so 99% of the time.

After the normal distribution, there are two more canonical images we want to show you before we bring this section on density plots to a close: a mildly skewed distribution called the gamma and a very skewed distribution called the exponential.

One other thing to keep in mind is that the gamma distribution produces only positive values.

To do real machine learning, we need

to find relationships between multiple columns in our data and use those relationships to make sense of our data and to predict things about the future.

