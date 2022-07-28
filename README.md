CLASS for the Mirror Twin Higgs model: class_twin
======================================
askldjf
This code (class_twin) can compute the evolution of the Universe for 
the Mirror Twin Higgs (MTH) model, i.e. when there exists a copy of 
the SM in the Universe. It is based on v2.9 of the CLASS code 
(http://class-code.net), and all the compilation and other rules of original CLASS apply 
here as well. I would like to take this opportunity to thank the authors 
of the CLASS code for producing and maintaining this amazing code.

There are three additional input parameters, in addition to those of the <img src="https://render.githubusercontent.com/render/math?math=\Lambda\rm{CDM}"> model, that are required to calculate the evolution of the Universe
for the MTH model. These MTH specific parameters are:

1. r_all_twin: ratio of amount of twin baryons to CDM (range: [0, 1})

2. Delta_N_twin: contribution of twin radiation to relativistic degrees of freedom of the Universe (range: [0.001, 1])

3. ratio_vev_twin: Vacuum expectation value (vev) of the twin sector as compared to that of the SM (range: [1, 15]). For instance: ratio_vev_twin = 3 implies vev of the twin sector is three times the vev of the SM.

In addition, use the following inputs for the MTH model in .ini file:<br />
nindex_idm_dr =  2<br />
alpha_idm_dr =  0.9, 1

By default, class_twin assumes that there is no twin or mirror 
sector and thus, works just like the original CLASS code. To
invoke the MTH model, make sure that all the three parameters
mentioned above are greater than 0. The easiest way to track the 
changes made in the code is to search for "#TWIN".

Note that if the twin sector is turned on, the input value of omega_cdm 
corresponds to the total dark matter, i.e. cold dark matter + twin sector. 

More details on this code can be found in the following paper:
https://arxiv.org/abs/2110.04317
