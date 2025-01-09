## Exam prep

### **Signals and Systems**

#### 1. **What is a signal?**

A **signal** is a function that conveys information about the behavior or attributes of a system or phenomenon. Signals can vary over time, space, or other dimensions. They can represent physical quantities like voltage, sound, temperature, or light intensity.

---

#### 2. **What can you do with a signal?**

- **Analyze**: Extract features, detect patterns, or measure properties (e.g., frequency, amplitude).
- **Modify**: Filter, amplify, compress, or transform (e.g., denoise a sound).
- **Transmit**: Send information across a medium (e.g., radio signals for communication).
- **Store**: Archive data for future use (e.g., images or audio files).
- **Synthesize**: Generate new signals (e.g., synthetic speech, animations).

---

#### 3. **What is a system?**

A **system** is any process or entity that takes an input signal, processes it, and produces an output signal. It can be a mathematical model, a physical device, or an algorithm.

Examples:

- An amplifier (increases signal amplitude).
- A filter (removes noise or certain frequencies).

---

#### 4. **Describe 3 signals where time is the independent variable and 3 where time is not.**

**Time as the independent variable:**

1. **Sound wave**: Amplitude of air pressure vs. time.
2. **Heartbeat signal**: Electrical voltage from an electrocardiogram (ECG) vs. time.
3. **Stock prices**: Value of a stock sampled at regular time intervals.

**Not dependent on time:**

1. **Image brightness**: Pixel intensity vs. spatial coordinates.
2. **Pressure map**: Pressure distribution over a surface (position vs. position).
3. **Temperature distribution**: Temperature in a room as a function of location.

---

#### 5. **What is the difference between a continuous and discrete signal?**

- **Continuous signal**: Defined for all points in time or space (e.g., analog sound waves).
- **Discrete signal**: Defined only at specific intervals (e.g., digital samples of audio).

---

#### 6. **What is the convention to recognize continuous and discrete signals?**

- Continuous signals: $x(t)$, where $t$ is a real number.
- Discrete signals: $x[n]$, where $n$ is an integer index.

---

#### 7. **What is the intuition behind sampling?**

Sampling converts a continuous signal into a discrete one by measuring its value at regular intervals. This allows digital systems to process analog signals.

---

#### 8. **How can block diagrams represent the interaction between signals and systems?**

Block diagrams use blocks and arrows:

- **Blocks**: Represent systems or operations.
- **Arrows**: Indicate the flow of signals between systems.

---

#### 9. **How can we use block diagrams to represent complex systems?**

Complex systems are modeled by connecting multiple blocks, where the output of one block serves as the input to another. This modular approach simplifies design and analysis.

---

#### 10. **Describe an example of a signal and system connected to AI (not in the book).**

- **Signal**: Sensor data from autonomous vehicles (e.g., LiDAR or camera images).
- **System**: A neural network processes these signals to detect objects and make driving decisions.

---

### **Sinusoidal Signals and Frequency Domain**

#### 11. **What is a sinusoidal signal?**

A periodic function, typically expressed as:

- $x(t) = A \sin(2\pi f t + \phi)$ or
- $x(t) = A \cos(2\pi f t + \phi)$, where $A$ is amplitude, ff is frequency, and $\phi$ is phase.

---

#### 12. **What are the components of a sinusoidal signal?**

1. **Amplitude (A)**: Peak value.
2. **Frequency (f)**: Cycles per second (Hz).
3. **Phase (ϕ)**: Horizontal shift.

---

#### 13. **Where do cosine and sine cross zero?**

- Sine: Zero crossings at t=0,π,2π,…
- Cosine: Zero crossings at t=π/2,3π/2,…

#### Where do they have maximum/minimum values?

- Sine: Maximum at t=π/2, minimum at t=3π/2.
- Cosine: Maximum at t=0, minimum at t=π.

---

#### 14. **How can we write sine in terms of cosine?**

$sin⁡(x)=cos⁡(x−π/2)$

---

#### 15. **What is the relation between period and frequency?**

$T = \frac{1}{f}$, where $T$ is the period, and $f$ is the frequency.

