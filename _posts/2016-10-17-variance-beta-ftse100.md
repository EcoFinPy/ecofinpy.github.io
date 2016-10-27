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

We calculate the returns on the risky asset $$r_t$$ and on the market $$m_t$$ in the same way:


$$ r_t = \ln(\frac{p_t}{p_{t-1}}) $$


where $$p_t$$ is the price of the asset at time $$t$$ adjusted for any distributions (such as dividends) and stock-splits. In calculating $$m_t$$ we use the float-adjusted capitalization of the market, adjusted for any distributions and for any additions or removals from the refernce market of assets, as the price of the market over time. A more concrete proxy of the price of the market is the adjusted market price of Exchange Traded Funds (ETFs) that are actively traded and that aim to track the same reference market. 

The variance $$\sigma^2$$ is calculated without taking reference to the market returns $$m_t$$ and it's done in fact asset by asset. Indeed, we define variance $$\sigma^2$$ in this context in the following manner:


$$ \sigma^2 = \frac{ \sum_{t=1}^{T} (r_t - \mu)^2 }{T} $$


where $$\mu = \frac{\sum_{t=1}^{T} r_t}{T}$$ is the arithmetic mean of the returns $$r_t$$ of the risky asset. In calculating the variance $$\sigma^2$$ of $$r_t$$ we assume that each observation in our sample of returns is equally likely to occur.

Riskiness of an asset is often deemed to be roughly measured by the actual historical volatility $$\sigma$$ of the returns. Thus, an asset with returns that manifest a higher historical volatility compared to the historical volatility associated with an other asset is deemed to be more risky than that other asset. The actual historical volatility $$\sigma$$ of the returns is simply defined by the square root of the variance $$\sigma^2$$ of the same returns.

It is often assumed that assets that demonstrate a high market $$\beta$$ ought to be more risky than those assets that manifest a low market $$\beta$$. This last statement holds true for the great majority of assets, as one can see in the graph below where we visualize the realized volatility and market beta for each component of the FTSE 100 index as of {{ page.date | date: '%B %d, %Y' }}.


![Market Beta and Realized Volatility]({{ site.url }}/assets/beta_sigma_data.jpeg)

It is clear that for the vast majority of the components of the FTSE 100 index there is a satisfactory tight relationship between Market Beta and realized volatility given that a majority of the points of the scatter plot are clustered approximately near to the fitted regression line. Nonetheless, there are still a few components that are substantially distant with respect to the fitted regression line. These components have manifested an exceptionally low Market Beta for the level of their high realized volatility.
This fact may be wholly explained by the fact that the risk profile of these components is likely to be affected much more by idiosyncratic risk factors than systematic risk factors. We denote the tickers of the companies that lie particularly distant from the regression line in the scatter plot above right next to their points.

One can conclude that Market Beta and realized volatility can sometimes differ widely. This fact has to be kept in mind when one aims to construct a measure of future predicted risk of an investment into a company's equity.