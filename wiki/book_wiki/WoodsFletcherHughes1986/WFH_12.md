If all six different pairs are tested at the 5% significance level there will be a much bigger than 5% chance that at least one of the tests will be found to be significant even when no population differences exists.

The greater the number of samples observed, the more likely it will be that the difference between the largest sample mean and the smallest sample mean will be sufficiently great - even when all the samples are chosen from the same population - to give a significant value when a test designed for just two samples is used.

Assuming that each sample comes from a population with variance of σ2, the four different sample variances are four independent estimates of the common population variance.

> These can be combined, or pooled, into a single estimate by multiplying each estimate by its degrees of freedom ( the sample size minus one) summing the four products and dividing the total by the sum of the degrees of freedom of the four sample variances, thus:

> __pooled variance estimate__ = [(n1-I)S12+(n2-I)S22+(n3-I)S32+(n4-I)S42] / (n1+n2+n3+n4-4)

> This estimate of the population variance is often called the __within-samples estimate of variance__ since it is obtained by first calculating the variances within each sample and then combining them.

__between-groups estimate of variance__, Sb2, since it measures the variation across the four sample means.

1. If the null hypothesis is true, both of these estimates of the same quantity, σ2, and it can be shown that the ratio of the estimates: F=Sb2 / Sw2 has an F-distribution with 3 (number of the sample variance of observations) and 36 (pooled estimate variance) df.

2. If the null hypothesis is not true, Sb2 will tend to be larger than Sw2 because the variability in the four sample means will be inflated by the differences between the population means.

    Large values of the F statistics therefore throw doubt on the validity of the .null hypothesis.

__One-way analysis of variance__ compares the means of groups which are classified according to a single criterion variable.

1. Suppose that samples of size n have been taken from each of m populations. We will write Yij for the j-th observation in the i-th group.

2. As is common when analysis of variance is presented, we write Yii. to mean the total of the observations of group i. That is Yi. = n∑j=IYij

3. A term, usually called the __correction factor__ or CF, is now calculated: CF=Y..2/mn (It is often necessary, when calculating for an ANOVA, to keep a large number of figures in the intermediate calculations.)

4. __Total sum of squares__, TSS, which is the sum of the between-groups sum of squares and the within-groups sum of squares. (The latter is often called the __residual sum of squares__, RSS): TSS=∑Yij2-CF

5. The within-groups sum of squares is the quantity left when the between groups sum of squares is subtracted from the total sum of squares - hence the term 'residual sum of squares'.

6. Generally the between-groups degrees of freedom will be m-1, one less than the number of groups, the total available degrees of freedom will be mn-I, one less than the total number of observations, and the residual degrees of freedom are obtained by subtraction.

See interpretation of ANOVA analysis in p. 199.

Note that the F-ratio for comparing errors is significant beyond the I% level, but to investigate this was no an important part of this analysis.

> We can simply taken account of the variability that this causes in the scores so that we can make a more sensitive comparison between groups. This type of experimental design is often called a __randomised block design__.

An experiment designed to give this kind of data structure is usually called a __factorial experiment__, the different criterion variables being called __factors__.

> These 'factors' are entirely unrelated to those of __factor analysis__. The different values of each factor are often referred to as the __levels of the factor__.

However, the analysis carried out thus tests the differences between the sample means of the locations calculated over all the observations for an origin irrespective of the sex of the subject.

Any difference between the levels of a single factor which is independent of any other factor is referred to as __a main effect__.

Differences which appear only when two or more factors are examined together are called __interactions__.

Provided there is more than one observation for each combination of the levels of the main factors it is possible to test whether significant interaction effects are present.

To test for a significant interaction we simply expand the ANOVA to include an interaction sum of squares calculated by: interaction SS=(∑Yij.2/5)-CF

> The only extra feature requiring comment is that ht degrees of freedom for the interaction term are obtained by multiplying the degrees of freedom of the main effects included in the interaction: the symbol for the interaction effect, is a useful mnemonic for this.

> The F-ratio for testing the interaction effect is significant at the I% level, showing that such effects need to be considered.

The practical implication of this would be that when considering possible differences between the scores of subjects of different sex we should not leave out of consideration their geographical origin.