---

#### 16. **What is a periodic function?**

A function that repeats at regular intervals. For a function $x(t)$, it satisfies $x(t+T)=x(t)$.

---

#### 17. **What does a frequency equal to zero represent?**

A constant (DC) signal with no oscillations.

---

#### 18. **What is the relationship between sinusoidal and complex exponential signals?**

Using Euler’s formula:

- $e^{j\omega t} = \cos(\omega t) + j\sin(\omega t)$, sinusoids can be represented as combinations of complex exponentials.

---

#### 19. **What is Euler's formula?**

$e^{j\theta} = \cos\theta + j\sin\theta$.

#### What about the inverse Euler's formula?**

- $\cos\theta = \frac{e^{j\theta} + e^{-j\theta}}{2}$
- $\sin\theta = \frac{e^{j\theta} - e^{-j\theta}}{2j}$

---

#### 20. **How do you sum sinusoidal signals with the same frequency?**

Use trigonometric identities to combine amplitudes and phases.

---

#### 21. **What is the benefit of representing signals in the frequency domain?**

It simplifies analysis, filtering, and manipulation by isolating frequency components.

---

#### 22. **What do you need to represent a sinusoid in the frequency domain?**

- Amplitude.
- Frequency.
- Phase.

---

#### 23. **What is the independent variable to describe a signal in the frequency domain? Is time still relevant?**

The independent variable is frequency (ff). Time is not directly represented but is relevant for interpreting transformations.

---

#### 24. **What formula do you use to move from time to frequency domains?**

The Fourier Transform:$X(f) = \int_{-\infty}^\infty x(t)e^{-j2\pi ft} dt$.

---

#### 25. **How do you read a spectrum representation?**

The spectrum shows amplitude (and sometimes phase) as a function of frequency. Peaks correspond to dominant frequency components.

---

#### 26. **What is the fundamental frequency? And how do you compute it?**

- The **fundamental frequency** is the lowest frequency at which a periodic signal repeats.
- Compute it as the reciprocal of the period (T):  
    $f_0 = \frac{1}{T}$

---

#### 27. **Is there any way to check if a fundamental frequency exists?**

A signal must be periodic to have a fundamental frequency. Check if the signal satisfies:  
$x(t + T) = x(t)$, for some $T > 0$.

---

#### 28. **What are the harmonics? And how do you calculate them?**

- **Harmonics** are integer multiples of the fundamental frequency ($f_0$).
- Formula for $n$-th harmonic:  
    $f_n = n \cdot f_0$, where $n = 1, 2, 3, \dots$

---

#### 29. **What is the DC component in a signal?**

The **DC component** is the average value of the signal over a period. For a periodic signal x(t)x(t), it is:  
$X_{\text{DC}} = \frac{1}{T} \int_0^T x(t) dt$

---

#### 30. **What is a periodic signal?**

A signal $x(t)$ is periodic if it repeats itself after a period $T$:  
$x(t + T) = x(t)$

---

#### 31. **Can we represent periodic signals as a function of other simpler periodic signals?**

Yes, periodic signals can be represented as a sum of sinusoids (Fourier Series):  
$x(t) = \sum_{n=-\infty}^\infty C_n e^{j2\pi n f_0 t}$,  
where $C_n$ are coefficients, $f_0$ is the fundamental frequency.

---

#### 32. **What are the steps to multiply sinusoids in the frequency domain?**

1. Represent the sinusoids in the frequency domain.
2. Perform **convolution** in the frequency domain, as multiplication in time corresponds to convolution in frequency.

---

#### 33. **What is the idea behind AM radio broadcasts?**

**Amplitude Modulation (AM)** encodes information by varying the amplitude of a carrier sinusoid. The carrier frequency remains constant, while its amplitude reflects the message signal.

---

#### 34. **How can we encode information as the amplitude of a sinusoid?**

Using **Amplitude Modulation (AM)**:

- Carrier signal: $c(t) = A_c \cos(2\pi f_c t)$,
- Modulated signal: $s(t) = [1 + m(t)]c(t)$, where $m(t)$ is the message signal.

