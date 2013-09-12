## What is a Signal?
* Any kind of physical variable subject to variations.
* Has independent and dependant variables.
* 1D: Music, Audio (time)
* 2D: Image (x, y)
* 3D: Video (x, y, t) (image + time)

## What is a System?
A process for transforming the input signal x(t) into an output signal.

## Signals as Functions
1. Continuous functions of real independent variables. 
  
  Eg. y = f(x) y = f(x1, x2)
2. Real valued functions of discrete variables (output only defined for certain values)
3. Discreate functions of discrete variables (output functions can only have certain variables)

## Signal Classifications

### Time Classifications

* **Continuous time**: signal is specified for every real value of independent variable
* **Discrete time**: signal is specified for only discrete values of the independent variable

### Signal Types
* **Analogue signal**: Amplitude(output, dep. variable) can only take values in a countinous range 
* **Digital signal**: Can only take values in a finite # of values (quantized). For example 1 or 0 (binary).

### Periodic or Aperiodic
* Signal $f(t)$ is periodic if there exists a positive constant to satisfy $$f(t+To) = f(t) \forall t$$
* If this is not possible the signal is *aperiodic*
* Smallest $To$ is also called the *period* of $f(t)$
* A periodic signal remains unchanged when time shifts integer multiples of the period
* Examples
  * A sine wave is *periodic*
  * DC bias is *aperiodic*

### Causal vs Non-causal signals
*Causal* signals are zero for all negative time (space)
$$f(t) = 0, t < 0$$
*Anticausal* signals are zero for all positive time (space)
$$f(t) = 0, t ≥ 0$$
*Non-causal* signals have non-zero values in entire domain of $t$

### Even or Odd Signals
Even signal is any signal where $f$ satisfies:
$$f(t) = f(-t)$$
Odd signal is a signal where $f$ satisfies:
$$f(t) = -(f(-t))$$
Any signal can be decomposed into an even or odd component
$$f(t) = f_{e}(t) + f_{0}(t)$$
$$f(t) = \frac 1 2 (f(t) + f(-t)) + \frac 1 2 (f(t) - f(-t))$$

![](https://raw.github.com/vtsatskin/CourseNotes/f7e86133d860e0384ac96b2cbadf2e399ef44029/SYDE252/images/even-odd-decomp.png)

* First term is even component $f_e(t)$, second term is odd component $f_o(t)$
* Even $f$ x odd $f$ = odd $f$
* Odd $f$ x odd $f$ = even $f$
* Even $f$ x even $f$ = even $f$

### Finite vs Infinite Length Signals
* Sin wave is an example of an Infinite signal
* Real signals are always finite

### Size of the Signal
* Size = largness or strength.
* By Energy: area under the curve of the signal.

## Energy & Power
Signal energy: $$E_f = \int_{-\infty}^{\infty} f^2(t) dt = \int_{-\infty}^{\infty} |f(t)|^2 dt $$
Power signal: is the time average (mean) of the squared amplitutde signal. 
$$P_f = \lim_{T \to +\infty} \frac 1 T \int_{-T/2}^{T/2} f^2(t) dt $$

Signal to Noise Ratio (SNR)
$$20log_{10}(\sqrt{\frac {P_\text{signal}} {P_\text{noise}}})$$

* A signal w/ finite energy is an **energy signal**
  * Amplittude **must** go to 0 as $t \to \infty$
* A signal w/ finite energy & different from zero power is a power signal
  * Amplittude must go to 0 as $t \to \infty$

### Power signal 
* The mean of an entity averaged over an infinite interval exists if either the entity is periodic or it has some statistical regularity
* Power signal has infinite energy & an energy signal has zero power.
* There exists signals that are neither energy nor power signals (e.g. ramp function)

* All practical signals have finite energy & thus are energy signals.
* Impossible to have infinite duration signal.

### Questions
* Are all energy signals also power signals? **NO**
* Are all power signals also energy signals? **NO**
* Are all signals either energy or power signals? **NO**

## Useful Signal Operations

### Shifting
* $f(t + T)$: Left shift
* $f(t - T)$: Right shift

### Time Scaling
* $f(\alpha t)$: Compression
* $f(\frac t \alpha)$: Expansion/dilation

### Time Inversion
* $f(-t)$: Inverts time

## Useful Signals

### Unit step $f^n$
$$ u(t) = 1, \text{if } t ≥ 0 $$
$$ u(t) = 0, \text{if } t < 0 $$

### Ramp $f^n$
$$ r(t, t_0) = 0, \text{if } t < 0 $$
$$ r(t, t_0) = 0, \text{if } 0 ≤ t ≤ t_0 $$
$$ r(t, t_0) = 1, \text{if } t > t_0 $$

### Unit Impulse $f^n$
$$\delta(t) = 0, t ≠ 0$$
$$\int_{-\infty}^{\infty} \delta(t) dt = 1$$

**Multiplication of a function by an impulse**

$$\phi(t) \delta(t) = \phi(0)\delta(t)$$
Essentially sampling one point of $\phi(t)$.

**Sampling property**
$$\int_{-\infty}^{\infty} \phi(t) \delta(t) dt
=\int_{-\infty}^{\infty} \phi(0) \delta(t) dt
=\phi(0)  \int_{-\infty}^{\infty} \delta(t) dt
=\phi(0)$$

$$\int_{-\infty}^{\infty} \phi(t) \delta(t -T) dt =\phi(T)$$

Unit step is the itegral of the unit impulse
$$\frac {du(t)} {dt} = \delta(t)$$

## Continuous Time Complex
$$f(t) = Ae^{jwt}$$

### Euler's relations
Note: j = complex number
$$Ae^{jwt} = Acost(wt) + j(Asin(wt))$$
$$cos(wt) = \frac {e^{jwt} + e^{-(jwt)}} {2} $$
$$sin(wt) = \frac {e^{jwt} - e^{-(jwt)}} {2j} $$
$$e^{jwt} = cost(wt) + jsin(wt)$$
* Discrete complex exponential
$$f[n] = Be^{snT}$$
$$= Be^{jwnT}$$
$$k=nT$$