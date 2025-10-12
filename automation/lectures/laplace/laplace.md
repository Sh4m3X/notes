# LAPLACE TRANFORMATION

## Definition
let f(t) be a function with t into the set of real numbers, aplying laplace means solve the following integral:

<img src="images/form1.jpg" alt="Form 1" style="display:inline-block; margin-right:10px;">

Where s = σ + jw is a complex number and with f(t) = 0 only if t<0. 
It take care of 0- to infinity because the previous part is completly described by the status of at time 0.
Our input must be considered only after t=0 and equal to zero until then.
To deal with Laplace transform we need to know how to use complex number.

## Some simple exemple
Let f(t) = e^p*t the function that must be integrated in the previous integral is e^((p-s) * t), the result will be:

1/p-s * [e^(p-s)*t](from 0- to infinity).

Now if we suppose that RE[s] > RE[p] = σ* (convergent ascix), for t that goes to infinity all tend to 0, and for t equal to 0 all tend to 1/(s-p), it converges.
Notice that as denominator there is a polynom of first grade that has root with a negative real part, this is bond to the fact that the starting signal  converges to  0 while going on.

A particular case of the previous one is the case where p = jw, the result then will change in 1/(s-jw).

Another useful case is the Heavside unary step function, this function is 1 from 0 to infinity and 0 before, so if plugged in Laplace transformation it will be an integral of:

e^-st 

so the result will be -1/s * e^-st (fro t = o- to infinity) that will return 1/s.

For sin and cosine we can use the euler notation:

laplace(sin(wt)) = laplace( (e^jwt - e^-jwt)/2j ) = w/(s^2 + w^2)

laplace(cos(wt)) = laplace( (e^jwt + e^-jwt)/2 ) = s/(s^2 + w^2)

notice in this case that the real part of roots that are +-jw is zero, in fact this signal don't converges.

## Properties
Linearity:
laplace(c1* f(t) + c2* g(t)) = c1 * laplace(f(t)) + c2 * laplace(g(t))

Coniugation:
F(s*) = F*(s)

Initial Value theorem:
if exist lim t->0+ f(t)
then lim t->0+ f(t) = lim s-> infinity sF(s)
this can be used also only for function which laplace transformation has the ascix of covergence less than zero.

Final Value theorem:
Analogous for the previous one:
if exist lim t->infinity f(t)
then lim t->infinity f(t) = lim s-> 0- sF(s)

Multiplication by exponential:
laplace(e^at *f(t)) = F(s-a)
this is also known as frequency translation when a = jw

Time translation:
in this case we premultiply f(t) by a step function, avoiding to a portion of the transformation different from 0 to enter in the integral.
laplace(δ-1(t-a)f(t-a)) = e^-as * F(s).

Convolution:
g(t) = f1(t)*f2(t) (convolution)
so g(t) is the integral of f1(t-tao)f2(tao)dtao
laplace(g(t))=laplace(f1(t))*laplace(f2(t)) multiplication
so  G(t) = F1(t)*F2(t)

Derivation:
laplace(f'(t)) = sF(s) - f(0-)
laplace(f''(t)) = s^2 F(s) - sf(0-) -f'(t)

Integration:
laplace(integral(f(t))) = F(s)/s

## Transformation of impulse
let's use this definition of Dirac's impulse:

δ0(x) = lim k-> infinity sqrt(k/PI)*e^(-k(x^2))

now let's say the integral(δ0*f(t))=lim k-> infinity integral(sqrt(k/PI) *e^(-k(x^2)) * f(x))
this can be written as a convolution, but in our case the input of the convolution is δ0 which means that the result of the convolution will be f(x) or h(t), so the function itself. This is why it's called impulsive response.

laplace(δ0) = 1

## Polinomyal transformation

let's call δ-k an object that is 0 for t<0 and t^(k-1)/(k-1)! for t>= 0 with k that goes from 1 to infinity.
notice that (t^k/k!)' = t^(k-1)/(k-1)!
using the integral property we can say that:
laplace((t^k)/k!) = laplace(integral(t^(k-1)/(k-1)!)) = laplace(t^(k-1)/(k-1)!) / s

the result of this is that: 
laplace(δ0(t)) = 1 impulse
laplace(δ-1(t)) = 1/s step
laplace(δ-2(t)) = 1/s^2 ramp
laplace(δ-3(t)) = 1/s^3 parabolic ramp
laplace(δ-k(t)) = 1/s^k 
and laplace(t^k) = k!/s^(k+1)

laplace(t^(k-1)* e^pt /(k-1)!) = 1/(s-p)^k