---

#### 35. **What is the idea behind FM radio broadcasts?**

**Frequency Modulation (FM)** encodes information by varying the frequency of a carrier sinusoid. The amplitude of the carrier remains constant.

---

#### 36. **How can we encode information as the angle (frequency and phase) of a sinusoid?**

Using **Frequency Modulation (FM)**:

- Carrier signal: $c(t) = A_c \cos(2\pi f_c t + \phi(t))$, where $\phi(t)$ is the phase determined by the message signal m(t)m(t).

---

#### 37. **What is a Chirp signal? Is there any relationship between this signal and FM?**

A **chirp signal** is a sinusoid with a frequency that increases or decreases over time:  
$x(t) = A \sin(2\pi f(t)t)$, where $f(t)$ varies with time.

- Chirps are related to FM as they involve frequency modulation with a time-varying frequency.

---
#### 38. **Why do we need to convert continuous signals to discrete-time? How can we do it?**

Digital systems require discrete-time signals for processing. Conversion is done through **sampling**, where the signal is measured at regular intervals:  
$x[n] = x(nT_s)$, where $T_s$ is the sampling period.

---

#### 39. **What are the sampling frequency and period?**

- **Sampling frequency ($f_s$)**: Number of samples per second ($f_s = 1/T_s$).
- **Sampling period ($T_s$)**: Time between successive samples ($T_s = 1/f_s$).

---

#### 40. **What is the intuition behind the Aliasing phenomenon?**

Aliasing occurs when the sampling frequency is too low, causing different signals to appear indistinguishable. It results in distortion and overlaps in the frequency domain.

---

#### 41. **What is the importance behind the Nyquist rate?**

The Nyquist rate ensures no aliasing occurs. It states the sampling frequency must be at least twice the highest frequency component in the signal:  
$f_s \geq 2f_{\text{max}}$.

---

#### 42. **Why do we need to convert discrete signals to continuous time? How can we do it?**

Conversion allows for reconstruction and interaction with analog systems. It is done using **interpolation**, typically with a low-pass filter.

---

#### 43. **How can we reconstruct continuous signals from discrete ones?**

If $f_s \geq 2f_{\text{max}}$, use a reconstruction filter (low-pass filter) to interpolate the sampled points. Commonly, a **sinc interpolation** is used.

---
#### 44. **What is a filter? How is it related to a system?**

A filter is a system designed to enhance or suppress specific components of a signal (e.g., low-pass, high-pass filters).

---

#### 45. **What is a unit impulse signal?**

A **unit impulse signal** $\delta[n]$ is a discrete signal that is zero everywhere except at $n = 0$, where it equals 1.

---

#### 46. **How can we write discrete signals as unit impulse signals?**

Any discrete signal $x[n]$ can be written as:  
$x[n] = \sum_{k=-\infty}^\infty x[k]\delta[n-k]$

---

#### 47. **What is a finite impulse response filter?**

An FIR filter processes a signal using a finite number of past and present inputs. Its output is a weighted sum of the input samples.

---

#### 48. **What is a difference equation?**

A **difference equation** describes the relationship between input and output signals of a system. Example:  
$y[n] = a_1 y[n-1] + b_0 x[n] + b_1 x[n-1]$

---

#### 49. **What is the support of a signal (or a function)?**

The **support** of a signal is the range of the independent variable where the signal is nonzero.

---

#### 50. **Consider the time 'n' as the present. What do $x[n]$, $x[n-1]$, and $x[n+1]$ represent?**

- x[n]x[n]: Current value.
- x[n−1]x[n-1]: Previous value.
- x[n+1]x[n+1]: Future value.

---

#### 51. **What is a causal filter?**

A filter is **causal** if its output at any time depends only on present and past inputs, not future inputs.

---

#### 52. **What is the general form of a causal FIR filter?**

$y[n] = \sum_{k=0}^M h[k]x[n-k]$,  
where $h[k]$ are filter coefficients, and $M$ is the filter order.

---

#### 53. **What is a convolution? How do you compute a convolution in a 2D signal?**

