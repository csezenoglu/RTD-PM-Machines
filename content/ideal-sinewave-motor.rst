********************
Ideal Sinewave Motor
********************

Torque
======

Torque production in magnetic machines can be investigated by the interaction of the magnet flux and the stator ampere-conductor distribution. 

.. rubric:: Stator conductor

In the ideal machine, stator conductors are distributed sinusoidal coductor-density around the stator circumference as shown in :numref:`ideal-sinewave-brushless-motor`. In any angle :math:`d\theta` the number of conductor is 

.. math::

    \frac{N_s}{2} \sin{p \theta} d \theta

.. note::

    "The sine-distributed winding is a hypothetical case with an infinite number of slots per pole per phase, the number of conductors per slot being modulated sinusoidally to produce a sine-distributed airgap m.m.f." T.J.E. Miller, 1989

.. figure:: ../img/ideal-sinewave-brushless-motor.png
    :align: center
    :scale: 100 %
    :name: ideal-sinewave-brushless-motor

    : Ideal Sinewave Brushless Motor.

.. rubric:: Ampere conductors

In angle :math:`d\theta` the ampere-conductors flowing in the positive direction are

.. math::

    i \frac{N_s}{2} \sin{p \theta} d \theta

.. rubric:: Magnet Flux distribution

The rotor magnet flux distribution is centered on its north pole d-axis and displaced by the positive :math:`\alpha` from the axis of the stator winding:

.. math::

    B(\theta) = B_{peak} \cos(p\theta - \alpha)

.. rubric:: The Force

The force on the elementary group of ampere-conductors is in the circumferential direction and is 

.. math::

    F = B_{peak} l i \frac{N_s}{2} \sin p \theta \cos(p\theta - \alpha) d \theta

.. rubric:: The Torque

This force produces a pair of :math:`2 F r_1` torque on the stator and equal amounts and opposite couple on the rotor. The total electromagnetic torque on the rotor is the integral of the elementary contributions over the whole airgap peripery: over p pole-pairs

.. math::

    \begin{align}
    T & = -p \int_0^{\pi/p} 2 F r_1 d \theta \\
    & = -\frac{\pi r_1 B_{peak} l i N_s}{2} \sin \alpha
    \end{align}

.. Note:: 

    Maximum positive torque is obtained with :math:`\alpha = -\pi/2` that is, with the rotor north d-axis lagging 90 electrical degrees behind the axis of the stator ampere-conductor distribution :cite:`miller:1989`. ``*``

.. rubric:: Three Phase Winding

Three phase windings whose axes are 120 electrical degrees apart, the rotating ampere-conductor distribution can be derived as ``*``

.. math::

    \frac{3}{2} I \sqrt 2 \frac{N_S}{2} \sin(p\theta-\omega t)

The rotating magnet flux distribution is

.. math::

    B(\theta) = B_{peak} \cos(p\theta - \omega t - \alpha)

The torque is

.. math::

    T = \frac{3}{2} I \sqrt 2 \frac{\pi r_1 l B_{peak} N_s}{2} \sin \beta

where :math:`\beta = -\alpha`. The angle :math:`\beta` is called torque angle, and is positive for motoring :cite:`miller:1989`.

.. Note:: 

    Although the armature-reaction mmf modifies the airgap flux-density, it does not figure in the torque expression unless it significantly affects the saturation level of the magnetic circuit :cite:`miller:1989`. ``*``

EMF
===

.. note:: 

    So the "flux rule" that the emf in a circuit is equal to the rate of change of the magnetic flux through the circuit applies whether the flux changes because the field changes or because the circuit moves (or both) ...

    Yet in our explanation of the rule we have used two completely distinct laws for the two cases :math:`– v × B` for "circuit moves" and :math:`∇ × E = −∂_tB` for "field changes".

    We know of no other place in physics where such a simple and accurate general principle requires for its real understanding an analysis in terms of two different phenomena.

    Richard P. Feynman, The Feynman Lectures on Physics

Emf equation can be derived two different approach:

#The emf equation of the sinewave motor can be derived by considering the emf induced in the elementary group of conductors. Then, rms phase emf is :cite:`miller:1989`

.. math::

    E_{ph} = \frac{\pi}{2\sqrt{2}}\frac{B_{peak}l\omega r_1 N_s}{p}

