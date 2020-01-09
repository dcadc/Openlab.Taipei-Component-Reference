Diode
===
Semiconductors/PN Junctions
< Semiconductors
This page may need to be reviewed for quality.
Jump to navigationJump to search
Semiconductors

Contents
1	Simple Models
2	Analysis of Diode Physics
2.1	Depletion Width
2.2	Depletion capacitance
3	References
Simple Models
These simple models are small signal approximations to how a fairly generic diode works. Zener and tunnel diodes are ignored.

At a first approximation, a diode is a device that will let current flow in one direction with zero resistance and will block current in the other direction with infinite resistance. Basically, it operates like a check valve for current.

A second approximation includes a constant voltage drop for current flow in the forward direction. The voltage drop varies with the type of diode, but is typically around 0.7 volts for fairly generic diodes and well over 1 volt for LEDs.

To get a third approximation, add a little resistance to the diode. Now things get a little more complicated. Since the v-i curve is non-linear, the resistance is not constant. However, if your signal is small and carried on a large offset, you can do a fairly accurate analysis by properly selecting the voltage drop and resistance.

Finally the fourth approximation accounts for the small leakage current that exists when the diode is reverse biased. This is typically in the range of nano-amps to a few micro-amps for most generic diodes.

If you need more accuracy than this, you will need to look at the physics that happens inside a diode.

Analysis of Diode Physics
Diodes junctions may be formed with N type and P type semi-conductor or semi-conductor and Metal junction.


as {\displaystyle \Phi }\Phi .

Depiction of Fermi level for metal and semiconductor
Depiction of the Fermi level for a metal and a semiconductor.
When the Metal and Semi-conductor come together, excess electrons diffuse from the semi-conductor to the metal until the Fermi levels are equal. As electrons diffuse from the semi-conductor to the metal, they leave behind their donor atom. This depletes the region near the interface of charge carriers and hence this region does not conduct well. Thus for charges to diffuse across this region, they require additional energy. Since the extent of the depletion of charges is some function of distance, the conduction band is bent to represent the energy required for diffusion in that region.

Depiction of femi level for metal and semiconductor
Depiction of the Fermi level for a metal and a semiconductor.
There will now exist 2 currents. Electrons diffuse from metal to semi-conductor over the barrier induced by the depletion region {\displaystyle I_{O}}{\displaystyle I_{O}}. Electrons diffuse from the semi-conductor over this barrier in the opposite direction {\displaystyle I_{F}}{\displaystyle I_{F}}. When there is no external applied voltage, there current will be equal and opposite.

Electrons will diffuse from semi-conductor to metal if they have enough energy to overcome the barrier. The energy of an electron is statistical, and is given by the Maxwell-Boltzmann distribution [1]. Thus as the temperature increases, the probability of the number of electrons occupying higher energy states increases. For low doping densities, the Maxwell-Boltzmann distribution may also be applied. However for non-zero temperature most excess electrons from the dopant will exist in the conduction band.

Maxwell-Boltzmann distribution says: given an energy W, the number of electrons with energy greater than W is given by:

{\displaystyle n_{W}=n\cdot e^{\frac {-W}{kT}}}{\displaystyle n_{W}=n\cdot e^{\frac {-W}{kT}}}

where n is the number density of electrons, k Boltzmann's constant and T the temperature.

Fermi level probability density function
Probability density function of electrons around Fermi level
The Maxwell-Boltzmann distribution does not apply to metals. The reason may be found in the referenced [1]. For small voltages one may assume {\displaystyle I_{O}}{\displaystyle I_{O}} to be constant.

{\displaystyle I_{F}=nqe^{\frac {-q\Psi }{kT}}}{\displaystyle I_{F}=nqe^{\frac {-q\Psi }{kT}}}

{\displaystyle I_{O}=I_{F}}{\displaystyle I_{O}=I_{F}} for no external potential. This equilibrium exists for a diffusion potential we will call {\displaystyle \Psi }\Psi , where {\displaystyle \Psi =\phi _{m}-\phi _{s}}{\displaystyle \Psi =\phi _{m}-\phi _{s}}. Thus the energy of an electron to cross this barrier is given by {\displaystyle q\Psi }{\displaystyle q\Psi }.

{\displaystyle I_{O}=I_{F}=nq\cdot e^{\frac {-q\Psi }{kT}}}{\displaystyle I_{O}=I_{F}=nq\cdot e^{\frac {-q\Psi }{kT}}}

{\displaystyle nq=I_{O}\cdot e^{\frac {q\Psi }{kT}}}{\displaystyle nq=I_{O}\cdot e^{\frac {q\Psi }{kT}}}

The fermi level of the n-type semi-conductor may be increased by an external potential. This will increase the number of electrons with energy to diffuse across the barrier. Thus the energy for electron to cross the barrier will become {\displaystyle q(\Psi -V)}{\displaystyle q(\Psi -V)}.

{\displaystyle I_{F}=nq\cdot e^{\frac {-q(\Psi -V)}{kT}}}{\displaystyle I_{F}=nq\cdot e^{\frac {-q(\Psi -V)}{kT}}}

{\displaystyle I_{F}=I_{O}\cdot e^{\frac {q\Psi }{kT}}\cdot e^{\frac {-q(\Psi -V)}{kT}}}{\displaystyle I_{F}=I_{O}\cdot e^{\frac {q\Psi }{kT}}\cdot e^{\frac {-q(\Psi -V)}{kT}}}

{\displaystyle I_{F}=I_{O}\cdot e^{\frac {qV}{kT}}}{\displaystyle I_{F}=I_{O}\cdot e^{\frac {qV}{kT}}}

Thus:

{\displaystyle I_{D}=I_{F}-I_{O}}{\displaystyle I_{D}=I_{F}-I_{O}}

