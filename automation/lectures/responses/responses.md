# RESPONSES

## Stability
A dynamim system with an output that converges to a value can be called stable. Viceversa, a system with an an output that diverges even without a divergent input is called instable.
Another definition used is the BIBO definition. BIBO means "Bounded Input Bounded Output". If we have a dynamic system SISO (Single Input Single Output) this is a stable BIBO system if starting from null initial conditions and with a litated input so that |u(t)|<=N< infinity for t>= t0 the output will be limitated so that |y(t)| <= M< infinity for t>=t0. For linear stationary system things are easier becuase of a theorem: 

th: a linear stationary SISO is BIBO stable if the impulsive response is absolutly summable:
integral(|h(t)|d(t))< infinity  (calculated from 0 to infinity).
another way to see this theorem is via the Laplace transform. if laplace(h(t)) has a negative abscissa, so the poles of the transform has the real part negative than we have the condition satisfied.

TH: a linear stationary system SISO is BIBO stable if and only if all the roots of the transfer function are negative or, if they are on the immaginary axis, has molteplicity of 1.

So for a linear stationary system, with NULL intial conditions, moved from the equilibrium with an input or a disturb limitated on time can cause three result:

- limitated response: |y(t)| <= M;
- convergent to 0: lim->infinity f(t) = 0;
- divergent response, doesn't exist and M.

Condition to each of these response:
- roots of transfer function with negative real part or null with multiplicity of 1;
- all roots of transfer function with negative real part;
- atleast one roots with positive real part.

when we have roots on the imaginary axis and mutiplicity of 1 we speak about limit of stability.
So stability is a intrinsic property of the system, not influenced by the input or initial conditions.

## Frequently considered response
y(t) = w(t) convolution u(t) = antilaplace(W(s)U(s)). If W(s) is a fraction and U(s) is too, Y(s) will depend on the roots of the system and the roots of the input. We analyse only the case that are useful to our porpuse so:
- impulsive response when u(t) is an impulse;
- indexical response when u(t) is a step function (we can obtain this integrating the impulsive response);
- ramp response, we can calculate that integrating the indexical response, or integrating two times the impulsive response.

The first one is used to see all and only the modes of the system. in Laplace the behavior of the system is entairly described by the transfer function, in time domain the system behavior is descibed by the impulsive response.

## System of the first order
system that can be represented as linear differential equation with costant coefficient of the first order, in laplace the most general rapresentation is this:
W(s) = 1/(1+stao), tao is the time costant.
this equation has just a pole s=-1/t.
if the numarator is A (a value), this will modify just the breadth.
the impulsive response will be:
y(t) = antilaplace(W(s)*1) = antilaplace(1/(1+stao))=1/tao *e^-t/tao
if tao > 0 than the function will converges to 0. The smaller tao will be the most rapidly the function will converges to 0. 
indexical response: y(t) = antilaplace(W(s)1/s)=antilaplce(1/(s(1+stao)) = antilaplace(1/s - tao/(1+stao)) = 1 - e^(-t/tao).
if tao>0 the indexical response will converges to 1, is stable and the response will never overshoot the bound. The greater tao is the faster will come closer to the convergence.
one important parameter is the settling-in time so the time when the response will differ from regime value of 5%. when tao is 1 this time is 3tao.

## Syestem of the second order
same shy for this.
W(s) = 1/((s^2/wn^2) + (2zita/wn)s + 1) = wn^2/(s^2 + 2zitaWns + wn^2)

zita is called damping coefficient whil wn will be called natural pulsation.

W(s) = R/(s-p) + R* /(s-p*) = (R+R*)(s-sigma)/(s^2 2sigmas + sigma^2 + w^2).

wn = sqrt(sigma^2 + w^2) = |p1| = |p2|
zita = -sigma/sqrt(sigma^2 + w^2) = cos\p1 = cos\p2.
the zita definition is ok only is sigma < 0.

if zita = 0 we have two pure complex poles.
if 0 < zita < 1 we have two  coniugate complex poles.
if zita > 1 we have two  real solution distinct so we can analize that as the sum of two different first order case.
if zita<0 we have two poles complex and coniugate with positive real part so the damping is improper.

Impulsive response:

y(t)=antilaplace(wn^2/(s^2 + 2zitaWns + wn^2)) = wn/(sqrt(1-zita^2)) * e^(-zitawnt) * sin(wn * sqrt(1-zita^2) * t).

indexical response:

y(t)=antilaplace(wn^2/((s^2 + 2zitaWns + wn^2)*s)) = 1 - 1/(sqrt(1-zita^2)) * e^(-zitawnt) * sin(wn * sqrt(1-zita^2) * t + arcos(zita))

the response is an oscillation that can be damped if zita>0 or not is zita<0.
the smaller is zita the grater are the oscillation, the grater is zita the smaller are the oscillation, with zita over 1 there are no oscillation.
the grater is the natural pulsation the faster we will reach the regime value.

we can consider different value:
- Max overshoot, the highest value during the oscillation;
- half-value time, time to reach 50% of the regime value;
- rise time tr1, time to pass from 10% to 90% of the regime value;
- rise time tr2, trace the line tangent to half-value time and see when the line meet the x-axis, then do the difference between tr1, and that point;
- assesement time, time to remain in a difference with regime of 5%;
- overshoot time.