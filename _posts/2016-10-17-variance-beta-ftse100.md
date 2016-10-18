---
layout: post
title:  "Variance and Beta of Daily Returns of FTSE 100 Components"
date:   2016-10-17 16:54:11 +0100
category: finance
tags: [ftse100,variance,beta]
---
The concept of market $$\beta$$ is often confused with that of variance $$\sigma^2$$ when referring to daily returns of a liquid risky asset. 
In this context, $$\beta$$ is the coefficient estimated by ordinary least squares in a linear regression model such as the following:


$$ r_t = \alpha + \beta m_t + \epsilon_t \, , \, t = 1,\ldots,T $$


where $$r_t$$ and $$m_t$$ are respectively the returns on the risky asset and on the aggregate and representative market of risky assets at time $$t$$.

The variance $$\sigma^2$$ is calculated without taking reference to the market returns $$m_t$$ and it's done in fact asset by asset. Indeed, we define variance $$\sigma^2$$ in this context in the following manner:


$$ \sigma^2 = \frac{ \sum_{t=1}^{T} (r_t - \mu)^2 }{T} $$


where $$\mu = \frac{\sum_{t=1}^{T} r_t}{T}$$ is the arithmetic mean of the returns $$r_t$$ of the risky asset.

It is often assumed that those assets that demonstrate a high market $$\beta$$ ought to be more risky than those assets that manifest a low market $$\beta$$. This last statement holds true for the great majority of assets, as one can see in the graph below.