Let:

{\displaystyle V_{T}={\frac {kT}{q}}}{\displaystyle V_{T}={\frac {kT}{q}}}

Then:

{\displaystyle I_{D}=I_{O}{\bigg (}e^{\frac {V_{D}}{V_{T}}}{\bigg )}-I_{O}}{\displaystyle I_{D}=I_{O}{\bigg (}e^{\frac {V_{D}}{V_{T}}}{\bigg )}-I_{O}}

{\displaystyle I_{D}=I_{O}{\bigg (}e^{\frac {V_{D}}{V_{T}}}-1{\bigg )}}{\displaystyle I_{D}=I_{O}{\bigg (}e^{\frac {V_{D}}{V_{T}}}-1{\bigg )}}


Depletion Width
The depletion width is given by the required amount of charge to be displaced to realize the diffusion potential. Thus if one knows the doping density and relative permittivity of the material, then one may calculate the depletion width.

Diagram of diode depletion region
Depletion region in diode junction
The depletion width is easiest realized by Poisson's Equation [1]. Assume constant doping density.

By Poisson's equation:

{\displaystyle {\frac {\partial ^{2}}{\partial x^{2}}}V(x)={\frac {\rho }{\varepsilon }}}{\displaystyle {\frac {\partial ^{2}}{\partial x^{2}}}V(x)={\frac {\rho }{\varepsilon }}}

where {\displaystyle \rho =qN_{d}}{\displaystyle \rho =qN_{d}} the charge density, {\displaystyle \varepsilon }\varepsilon the permittivity and x the distance from the junction.

{\displaystyle V={\frac {qN_{d}x^{2}}{2\varepsilon _{0}\varepsilon _{r}}}}{\displaystyle V={\frac {qN_{d}x^{2}}{2\varepsilon _{0}\varepsilon _{r}}}}

The depletion width is some function of barrier height, {\displaystyle (\Psi -V)}{\displaystyle (\Psi -V)}. Therefore solve for {\displaystyle x=W_{d}}{\displaystyle x=W_{d}}

{\displaystyle \Psi -V={\frac {qN_{d}W_{d}^{2}}{2\varepsilon _{0}\varepsilon _{r}}}}{\displaystyle \Psi -V={\frac {qN_{d}W_{d}^{2}}{2\varepsilon _{0}\varepsilon _{r}}}}

{\displaystyle W_{d}={\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}(\Psi -V)}{qN_{d}}}}}{\displaystyle W_{d}={\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}(\Psi -V)}{qN_{d}}}}}

Depletion capacitance
Capacitance is the change in charge for change in voltage over the depletion width.

Given:

{\displaystyle C={\frac {\partial Q}{\partial V}}}{\displaystyle C={\frac {\partial Q}{\partial V}}}

{\displaystyle Q=qN_{d}W_{d}YZ}{\displaystyle Q=qN_{d}W_{d}YZ}


Then:

{\displaystyle C={\frac {\partial (qN_{d}W_{d}YZ)}{\partial (\Psi -V)}}}{\displaystyle C={\frac {\partial (qN_{d}W_{d}YZ)}{\partial (\Psi -V)}}}

{\displaystyle C=qN_{d}YZ{\frac {\partial W_{d}}{\partial (\Psi -V)}}}{\displaystyle C=qN_{d}YZ{\frac {\partial W_{d}}{\partial (\Psi -V)}}}

{\displaystyle C=qN_{d}YZ\cdot {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}\cdot -{\frac {1}{2}}{\bigg (}{\frac {2\varepsilon _{0}\varepsilon _{r}(\Psi -V)}{qN_{d}}}{\bigg )}^{-{\frac {1}{2}}}}{\displaystyle C=qN_{d}YZ\cdot {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}\cdot -{\frac {1}{2}}{\bigg (}{\frac {2\varepsilon _{0}\varepsilon _{r}(\Psi -V)}{qN_{d}}}{\bigg )}^{-{\frac {1}{2}}}}

{\displaystyle C=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}}{\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}}\cdot {\sqrt {\frac {qN_{d}}{2\varepsilon _{0}\varepsilon _{r}(\Psi -V)}}}\cdot {\frac {\sqrt {\Psi }}{\sqrt {\Psi }}}}{\displaystyle C=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}}{\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}}\cdot {\sqrt {\frac {qN_{d}}{2\varepsilon _{0}\varepsilon _{r}(\Psi -V)}}}\cdot {\frac {\sqrt {\Psi }}{\sqrt {\Psi }}}}

{\displaystyle C=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}}\cdot {\frac {1}{\sqrt {\Psi }}}\cdot {\sqrt {\frac {\Psi }{\Psi -V}}}}{\displaystyle C=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}}}}\cdot {\frac {1}{\sqrt {\Psi }}}\cdot {\sqrt {\frac {\Psi }{\Psi -V}}}}

{\displaystyle C=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}\Psi }}}\cdot {\frac {1}{\sqrt {1-V/\Psi }}}}{\displaystyle C=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}\Psi }}}\cdot {\frac {1}{\sqrt {1-V/\Psi }}}}

Let:

{\displaystyle C_{0}=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}\Psi }}}}{\displaystyle C_{0}=-{\frac {1}{2}}qN_{d}YZ\cdot {\sqrt {\frac {2\varepsilon _{0}\varepsilon _{r}}{qN_{d}\Psi }}}}

Therefore:

{\displaystyle C={\frac {C_{0}}{\sqrt {1-V/\Psi }}}}{\displaystyle C={\frac {C_{0}}{\sqrt {1-V/\Psi }}}}

References
[1] John Allison. Electronic Engineering Semiconductors and devices. McGraw-Hill Book Company, Shoppenhangers Rd Maidenhead Berkshire England,1971.

Category: Book:Semiconductors