and line-line emf is :math:`\sqrt{3}E_{ph}`. 

#The emf equation can also be derived from Faraday's law. This alternative method is included here because it is the basis of the phasor diagram and provides the means for calculating the inductive volt drop due to armature reaction. Faraday's law is more rigorous than the BLV formulation, but it is useful to show that for E both methods give the same result. :cite:`miller:1989`

#By Faraday's law, the instantaneous e.m.f. induced in the stationary phase winding of Fig. 5.1 is given by :cite:`miller:1989`

.. math::

    e = - \frac{d\Psi}{dt}

#On open-circuit there is no current in the coil, and all the flux is due to the magnet. The flux through the elementary coil is :cite:`miller:1989`

.. math::

    \phi = \frac{B_{peak}Dl}{p} \sin{(p\theta)}\cos{(\omega t + \alpha)}

#The flux-linkage of the elementary coil is :cite:`miller:1989`

.. math::

    d\Psi = \phi [\frac{N_s}{2} \sin{p \theta} d \theta]

#The total flux-linkage of the winding is :cite:`miller:1989`

.. math::

    \Psi = \frac{B_{peak}lr_1N_s\pi}{2p} \cos{(\omega t + \alpha)}

#By Faraday's law the instantaneous phase e.m.f. is :cite:`miller:1989`

.. math::

    e = - \frac{d\Psi}{dt} = \omega \frac{B_{peak}lr_1N_s\pi}{2p} \sin{(\omega t + \alpha)}

#The r.m.s. phase e.mf. is :cite:`miller:1989`

.. math::

    E_{ph} = \frac{\omega}{\sqrt{2}} \frac{B_{peak}lr_1N_s\pi}{2p}

Inductance of Phase Winding
===========================

Self-inductance is the actual airgap inductance and assumed that the rotor stationary and unmagnetized, other phases are open-circuited, and leakage inductance is negligible. The self-inductance of the phase winding is obtained from the flux-linkage per ampere :cite:`miller:1989`. 

.. math::

    L_s = \frac{\Psi_a}{i}

Total flux-linkage generated by armature current (subscript 'a') :math:`\Psi_a` is

.. math::

    \Psi_a = \frac{\pi}{4} N_s \Phi_a

Fundamental armature reaction flux per pole :math:`\Phi_a` can be calculated by integrating the flux-density around the periphery of the airgap.

.. math::

    \Phi_a = \frac{B_{peak} D l}{p}

In order to determine magnetic flux density around airgap :math:`B=\mu H` can be used. Total mmf, :math:`F = H l`, is equal to the winding current mmf :math:`i`. Therefore, current distribution of the phase is

.. math::

    F_g = H_g g'' = \frac{N_s i}{2p} \cos{p\theta}

Then,

.. math::

    B(\theta) = \mu_0 H_g = \frac{\mu_0 N_s i}{2pg''}\cos{p\theta} = B_{peak}\cos{p\theta}

Finally, self-inductance is obtained 

.. math::

    L_s = \frac{\pi \mu_0 N_s^2 lr_1}{4p^2g''}

Synchronous Reactance
=====================

#Rotating flux wave in a three-phase motor, established by armature reaction, generates voltages in all three phases. In each phase the voltage is proportional to :math:`I` and is therefore regarded as the voltage drop :math:`X_s I` across a fictitious reactance, the 'synchronous reactance', :math:`X_s`. By substituting the peak flux-density into the expression derived earlier for emf, and dividing by :math:`I`, we get

.. math::

    X_s = \frac{3\pi\mu_0N_s^2lr_1\omega}{8p^2g''}

#This expression applies to an ideal two-pole sine-distributed three-phase winding with Ns turns in series per phase, and it neglects the leakage inductance of the slots and end-turns. To obtain a practical formula for a real winding, we must first find an effective value for the sine-distributed turns. This is done by means of Fourier analysis and winding factors :cite:`miller:1989`.

Sinewave Motor with Practical Windings
======================================

:cite:`miller:1989`

Phasor Diagrams
===============

:cite:`miller:1989`

Sinawave Motor: Circle Diagram and Torque/Speed Characteristic
==============================================================

:cite:`miller:1989`

