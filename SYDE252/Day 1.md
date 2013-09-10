## Signal Classifications

### Periodic or Aperiodic
* Signal $f(t)$ is periodic if there exists a positive constant to satisfy $$f(t+To) = f(t) \forall t$$
  * Example: Sine wave => periodic
  * dc bias => aperiodic
* If this is not possible the signal is *aperiodic*
* Smallest $To$ is also called the *period* of $f(t)$
* A periodic signal remains unchanged when time shifts integer multiples of the period

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

* First term is even component $f_{e}(t)$, second term is odd component $f_{o}(t)$

* Even $f$ x odd $f$ = odd $f$
* Odd $f$ x odd $f$ = even $f$
* Even $f$ x even $f$ = even $f$

TODO: Include graphics for this
