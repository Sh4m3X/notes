# INVESTMENTS

## General definition
To invest means to spend part or the totality of one's capital in order to achive a gain in short or long term. 
Projects in economy starts with an investment, so an initial cost, to have future revenue.
The future is the first element of risk for an investor. Risks in investment is that element that determines the quantity of the possible futere revenue. The higher are the risks taken the higher will be the possible revenue if all go well.

Inflation is the rate at which general prices for goods are rising. Inflation of 2% means that if i buy something for 100 today the next year i will buy it 102.
Deflation is the opposite of inflation. In general for market is better the presence of a low inflation than deflation.

Projects of investment can be:
Indipendent
Dipendent: alternative, conditional, concurrent.

## Interess and Interess rate
Let's call P the capital invested in t0 and F the income of the investment at tf.
we will call interess I = F - P
we will call rate of interess i = I/P

## simple vs compound
Let's say that we invest a certain ammount P for n years for a rate of i each year, what does this means in terms of F?

if we invest P and the rate is i, this means that each year we will have a gain of P*i, this for n year, and the last year we will receive also our initial P.
 
So F will be:
F = P + P* i* n = P(1+i*n)

This is simple interess. 

What differes in compound interess is that each year, instead of just taking the income, we decide to reinvest each ammount. What does it means in terms of math?

in t = 0 we invest P.
in t = 1 our income will be I1 = p*i --> F1 = P + P * i
in t = 2 our income will be I2 = F1 * i = (P + P * i) * i --> F2 = P(1 + i) * i + P(1+i) = (1+i)(P * i + P) = (1+i)^2 * P

in t = n our F = P*(1+i)^n and I = F - P = P ( (1+i)^n -1 )

So this means that the growth of compound interess is higher because in terms of function it is an exponential.

## Nominal rate vs Real rate
let's say that someone propose to us a annual nominal rate (TAN) r that is compound on m fraction of a year.
This means that each period of time the rate is r/m. 
now we can think out interess like a compound interest with rate i*m = r/m that is done in m period so in formulas our income will be:

F = p(i + i*m)^m = p (i+r/m)^m
I = F - P = P ((1+i*m)^m -1)

but we now that the rate of an interess can be calculated with I/P
so i* = (1+im)^m - 1
this is the value of the real rate vs the nominale rate of the TAN.

## Attualization
Attualize an Income means: "if i invest my money in n years i will have a certain Income, how can i translate that income in today's money?", how granpa says “A few, damned quick!”. 

To do that is just question of reverse the simple interess and compound interess.

There is also other way to do that, for exemple imagine to don't now what's the original capital P but you know each year you receive an ammount A.
F in this case will be the sum(A(1+i)^n+k) where k goes from 1 to n, if we juggle with this sum we can also obtain the equivalent:

F = A((1+i)^n - 1)/i
A = F*i/((1+i)^n - 1)

Now what happens if we know that the investment was compound? F = P(1+i)^n and so
P = A((1+i)^n - 1)/(i(1+i)^n)

same can be done with simple interess.

### VAN or PW
VAN(i) = sum(Fk/(1+i)^k) or VAN(i) = sum(Fk/(1+in))