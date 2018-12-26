============
Introduction
============

History
-------

.. check

The axial flux machine is not a new discovery, the first working prototype was built by M. Faraday in 1831 [9]. But due to the complexity in mechanical design, difficulty to maintain a uniform airgap, and poor quality PMs, made the radial flux counterpart a more cost effective motor and has been the number one choice since its introduction in 1837 patented by inventor T. Davenport. After the invention of high quality PMs in the 1980s, the AFPM is now proven to be cost effective, and challenging its radial flux counterpart in a number of areas[3] :cite:`lomheim:2013`.

Axial vs Radial Flux Machines
-----------------------------

.. check

The difference between radial and axial flux machines lies in their names; the radial flux machine use radial directed magnetic flux established on the rotor which interacts with stator current to produce electromagnetic torque. The axial flux machine has axial directed magnetic flux which interacts with stator current to produce torque.
In an electrical machine the force is acting in the circumferential direction, which means that the current and magnetic fields are confined to the radial and axial directions which lead to the two machine types.
The advantage of the axial flux machine is the possibility to design a very compact disc shaped motor, with high torque per volume :cite:`lomheim:2013`.

.. math::
    
    T_{radial} = k D^2 L \\
    T_{axial} = k D^3

.. check

The machine torque sizing equations for a radial flux compared to axial flux is given by (2) and (3) respectively, where k is the machine constant used to compare sizing of equal designed machines, D is the diameter of rotor, and L is the length of the machine[2]. The key difference between axial flux and radial flux is that the radial flux machine can be scaled by adjusting the length of the machine, while the axial flux has an optimized machine length for a given diameter. The diameter of an axial flux machine has its mechanical limitations, where increasing the diameter results in higher torque while the contact surface to the shaft joint is constant[9]. Because of this, the scaling of an axial flux machine is done by having multiple discs when maximum diameter is reached. When the radial flux machine is scaled with length, the end coil volume remains the same, while an axial flux machine has the same amount of end coil in each inserted disc, giving the radial flux an advantage in high torque applications. It is proven that the axial flux design can be used in the high speed-high torque power ranges, and is up to four times lighter and much smaller than its radial counterpart at equal rating[7] :cite:`lomheim:2013`.

.. figure:: ../img/axial-flux-vs-radial-flux.png
    :align: center
    :scale: 100 %
    :name: axial-flux-vs-radial-flux

    : Axial vs Radial Flux Machines, The Design, Implementation, Evaluation and Results of a Race Car for the Collegiate Formula SAE Electric Competition 2016.

Axial Flux Machine Features
---------------------------

- For the analysis of axial-flux type motor, a three-dimensional finite element analysis (3-D FEA) approach was necessary. However, 3-D FEA requires large time for computation. [2006 Characteristic analysis of the slotless axial-flux type brushless DC motors using image method 188]

- Generally slotless single axial-flux type motors hardly saturated due to large and constant air-gap length so the analytical solutions can give precise result for this kind of application. [2006 Characteristic analysis of the slotless axial-flux type brushless DC motors using image method 188]

Topologies
----------

Sürekli mıknatıslı eksenel akılı makineler içinde birçok farklı topoloji bulunmakla birlikte, :numref:`afpm1` gibi sıradan bir tek rotor tek statorlu yapıda; sargılar, akının geri dönebileceği çelik bir plaka üzerine konumlanır ve sargıların üzerinde de rotora bağlı mıknatıslar bulunmaktadır. [4]

.. figure:: ../img/afpm1.png
    :align: center
    :scale: 100 %
    :name: afpm1

    : PM axial filed motor configuration