Convolution is the integral (or sum in discrete cases) of the product of two signals, one of which is flipped and shifted. For 2D signals, it is computed as:  
$y[m,n] = \sum_{i}\sum_{j}x[m-i, n-j]h[i, j]$

---

#### 54. **How can we interpret FIR filters as convolutions?**

An FIR filter computes the convolution of the input signal with the filter's impulse response.

---

#### 55. **What are delaying, multiplying, and adding units?**

- **Delaying**: Shifts the signal in time.
- **Multiplying**: Scales the signal by a coefficient.
- **Adding**: Combines multiple signals.

---

#### 56. **How can we interpret those units in block diagrams?**

They represent operations performed on signals as part of a larger system.

---

#### 57. **What is time invariance in a system?**

A system is **time-invariant** if shifting the input results in an equivalent shift in the output.

---

#### 58. **What is linearity in a system?**

A system is **linear** if it satisfies superposition:

1. Scaling: $x[n] \to a y[n]$.
2. Additivity: $x_1[n] + x_2[n] \to y_1[n] + y_2[n]$

---

#### 59. **What is a linear time-invariant system? Why is it special?**

An **LTI system** is both linear and time-invariant. It is special because its behavior is fully described by its impulse response, and it has straightforward frequency domain analysis.

---

#### 60. **How can we compute a correlator in an image?**

A correlator computes the similarity between an image and a template by performing convolution.

---

#### 61. **What is Sobel edge detection?**

Sobel edge detection is a method for finding edges in images. It uses convolution with Sobel kernels to compute image gradients, highlighting regions of high intensity change.

---

#### **62. How can we write FIR filters in terms of frequency?**

FIR filters can be expressed in terms of their **frequency response** $H(e^{j\omega})$:  
$H(e^{j\omega}) = \sum_{n=0}^M h[n] e^{-j\omega n}$,  
where $h[n]$ are the filter coefficients and $\omega$ is the angular frequency. This is essentially the **Discrete-Time Fourier Transform (DTFT)** of the filter's impulse response.

---

#### **63. What is the interpretation behind the magnitude and angle for FIR filters?**

- The **magnitude** $|H(e^{j\omega})|$ represents the **gain** of the filter at a specific frequency ω\omega.
- The **angle** $\arg(H(e^{j\omega}))$ represents the **phase shift** introduced by the filter at that frequency.

---

#### **64. How do a sinusoid's amplitude, frequency, and phase change after applying an FIR filter?**

When an FIR filter is applied to a sinusoidal signal:

- The **amplitude** is scaled by $|H(e^{j\omega})|$.
- The **frequency** remains unchanged.
- The **phase** is shifted by $\arg(H(e^{j\omega}))$.

---

#### **65. Can the gain in a filter be negative?**

Yes, a filter can have a **negative gain**, which means the output sinusoid is inverted in phase (a $180^\circ$ phase shift) while retaining its magnitude.

---

#### **66. How can we eliminate frequencies in a signal?**

To eliminate specific frequencies, use a **filter** designed to attenuate those frequencies. Examples include:

- **Low-pass filters**: Eliminate high frequencies.
- **High-pass filters**: Eliminate low frequencies.
- **Band-stop filters**: Eliminate frequencies in a specific range.
- **Notch filters**: Eliminate a very narrow frequency band.

---

#### **67. How can we interpret a convolution operation in the spectrum domain?**

Convolution in the time domain corresponds to **multiplication** in the frequency domain:  
$x[n] * h[n] \xleftrightarrow{\text{Fourier}} X(e^{j\omega}) H(e^{j\omega})$.  
This means the output spectrum is the product of the input spectrum and the filter's frequency response.

---

#### **68. How can we handle cascade LTI systems in the spectrum domain?**

For cascade systems, the total frequency response is the product of the individual system responses:  
$H_{\text{total}}(e^{j\omega}) = H_1(e^{j\omega}) H_2(e^{j\omega})$.

---

#### **69. Is there a systematic way to transform signals from the time to the frequency domain?**

Yes, the **Discrete Fourier Transform (DFT)** provides a systematic way to move signals from the time domain to the frequency domain.

