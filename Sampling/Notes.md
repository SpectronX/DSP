### Introduction

What's the one characteristic of almost every real-world signals we encounter in our lives daily? 
They are continuous signals.

From the light of bulbs lighting our rooms, to the light from distant stars reaching Earth, all these signals are continuous in nature.

A signal is considered continuous if it is defined at every instant of time and spans over a continuous range of values. 
Imagine a graph of a one-cycle sine wave with its magnitude plotted against time. 
The magnitude of the sine wave can be determined at any point in time, even at the one-thousandth of a second.
This demonstrates how the signal, at every point in time, has a well-defined value.

Then comes electronics: the power that drives virtually every device on our planet.
The basis of the operation of electronic devices is how they handle data: in binary form.
Using transistors, the state is either ON or OFF, 1 or 0. There are no values in between.
It becomes evident that signals in continuous time cannot be directly processed by digital systems.
since they would require an infinite amount of memory for processing. 
Remember, a continuous signal has values at every point in time: infinite number of points.

How do we then take a signal, continuous in nature, and process it with digital devices? Sampling.

Sampling
With sampling, we're simply taking snapshots of the signal at specific time instances.
So, using our sine wave, if we sample the signal every 1 second,
we're effectively recording the magnitude of the sine wave at every 1 second.
This in turn gives us the discrete values of time along with the corresponding magnitude at those times.

In the continuous form, we could have asked what the value of the signal was between 1 second and 2 seconds.
In the discrete form, there is no defined value between 1 second and 2 seconds: it's simply the values at 1 second and at 2 seconds

Ways of sampling
When dealing with real electronics, an analog-to-digital converter (ADC) performs the sampling process.
A Digital-to-analog converter (DAC) performs the reverse operation 
By applying a sample-and-hold method, the converter takes discrete-time values of the signal at a defined sampling rate.
In code, which would mostly be done here, all one needs to do is explicitly define the sampling period or sampling frequency.
A stem plot is often used to show the values of a signal at discrete time instants
However, if the signal is not sampled properly, one might reconstruct the original signal as one with a different frequency.
The term that describes this phenomenon is \emph{Aliasing}