All one-way ANOVA test can be summarised neatly in a simple mathematical model: Yij=µieij, where Yij is the j-th score observed at the i-th location, µi is the population mean at the i-th location, and eij is the random amount by which the j-th score, randomly chosen at the i-th location, deviates from the mean score.

> Although this simple model is perfectly adequate for the one-way ANOVA problem, it does not generalise easily to more complex cases such as the factorial experiment.

Li=Mi-M, which is the difference between the mean of the overall population and the mean score of the population of scores of value from the i-th location, µi,,.

> µi=µ+Li, and sustituting this into the previous model: Yij=µ+Li+eij

> Some values in such a model, Yij and eij, depend on the specific data values observed in the experiment. Others, µ and Lij are assumed to be fixed for all the different samples that might be chosen; they are population, as opposed to sample, values and are referred to as __the parameters of the model__. µ is usually called the __grand mean__ and Li the __main effect__. of origin i.

The previous null hypothesis that all the µi had the same value, µ, can now be restated as H0:Li=o, for every value of i. This model can be generalised to cover a huge variety of situation.

> A suitable model would be: Yij+µ+bi+gj+eij which says that each score, Yij, is composed of four components summed together, the grand mean, µ, the __block effect__, bi, the __group effect__, gj, and the random variation eij about the mean score of judges of type j scoring the error i for its gravity.

We can also examine the degree to which a particular score is well or badly fitted by the model, by calculating the value of the __random__ or __residual__ component of the score, eij.

The __esidual error__ the difference between the observed and fitted values seem rather large, which suggest a good correspondence between the observed and fitted values of the score.

> This brings us to the last parameter which apparently has not yet been estimated, namely σ2, the random error variance or residual variance.

> This value is important when it comes to deciding which types of judges do seem to be giving different scores, on average, for the errors used in the study.

There are theoretically correct procedures for making __multiple comparisons__ - comparing all the possible pairs of means - but they are not simple to carry out.

A frequently adopted rule of thumb is the following.

> Provided that the ANOVA has indicated a significant difference between a set of means, calculated the standard error s\* for the comparison of any pair of means by: s*=√[(2*residual mean square)/n], where n is the number of observations which have been averaged when calculating each mean.

Then find the difference between each pair of means.

1. If the difference between a pair of means is greater than 2s\*, take this as suggesting that the corresponding population means may be different.

2. If the difference in two sample means is greater than 3s\*, take this as reasonably convincing evidence of a real difference.

It is important always to consider the observed magnitude of the difference in the means as estimated from the data and ask whether they seem large enough to be important, whether or not they are found to be significant by a statistical hypothesis test.

However in Yijk=µ+Li+Sj+eik, there is an assumptions that, apart from the random variation, eijk, each score can be reconstructed by the addition of three parameters, the grand mean plus the effect of having origin i pus the effect of the subject being of sex j.

This model will not give an adequate description of the data.
There seems to be an interaction between sex and location, males scoring better, on average, in one location and females scoring in another.
In this example, it is quite unhelpful to say that the mean scores for the different sexes are about equal when that hides the fact that, between some origins, there seems to be an important difference of scores.

In order to make this comparison we have to use the standard error for comparing interaction means.
In any case, an observed average difference of IO makes in a test which was scored out 50 is sufficiently large to merit further investigation.

__Fixed effects model__: Yijk = µ+Li+Sj+eijk, the results will not extend to other origins.

__Random effect__: the four levels of the factor being chosen randomly from a population of possible levels.

For a one-way ANOVA the calculations and the F-test are carried out exactly the same whether or not origin is viewed as a fixed or random effect.

However, we have frequently indicated that, whatever the results of a hypothesis test, it is always advisable to estimate the parameters of any model in case important effects have been missing by the statistical test or unimportant effects exaggerated.

With higher order ANOVA (that is, two-way or mode), even the F-tests will differ, depending on which effects we assume to be random or fixed, though the actual calcu we have to use the standard error for comparis will always be the same.

Every different mixture of random and fixed effects gives rise to different sets of F-ratios and the greater the number of factors the greater is the number of possible combinations.

It is sensible to avoid the random factors effects assumption wherever possible, choosing levels of the different factors for well-considered experimental reasons rather than randomly.

The fixed effects model is always easier to interpret because all the parameters can always be estimated.

Remember that an important assumption of the ANOVA model is that the variability should not depend on the levels of the factors. It may very well be that, say, different sets of judges find it easier to agree about the gravity of one type of error than the gravity of another.