---

#### **70. What is the DFT formula? (Hint: Search for the matrix form as well)**

The DFT formula for a signal $x[n]$ of length $N$:  
$X[k] = \sum_{n=0}^{N-1} x[n] e^{-j\frac{2\pi}{N}kn}, for k=0,1,…,N−1k = 0, 1, \dots, N-1$.

Matrix form:  
Let $\mathbf{W}$ be the **DFT matrix** of size $N \times N$, where $W_{m,n} = e^{-j\frac{2\pi}{N}mn}$  
Then$\mathbf{X} = \mathbf{W} \mathbf{x}$, where $\mathbf{x}$ is the input signal vector.

---

#### **71. Is there any constraint in the input signals for using the DFT?**

The DFT assumes the input signal is:

1. **Periodic** with period $N$.
2. **Finite in length**, typically padded with zeros if necessary.

---

#### **72. Where are the principal frequencies in the signal?**

The **principal frequencies** are found in the range $[0, \frac{f_s}{2}]$ for a real signal, corresponding to the **positive frequencies**.

---

#### **73. Does a real signal have negative frequencies with the DFT?**

Yes, but for real signals, the negative frequencies are **conjugates** of the positive frequencies. This redundancy is exploited in analysis.

---

#### **74. How can we move a signal from the frequency to the time domain?**

Use the **Inverse Discrete Fourier Transform (IDFT)**:  
$x[n] = \frac{1}{N} \sum_{k=0}^{N-1} X[k] e^{j\frac{2\pi}{N}kn}$, for $n = 0, 1, \dots, N-1$.

---

#### **75. How does the fast Fourier transform simplify the DFT calculation?**

The **Fast Fourier Transform (FFT)** reduces the computational complexity of the DFT from $O(N^2)$ to $O(N \log N)$ by exploiting symmetries and redundancies in the DFT computation.

---

#### **76. Is it possible to compute a convolution by using DFT?**

Yes, convolution can be computed using the DFT:

1. Take the DFT of both signals.
2. Multiply their spectra point-wise.
3. Perform the IDFT of the product to obtain the result.

---

#### **77. What is the definition of the z-transform for a finite-length discrete signal?**

The **z-transform** of a discrete signal $x[n]$ is:  
$X(z) = \sum_{n=-\infty}^\infty x[n]z^{-n}$,  
where $z$ is a complex variable.

---

#### **78. What is the interpretation of the z-transform?**

The z-transform provides a frequency and time-domain hybrid representation of discrete signals. It generalizes the DTFT and is useful for analyzing system stability and behavior.

---

#### **79. In particular, what is the interpretation behind $z^{-1}$?**

The term $z^{-1}$ represents a **unit delay** in the time domain.

---

#### **80. What is the advantage of analyzing discrete signals in the z-domain?**

Analyzing signals in the z-domain simplifies operations (e.g., convolution becomes multiplication). It also allows us to solve difference equations and study system stability using the pole-zero plot.

---

#### **81. What is the z-transform of a FIR filter?**

For an FIR filter with coefficients $h[n]$  :
$H(z) = \sum_{n=0}^M h[n]z^{-n}$.

---

#### **82. What is a convolution, $x[n]*h[n]$, in the z-domain?**

Convolution in the time domain corresponds to **multiplication** in the z-domain:  
$X(z)H(z)$.

---

#### **83. How can we analyze LTI cascade systems in the time domain?**

For cascade systems, convolve the impulse responses of the individual systems:  
$h_{\text{total}}[n] = h_1[n] * h_2[n]$.

---

#### **84. What are the zeros of the system function?**

The **zeros** are the roots of the numerator of the system function $H(z)$.

---

#### **85. What is the interpretation of the zeros?**

Zeros represent frequencies where the system's output is attenuated completely.

---

#### **86. What are the poles of the system function?**

The **poles** are the roots of the denominator of the system function $H(z)$.

---

#### **87. What is the interpretation of the poles?**

Poles determine the system's stability and resonance characteristics. If poles lie outside the unit circle in the z-plane, the system is unstable.

