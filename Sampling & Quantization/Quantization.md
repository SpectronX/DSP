### Quantization

A mathematical function, \(y = f(x)\), has \(x\) as the independent variable and \(y\) as the dependent variable. When this relation is plotted, we get the values of \(y\) on the \(y\)-axis and that of \(x\) on the \(x\)-axis. In sampling, the independent variable is converted from continuous to discrete. Quantization handles the discretization of the dependent variables.

While sampling takes snapshots of the signal in steps of the sampling period, quantization defines discrete levels for which the signal magnitude is represented. For example, the magnitude of a sine wave lies between -1 and 1. The magnitude can therefore take any value within this range. If we define the number of quantization levels as 8, then it means we need to have only 8 values between -1 and 1, discarding the infinite number of values in between.

### Method of Quantization

First, the number of quantization levels is defined. This is determined by the number of bits used in the quantizer. The number of bits would also determine the resolution of the quantization. The formula to calculate the number of levels \(L\) is:

$$ L = 2^{\text{No of bits}} $$

This formula gives the number of combinations we can obtain with the number of bits we have. 
- 2 bits give 4 combinations of 0s and 1s.  
- 3 bits give 8 combinations of 0s and 1s.

Next, we determine the length/range of the signal. This can also be obtained through the formula:

$$ R = y_{\max} - y_{\min} $$

In the case of a sine wave, its length would be: $$ 1 - (-1) = 2 $$

The quantization levels are defined in steps. A step is calculated using the formula:
$$ \Delta = \frac{R}{L} = \frac{(y_{\max} - y_{\min})}{2^n} $$

Therefore, with a 3-bit quantizer, we have 8 levels with a step size of: $$ \frac{2}{8} = 0.25 $$

Here is a table that shows the various binary representations for 3 bits and their corresponding quantization levels:
