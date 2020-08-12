## MATLAB tools for a general TiRe-LII error model

This constitutes a software package distributed in
association with [Sipkens et al. (2017)][1], which evaluates
a general error model for time-resolved laser-induced
incandescence (TiRe-LII) signals.  

### Description and instructions

This software is an implementation of the general error model
described in the associated work, which simulates signals according
to the described error model (sufficient for generating Figure 1) and
demonstrates a fitting procedure to infer the error model parameters
from the produced signals.

This software package was developed for use with MATLAB 2016a running
on Windows. Users can execute the main script immediately, provided
all attached files are located in the same directory and that
directory is included in the MATLAB path. One must then enter
`main_simulate_C` in the MATLAB command line.

The code will display the source error model parameters chosen to
generate the data, as well as parameters fit to the signals generated
using the given error model. The code will also output two figures:
(i) a plot showing a sample signal, expected mean signal, and
single-shot expected signal with time (corresponding to Figure 1 in
the associated paper) and (ii) a plot show the average verses the
variance of the associated signals and the corresponding error
model fit to the data.

Error model parameters can be modified by editing the assignment of
tau, theta, and gamma in the `main_simulate_C.m` script.

### Components

This software distribution includes the following files:

*README.md* -		This file.

*main_simulate_C.m* - 	Primary script which loads signals, calls
			function to simulate signals, and performs
			fitting procedure on the data.

*simulate_noise.m* -  	Takes error model parameters and generates
			multiple realizations of signals

*J.mat* - 		Matlab data for a sample expected mean TiRe-LII signal
			generated for C-N2 using the Michelsen
			model from [Michelsen et al. (2007)][mich].

----------------------------------------------------------------------

#### Contact information

The primary author of the code is Timothy A. Sipkens, who can be
emailed at [tsipkens@uwaterloo.ca](mailto:tsipkens@uwaterloo.ca).
Alternatively, one can contact Kyle J. Daun at
[kjdaun@uwaterloo.ca](mailto:kjdaun@uwaterloo.ca) who supported code
development.

#### How to cite

Users of this work should cite, 

[T. A. Sipkens, P. J. Hadwin, S. J. Grauer, and K. J. Daun, “General error model for analysis of laser-induced incandescence signals,” Applied Optics, 56(30), 8436-8445 (2017).][1], 

and can consider citing this repository, if this code is used directly. 

#### Size

9.98 KB



[1]: https://www.osapublishing.org/ao/abstract.cfm?uri=ao-56-30-8436

[mich]: https://link.springer.com/article/10.1007/s00340-007-2619-5

