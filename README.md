# Ratio Tunnel Option Valuation

A ratio tunnel option offers the contract holder the right either long or short, at a contract maturity, a preset underlying collar. Notional principals and strikes in the collar may be different. In the system, the ratio tunnel option and the underlying collar are strictly European type. The ratio tunnel option model applies analytical close form pricing formulae for vanilla compound options.

A ratio tunnel option is defined as a European vanilla option upon a European collar. It is another special case of a general compound option. We can get a close form pricing formula for the option on collar, or the ratio tunnel option (see https://finpricing.com/lib/EqCallable.html ). Most of results presented in the report (see footnote 1) can be applied here. Therefore, in the following, we just provided some specified information which is necessary in this case.

Our test cases cover currency pairs under European and American quoting conventions, and different call-put principal ratios. Risk numbers, including spot rate Delta’s, forward point Delta’s, Gamma’s, Vega’s, and Rho’s, as well as P/L’s have also been tested.

For an underlying collar, let us define Kc and Kp be the strikes of a call and a put in the collar, respectively,
and Tclr be the maturity of the collar. Let T be the maturity of the ratio tunnel option where T < Tclr and
PN be the notional principal of the option measured in the unit of an underlyer. Now we have

 

where

 

Then the matured payoff of the ratio tunnel call option at T can be given by

 

where K is the unit strike of the ratio tunnel option. Clearly, the ratio tunnel put option can be defined by
the following matured payoff

 

Let us consider the following non-linear equation

 

The function g(¢) is strictly increasing with respect to S and with the co-domain including [0;1). Therefore,
for any K ¸ 0, there is a unique strictly positive solution of (4), which is denoted by Sclr. Further, we have

 

where

 

The solution Sclr can be obtained by using Newton-Raphson method.

Let t · T be a generic valuation time and pcClr(t; St;K; ¡) be the t-value of a ratio tunnel call per unit
notional principal. Then we have

 

The expectation in the second term on the right side of (7), denoted by I2, can be re-written as

 

The expectation in the third term on the right side of (7), denoted by I3, is given by

 


