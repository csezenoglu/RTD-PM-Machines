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

#The emf equation of the sinewave motor can be derived by considering the emf induced in the elementary group of conductors. Then, rms phase emf is

.. math::

    E_{ph} = \frac{\pi}{2\sqrt{2}}\frac{B_{peak}l\omega r_1 N_s}{p}

and line-line emf is :math:`\sqrt{3}E_{ph}`. 

#The emf equation can also be derived from Faraday's law. This alternative method is included here because it is the basis of the phasor diagram and provides the means for calculating the inductive volt drop due to armature reaction. Faraday's law is more rigorous than the BLV formulation, but it is useful to show that for E both methods give the same result.

#By Faraday's law, the instantaneous e.m.f. induced in the stationary phase winding of Fig. 5.1 is given by

.. math::

    e = - \frac{d\Phi}{dt}
