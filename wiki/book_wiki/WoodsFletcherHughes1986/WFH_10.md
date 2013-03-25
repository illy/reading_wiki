There types of possibility of scattergram:

1. There is an exact linear relationship between X and Y, distorted only by measurement error or some other kind of random variation in the two variables.

2. There is a non-linear relationship between X and Y which, especially in the presence of random error, can be represented quite well by a linear model.

3. There is no degree of linear relation between X and Y and any apparent linearity in the way the points cluster due entirely to random error.

__Linear correction__:

> __Covariance__ designates COV(X, Y), and is defined by: COV(X, Y) = I/(n-I)∑(Xi- x̄)(Yi-x̄). It is a scale-dependent measure.

> However, the use of covariance as a descriptive variable indicating the degree of linearity in a scatter diagram is made difficult by two awkward properties it possesses.

To describe, in some sense, the quantity r, known as the __correlation coefficient__ (formally as the 'Pearson product-moment coefficient of linear correlation'), in which we use the product SYSY as a denominator: r(X,y) = COV(X, Y)/SxSy.

1. r does not have any units.

2. It has the same value for both scattergrams. Changing the scale in which one, or both, variable are measured does not alter the value of r. (__scale-independent__)

3. The value of the numerator, ignoring the sign, can never be greater than SXSY, and hence the value of r can never be greater than I.

A more convenient formula for the calculation of the numerator in the formula for r is presented and the calculations are demonstrated as: COV(X, Y) = ∑(Xi- x̄)(Yi - Y-bar)

1. Even if two variables are completely uncorrelated, the value of r calculated from any random sample of pairs of observations on the variables will not be exactly zero.

    Simply because of the randomness of the sampling process the value of r will be different from on sample to another. The value of r obtained by calculating from a sample or pairs 9X, Y) is then an estimate of 𝘱.

2. A population in which X and Y are mutually independent would have x̄ = o and this hypothesis is frequently tested.

    But probably no single sample of pairs (X, Y) will give a value of r which is exactly zero.

3. Provided that both the variables involved have a normal distribution, r can itself be used as the test statistic, though critical values will depend on the sample size.

A sample correlation coefficient is a point estimator of the population value, 𝘱, and may vary considerably from one sample to another.

A confidence interval would give much more information about the possible value of 𝘱.

There is no simple way to obtain a confidence interval for the true correlation 𝘱, in samples of less than 50 or so, even if both variables have a normal distribution.

> For larger samples and normally distributed variables a 95% confidence interval can be calculated as follow (Fisher's Z-transformation): (eX-I)/(eX+I)<𝘱<(eY-I)/(eY-I), where X=2(Z-1.96/√(n-3)), Y=2(Z+1.96/√(n-3)), and Z=I/2\*loge((I+r)/(I-r)).

Using Fisher's Z-transformation it is also possible to test whether two correlation coefficients, estimated from independent samples, have come from populations with equal population correlations.

For sample size greater than 50 the statistic has a distribution very close to that of the standard normal and the hypothesis H0 : 𝘱1 = 𝘱2 versus H1 : 𝘱1 ≠ 𝘱2 can be tested by comparing the value of the statistic to percentage points of the normal distribution.

1. It is perfectly possible that the correlation between X and Y is the same as the correlation between X and W.

2. The test is relevant only if the correlations r1 and r2 are based on independent samples. if X, Y and W were all measured on the same n subjects the test would not be valid.

The correlation coefficient is often used to describe the extent to which knowledge of the way in which the values of one variable vary over observed units can be used to assess how the values of the other will vary over the same units.

> This is frequently expressed by a phrase such as 'the observed variation in X (or Y) accounts for P% of the observed variation in Y (or X)'. The value of P is obtained by squaring the value of r.

As always, it is important to keep in mind that another random sample of values (Xi, Yi) from the same population will lead to a different value of r and r2.

> How good that estimate is will, as usual, depend on the sample size.

> An important point to realise here is that by a 'random sample' we mean a sample chosen randomly with respect to both variables.

It is worth noting that just a few unusual observation can affect greatly the value of r.

__Looking closely at the data before carrying out any analysis__.

A highish correlation apparently due to only two or three observations ought to be treated with great caution.

> Apart from any other reason, if both variables come from normally distributed populations it will be extremely rare for a random sample of moderate size to contain two or three unusually extreme data value - often called __outliers__.

If X and Y vary independently of one another, there ought to bt no relation between the rank of a particular Xi among the Xs and the rank of the associated Yi among the Ys. It ought therefore to be possible to derive a measure of the correlation between X and Y by considering the relationship between there rankings.

> One such measure is rs, the __Spearman rank correlation coefficient__. Suppose a random sample of n pairs has been observed and Ri and Si be the rank of the Xs and Yx as we have defined them above.

> Let D = ∑(Ri - Si)2. then rs is calculated by the formula: rs = I- 6D/(n3-nI)

Use the formula in the presence of ties, but to suspect that the apparent correlation may be very slightly exaggerated in the presence of a substantial proportion of tied rank.

1. rs will tend to underestimate the true correlation and will be more variable from one sample to another than the Pearson correlation coefficient.

2. rs was designed to cope with data sets which are not normally distributed or whose exact values are not known and should not be used on data which have a more or less normal distribution.

3. for certain kinds of data the population value, 𝘱s, of the Spearman coefficient is very different from that of 𝘱, the Pearson correlation coefficient, in the same population.

    Since rs is often calculated rather than r precisely in those situations where the underlying distribution of the data is unknown it is never safe to try to interpret rs as a measure of correlation.

In large samples and when the two variables are actually independent (so that 𝘱 = 𝘱s =o) the values or rs and r will be very similar.

There is no simple relationship, in general, between r and rs, nor between the population correlation coefficients 𝘱 and 𝘱s.

There is no simple way to interpret the 'strength' of correlation implicit in a sample value of rs.>>types of possibility of scattergram:
