At the highest level of abstraction, we can think of machine learning as a set of tools and methods that attempt to infer patterns and extract insight from a record of the observable world.

Statistics has almost always been concerned with learning something interpretable from data, whereas machine learning has been concerned with turning data into something prac- tical and usable

Machine learning is concerned with teaching computers something about the world, so that they can use that knowledge to perform other tasks.

n contrast, statistics is more concerned with developing tools for teaching humans something about the world, so that they can think more clearly about the world in order to make better decisions.

Two particularly important types of patterns constitute the core problems we’ll provide you with tools to solve: the problem of classification and the problem of regression, which will be introduced over the course of this book.

R is an extremely powerful language for manipulating and analyzing data. Its meteoric rise in popularity within the data science and machine learning communities has made it the de facto lingua franca for analytics.

R’s success in the data analysis community stems from two factors described in the preceding epitaphs: R provides most of the technical power that statisticians require built into the default language, and R has been supported by a community of statisticians who are also open source devotees.

In addition, as in other scientific computing environments, the fundamental data type in R is a vector.

Vectors can be aggregated and organized in various ways, but at the core, all data is represented this way.

Fundamentally, a data frame is simply a column-wise aggregation of vectors that R affords specific functionality to, which makes it ideal for working with any manner of data.

Because R exploits defaults very heavily, we have to be particularly conscientious of the default parameter settings for the functions we use in our scripts.

As such, we have to set stringsAsFactors=FALSE to prevent this. In fact, it is always a good prac- tice to switch off this default, especially when working with unfamiliar data.

To do this, we explicitly define the empty string as the na.string

From the data documentation, we construct a character vector that corresponds to the appropriate column names and pass it to the names functions with the data frame as its only argument

The strsplit function will throw an error if the split character is not matched; therefore, we have to catch this error. In our case, when there is no comma to split, we will return a vector of NA to indicate that this entry is not valid.

With the function defined, we will use the lapply function, short for “list-apply,” to iterate this function over all strings in the Location column.

The plyr family of functions work a bit like the map-reduce-style data aggregation tools that have risen in popularity over the past several years. They attempt to group data in some specific way that was meaningful to all observations, and then do some calcula- tion on each of these groups and return the results.

