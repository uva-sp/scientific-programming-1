# Fitting data and evaluating errors

![embed](https://player.vimeo.com/video/138378099)

To figure out the inner workings of (physical) phenomena, data is collected to examine any dependencies. That could be the mass of the Higgs boson, the decay of uranium, but also the number of children in a family as function of the average length of the parents. You could look for a (causal) relationship: linear, exponential etc. and in the process determine the corresponding parameters and their margin for error. If you've found a fitting description you can then do predictions using that model. Each measurement is accompanied by an uncertainty that indicates the precision by which the magnitude is measured. The smaller the error, the more accurate the measurement and the more 'important' it is in regards to comparing the measurements to your model.

To find the 'best' value we need a measure (metric) that describes the 'quality' of the fit. Here we use the  $$\chi^2$$-measure: the sum of the average deviation of the measurements and the model weighed by their error.

For each point we determine *how many standard deviations the point is away from my model/predictions?*.

$$\chi^2 = \sum_{i~ {\rm (datapoints)}}  \left(\frac{  y_i - f(x_i|\vec{\alpha}) }{\sigma_i}\right)^2$$

Here $$\vec{\alpha}$$ is the vector with parameters that are used in your model. For each choice of parameters in your model the distance of each measurement to the model changes and gives a new $$\chi^2$$. To be complete: the $$\chi^2$$ is just a number.

## The best value of your model and uncertainty

The best value of your model ($$\alpha_{best}$$) and the uncertainty of it ($$\Delta_{alpha}$$).

In the fitting procedure we look for the value of parameters in your model that result in the smallest $$\chi^2$$. Because those are the 'best' values of the model, since those values cause the model to best describe the data.

Each value of your parameters that is different than $$\alpha_{best}$$ will change the value of $$\chi^2$$ (it will increase which means there is a worse match with the data). The difference between the value of the $$\alpha$$ for which the $$\chi^2$$ would increase exactly 1 is called the uncertainty.

The result of your fit can be represented as follows:

$$\alpha = \alpha_{best} \pm \Delta_{alpha}$$

Although we assume that the error in $$\alpha$$ is symmetrical it does not mean that is always the case. Always evaluate the negative and positive error separately by monitoring how the $$\chi^2$$ changes when the parameters become respectively smaller and larger.

## Example: Wesley Sneijder

Someone has been intensively measuring the percentage of good passes ($$y$$-value) that Wesley Sneijder gave during the various matches ($$x$$-value) of the qualifier for the World Cup. Because the accuracy with which the percentage is determined depends on the number of passes in a match, the error won't be the same for each match.

match number (x)     |  1 |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 
$$f_{good}$$ (y)        | 55 | 50 | 39 | 58 | 54 | 57 | 78 | 66 | 62 | 82 
$$\sigma$$ (bad at y)  |  5 |  4 |  9 |  4 |  5 |  5 |  7 |  3 |  6 | 6

![](FitExampleCombined.png)

The data is represented on the left hand plot. We assume that Wesley's performance is constant and thus assume that the model that describes this data best is a constant. That means our model only has 1 parameter: $$f(x)=c$$. The questions is: *which value of $$c$$ describes the data best and which uncertainty should be attributed to that prediction?*.

## Calculating $$\chi^2$$

Let's try different values for $$c$$ and calculate for each of them the $$\chi^2$$. If, for example, we hypothesize a value of $$c=56$$ then the corresponding $$\chi^2$$ is:

$$
\begin{eqnarray}
   \chi^2(c=56)&=&    
   \tiny{
   \left( \frac{(55-56)}{5} \right)^2+
   \left( \frac{(50-56)}{4} \right)^2+
   \left( \frac{(39-56)}{9} \right)^2+
   \left( \frac{(58-56)}{4} \right)^2+
   \left( \frac{(54-56)}{5} \right)^2+
   \left( \frac{(57-56)}{5} \right)^2+
   \left( \frac{(78-56)}{7} \right)^2+
   \left( \frac{(66-56)}{3} \right)^2+
   \left( \frac{(62-56)}{6} \right)^2+
   \left( \frac{(82-56)}{6} \right)^2
   }\\
   &=&47.07
\end{eqnarray}
$$

You can now try different values of $$c$$ and calculate the $$\chi^2$$ for each. The distribution is drawn in the plot on the right hand side above. There is an obvious minimum present: at $$c=60.3$$ the $$\chi^2$$ is at a minimum, specifically $$\chi^2_{min} = 38.87$$. The value $$c=60.3$$ describes the data best. 

When calculating the $$\chi^2$$ we can see that there is an area $$ 58.8 < c < 61.8$$ for which the $$\chi^2$$ differs less than 1 unit with $$\chi^2_{min}$$. The boundaries on the left and right in hypotheses of $$c$$ are both 1.5 apart of $$c_{best}$$. As a result the uncertainty of $$c$$ is 1.5.

The result of the fit of our model to the data is as follows:
percentage good passes = $$ 60.3 \pm1.5$$

## Assignment: fitting a model to the data

Declare a function `fit()` in a file called **fit.py** that verifies the aforementioned result.

1. Create a plot of this data with the errors

    Tip: use the function `plt.errorbar(x, y, yerr=yerror)`. Search on the internet how to properly user this function.

2. `Print` the best value of $$c$$.

3. `Print` on a separate line the corresponding uncertainty $$\Delta_c$$.

Answer for yourself the question: how does the result change if the error on each of the measurements becomes twice as large?


## Testing

   checkpy fit