---

#### **88. How to derive a Laplace transform?**

The Laplace transform of a function $f(t)$ is defined as:  
$F(s) = \int_{0}^\infty f(t)e^{-st} dt$,  
where $s$ is a complex variable.

---

#### **89. How to solve ODEs using Laplace transforms?**

1. Take the Laplace transform of both sides of the ODE.
2. Solve for the transformed variable $F(s)$.
3. Use the inverse Laplace transform to find the solution in the time domain.

### Questions inspired by previous exams:
- when f when $\omega$ 
	the standard for should be $x(t)=Acos(\omega_{0}+\varphi)$ with $\omega_{0=2\pi}f$, where $f$ is a cyclic frequency and $T=\frac{1}{f}$
	in the time-domain we use $x(t)=Acos(2\pi ft+\varphi)$, so just assume the if 2$\pi$ appears in the formula, they use f and $\omega$ otherwise
- calculating $\varphi$ 
	find timestamp at which the signal has reached nice number of oscillations from the 0 point, then compare the argument of the cosine with argument of cosine of f = 1 and no shift at time equal to the number of oscillations, solve for theta)
	e.g. $150\pi(0.045)+\varphi=2\pi(3.5)$
- proper calculations of complex signals (is it sinsin, sincos or coscos)
	if pattern repeats but up-and-down then it is sincos, coscos for beat notes (∑ of 2 periodic signals wth the same amplitude and nearly identical frequency, giving a new periodic signal alternating up and down and enveloping, but repeating one pattern not 2)
- how to go from a signal formula to its frequency spectrum and vice versa?
	put $f_0$ of the f axis and the value of $0.5Ae^{j\varphi}$ on the vertical, don't forget to do the same for the conjugate (reverse all signs)
- finding Fourier coefficients from a spectrum and/ or a signal
	- we're taking phasors
- finding sampling frequencies for input going through a perfect C-to-D and vice versa
	$x[n]=x(nT_s)=x(\frac{n}{f_s})$
- finding Nyquist rate for a signal and the Nyquist sampling rate
	Continuous frequency with highest frequency $f_{max}$ can be reconstructed exactly from discrete samples $x[n] = x(nT_s)$ if samples are taken at a rate $f_s > 2f_{max}$ (i.e. twice per oscillation).
- over/undersampling and aliasing
	over if above the Nyquist rate, under if below, if under than aliasing occurs and different signals start to look the same
- folding
	Sampling $f_{max} < f_s < 2f_{max}$, then we undersample, but we receive a negative frequency. Which is opposite to the one that we actually wanted to find, therefore we can switch to the other side by adding $\pi$ to flip the signal.
- finding periodicity in between different signals
	take the GDC
- finding $T_0$ for periodic signals
	1/frequency found
- general form of a causal filter $y[n]=\sum\limits_{k=0}^{M}b_{k}x[n-k]=b_{0}x[n]+b_{1}x[n-1]+...+b_{m}x[n-M]$
	$b_k$ is vector of scaling factors applied to the values
	**order $M$** — determines how many values are considered (summed over)
	**length** $L$ — the number of non-zero coefficients in $b_k$, usually $L = M+1$ (as k starts from 0, so it is actually equal to how many numbers we sum)
- checking if a system is causal, time-invariant and linear
	causal → only depends on past values
	time-invariant → If the input is delayed by $n_0$ results in the output being delayed by $n_0$, (delay = changing all $n$ to $n - n_0$).
	linear → Linear combination of inputs will result in the same linear combination of outputs.
- First order difference filters
	$y[n]=x[n]-x[n-1]$
- second order difference filters
- averager filters
- How to compute the frequency response of a composite signal?
    Find the frequency response to the components depending on their frequency and multiply them separately.
- padding for fast Fourier
- calculating frequency responses
	1. find the frequency
	2. find the frequency response & put in the frequency to obtain $H(e^{j\hat{\omega}})$ 
	3. multiply $y[n]$ with the $H(e^{j\hat{\omega}})$
### Important formulas:
- euler's inverse formula
