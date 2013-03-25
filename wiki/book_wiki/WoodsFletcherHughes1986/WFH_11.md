__Common standard deviation__: s = √{[(n1-I)si2+(n2-I)s22]/(n1+n2-2)}

__t-value__: t=(x̄1-x̄2)/√(s2/n1+s2/n2)

This statistics has a t-distribution with n1+n2-2 df whenever the null hypothesis is true.

It will usually make good sense to estimate how large that difference seems to be. A 95% confidence interval for the difference µ1-µ2 is given by: x̄1-x̄2 ± constant\*√(s2/n1+s2/n2).

If a linguistic experiment is carried out in such a way that several tokens of a particular linguistic item occur close together the subject may, consciously or not, cause them to be more similar than they would normally be.

> Such a lack of independence in the data will distort the results of any analysis, including the test discussed in this chapter.

__F-distribution__ depends on the degrees of freedom of both the numerator and the denominator.

1. We have seen that it is necessary to assume that two populations have the same standard deviation or, equivalently, the same variance before a t-test for comparing their means will be appropriate.

2. It is possible to check the validity of this assumption by testing H0:σ12 = σ22 against H0:σ12 ≠ σ22 using the test statics: F= larger sample variance / smaller sample variance.

3. In every case the relevant degrees of freedom will be those used in the divisors of the sample standard deviations.

4. However, F-test also requires that the samples be from normally distributed populations and it is rather sensitive to failures in that assumption. If the null hypothesis is true and the population variance are equal the distribution of this test statistics is known.

The only real difference is that the F-test it is possible to consider a on-sided alternative such as H1:p1<p2 while the chi-squared test will always require a two-sided alternative.

It will usually be helpful to estimate how unlike two proportions may be whenever a test has found them to be significantly different.

> An approximate 95% confidence interval for the difference in two proportions is calculated by the formula: |p1-p2|±{1.96\*√[p1(I-p1)/n1+p2(I-p2)/n2]}

> This interval does not include the value zero, which we would expect since the hypothesis that p1=p2, or p1-p2 = o, was not rejected at the 5% level. This occurs because the confidence interval is not exact.

This __paired comparison__ or __correlated samples t-test__ will frequently be relevant and it is usually good experimental practice to design studies to exploit its extra sensitivity.

> However, it requires exactly the same assumption as the test which uses independent samples; the two populations being compared should be approximately normally distributed and have equal variance.

A 95% confidence interval for the difference between the two population means can be calculated as: |d|±(constant\*s/√n)

> where the constant is the 5% significance value of the t-distribution with (n-1) df.

We have seen that experimental situations do arise where the assumption that two populations have equal variances may be untenable, and that this will affect the validity of some of the tests introduced above.

__Nonparametric tests__: require no special distributional assumptions: 𝜒2 test for association in contingency tables and test for significant rank correlation belong to this kind.

__Two-sample Mann-Whitney rank test__: Z = [T-m/2(m+n+10)]/≈√[mn/12(m+n+1)], which can then be compared with critical values of the standard normal distribution. to see whether the null hypothesis of equal population means can be rejected.

We can test the null hypothesis H0: the judges are giving the same assessment scores, on average, versus the two-sided alternative H1: on average the assessment scores of the judges are different, although it is unlikely that the assessment scores are normally distributed and the size of the sample is not large enough for us to rely on the Central Limit Theorem.

For the one-sided alternative we first of all have to ask whether there are any indications that the alternative is true.

If T is greater than 2, the test can still be carried out by calculating S and T in the same way and then using the test statistic: Z = (T-2S-I)/√T, which should be referred to Table A3 (critical values of the standard normal distribution).

Type 1 error, the incorrect rejection of a valid null hypothesis; Type 2 error: the failure to reject the null when it is mistaken.

The __paired sample t-test__ results in the conclusion that there was a difference, significant at the 5% level, between the mean scores of the two groups.

1. It makes use of the fact that the populations of scores are normally distributed;

2. It uses not only the direction but also the size of the difference in paris.

3. It is more sensitive to differences in the population means and will readily give a significant value when such differences exist.

The __sign test__ could not detect a difference, not even at the 5% significance level, which is the weakest level of evidence which, by general convention, most experimenter would require in order to claim that 'the null hypothesis can be rejected'.

1. For any set of data the sign test will be more likely than the t-test to cause a type II error.

2. However, if the assumption about the parent population which underlies the t-test, i.e. that they are normally distributed, is not justified, the likelihood of a type I will be higher than the probability indicated by t-value.

__Assessing a statistical hypothesis is similar to many other kinds of judgment. The correctness of the conclusion will depend on two thins: the quantity of the information available and its quality__.

__A sensible procedure might be first to use the sign test__.

If a t-test is carried out, the researcher should be aware of the consequence of the possible failure to meet the assumptions of the test.