> The variance of scores on the latter error would be greater than on the former.

> If the difference is large this could have serious implications for the validity of the ANOVA.

A completely reliable test would be one in which an individual subject would always obtain exactly the same score if it were possible for him to repeat the test several times.

In fact, a subject taking the test will not usually express his true score exactly, due to random influences.

> The score actually observed for the i-th subject will be Yi=µi+ei where the error, ei is usually assumed to be normally distributed with mean zero and some variance, σ2.

> This model can be written: Yij=µ+ai+eij, where µ is the mean 'true' score of all the students in the population and ai is the difference between the 'true' score of the i-th student and the mean for all student.

Since we had previously assumed that true scores were normally distributed with mean µ and variance σb2, the values ai will be from a normal distribution with mean zero and variance σb2.

> Now if the measurement error variance is close to zero, all the variability in scores will be due to differences in the true scores of students. A common reliability coefficient is rel=σb2/(σb2+σ2), which is the proportion of the total variability which is due to true difference in the subjects.

> If rel=1, there is no random error. If the rel is close to zero, the measurement error is large enough to hide the true differences between students.

> It can be shown that rel=𝘱, the correlation between two repetitions of the same test over all the subjects, and rel is frequently estimated by r, the correlation between the scores of a sample of subjects each of whom takes the test twice.

It is simply not possible to administer exactly the same test to a group of subjects on different occasions. it is much more common to administer two forms of the same test.

The random effects ANOVA model provides a different method for estimating the reliability and also offers the possibility of checking the assumption that the 'parallel forms' of the test do measure the same thing in the same way.

There are two ways to tackle the analysis of this data.

1. One is to assume that the parallel forms are equivalent so that the data can be considered as two independent observations of the same trait score on ten students.

2. The correlation between the two sets of scores would frequently have been used as an estimate of the reliability.

    The sample correlation will be a good estimator of the reliability only if it is true that the parallel forms of the test really do measure the same trait on the same scale.

To obtain this second ANOVA we have assumed the model: Yij=µ+ai+fj+eij, where fj is the difference between the overall mean score µ of all forms of the test over the whole population and the man of the j-th form used in this study over the whole population, i.e the main effect of forms.

> The F-ratio corresponding to this effect is highly significant, showing that the mean marks of different forms is not the same.

In fact, the use of the correlation coefficient ignores entirely the variability caused by using different forms.

The ANOVA method extends with no difficulty to the case where several parallel forms have been used.

There are two special points, of some importance in linguistic research, which need to be mentioned:

1. The possibility of transforming data which do not meet the assumptions required for ANOVA to a different forms which do.

        There are many possibilities, depending on the specific features of the original data which might cause problems.

a. However, one special case which may arise fairly frequently in applied language studies is data in the form of proportions or percentages. Such data would lack symmetry and could not be normally distributed. Furthermore, since most of the subjects would then have very similar scores, the sample variance would be small.

b. Provided most of the subjects in the experiment obtained scores in the range 20%-80% it would probably be acceptable to analyse thee raw scores directly.
However, if more than one or two scores lie outside this range, in particular if any scores are smaller than 10% correct or greater than 90% correct, it will not be safe to analyse them by the methods of earlier chapters without first transforming them.
Arsine transforming: the traditional way to change the scores of the individual subjects to scores on a different scale in such a way that the new scores will be normally distributed and have constant variance.
If the variance of the values in the different groups seems to be roughly proportional to their means then analysing the logarithms of the original values will give more reliable results.
If, instead, the standard deviations of the groups are proportional to their means, taking square root will help.
In some situations, the subjects are divided into groups and each subjects is measured on several variables.
The observation Yijk will be the reaction time of the k-th subject of the i-th nationality to the j-th stimulus.
The comparison of stimulus can be carried out within each subject while the comparison of nationalities can only be carried out between sets of subjects.
Variation in the reaction times of a single subject on different applications of the same stimulus is likely to be rather less than variation between subjects reaching to the same stimulus.
Stimulus can therefor be compared more accurately than nationalities from such a design.
Standard texts on ANOVA often refer to this as a split-plot design since it typically occurs when several large agricultural plots (subjects) are treated with different fertilisers and then several varieties of a cereal are grown in each plot.
