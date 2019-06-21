# CA5 Random Signals and Spectrum Estimation
## 1. Generate and plot a random signal
Plot the signal. In a second plot, plot a length 100 segment of the signal with both lines and asterisks (to get a better idea of what the signal looks like). (The np.s_[] function is handy for repeating a slice.)
## 2. Calculate and plot the DFT of the signal.
As the title says, calculate the DFT and plot the magnitude of the DFT. The signal is noisy and therefore so is the DFT.
## 3. Verify Parseval's Theorem
Parseval's theorem says
∑n=0N−1|x[n]|2=1N∑k=0N−1|X[k]|2
∑n=0N−1|x[n]|2=1N∑k=0N−1|X[k]|2
 
Verify this for x.
## 4. Use the Welch Spectrum Estimator
The DFT is noisy, not surprising since the signal is pure noise. For noisy signals the Welch estimator does a better job than the DFT. Plot the Welch spectrum estimate.
## 5. Low pass filter
Generate a lowpass signal y from x using a basic lowpass filter, e.g., length 15 and cutoff 0.25 of the Nyquist rate. Plot y. As above, plot a short segment with both asterisks and lines.
## 6. Calculate the plot the Welch estimator for y
## 7. Plot the Spectrum Estimate and Filter Response on same curve
On the same axes, plot the Welch spectrum estimate of y and the filter's magnitude response. Use a log scale on the Y-axis. The two curves should be close, i.e., the spectrum estimate should be close to the filter magnitude response. (Putting noise into a filter is a traditional technique for measuring a filter's response.)

Notes: The Welch (and other spectral estimates by default only output the positive frequency half of the spectrum. Accordingly, they multiply the spectrum estimate by 2. However, sig.freqz does not multiply by 2. Also, spectrum estimates output estimated energy, while frequency response is magnitude.
## 8. Add a sinusoid
Create a new signal z by adding a sinusoid to y. Make sure the frequency of the sinusoid is within the passband of the filter. Use a sinusoidal amplitude of 0.5. Plot a segment of z.
## 9. Plot Spectrum Estimate of Sinusoid With Noise
Plot the Welch spectrum estimate of z. Where is the sinusoid? Annotate your plot with an indication of where the sinusoid is.
## 10. High Pass Filter
Filter x with a high pass filter (cutoff = 0.75 of Nyquist) and plot a segment with asterisks and lines.
## 11. Spectrum and Filter Response
Repeat step 7 for the high pass signal. Plot both the spectrum estimate and filter response on the same plot (with a log scale on the Y-axis). Both curves should be close together.
