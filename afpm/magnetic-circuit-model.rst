.. 1995 Design of slotless torus generators with reduced voltage regulation

Magnetic Circuit Model
======================

.. warning:: bu kısmın son hali tezde mevcut. AFPM-machines-v1.docx dosyasından güncellenecek.

The analysis of systems with one or more closed magnetic flux path loops can be done with a magnetic circuit. An example of a magnetic circuit model of a two rotor and a coreless stator afpm machine is shown in :numref:`afpm-magnetic-circuit-model`.

.. figure:: ../img/afpm-magnetic-circuit-model.png
    :align: center
    :scale: 80 %
    :name: afpm-magnetic-circuit-model

    : Magnetic circuit model of a two rotor and a coreless stator afpm machine.

For accurate analysis with the magnetic circuit model, the model of each element should be obtained in detail. Sadeghierad et al. investigated magnetic circuit model elements of a high-speed AFPM generator :cite:`sadeghierad:2008leakage`, :cite:`sadeghierad:2009detail`. Zheng et al. investigated a one rotor one stator AFPM machine with using magnetic circuit model. Then a simplified model was obtained that ignores the back-iron reluctances :cite:`zheng:2005analysis`. 

Zheng:

Flux of permanent magnets and useful flux is calculated by

.. math::

    \phi_m=\phi_r\frac{P_g+4P_{ml}}{P_g+P_m+4P_{ml}} \\
    \phi_u=\phi_r\frac{P_g}{P_g+P_m+4P_{ml}}

Magnetic flux density of the air-gap, the stator back iron and the rotor back iron is given respectively.

.. math::

    B_g=\frac{\phi_u}{A_g}=\frac{B_rP_g}{P_g+P_m+4P_{ml}}\left(\frac{A_m}{A_g}\right) \\
    B_{si}=\frac{\phi_u}{{2A}_{si}}=\frac{B_rP_g}{P_g+P_m+4P_{ml}}\left(\frac{A_m}{{2A}_{si}}\right) \\
    B_{ri}=\frac{\phi_m}{{2A}_{ri}}=\frac{B_r\left(P_g+4P_{ml}\right)}{P_g+P_m+4P_{ml}}\left(\frac{A_m}{{2A}_{ri}}\right)

Burada manyetik direnç eşitlikleri şöyle verilmiştir [2]:

.. math::

    R_m=\frac{L_{axm}}{\mu_rA_m} \\
    R_g=\frac{L_g}{A_g}

Rotor ve stator arka çeliğinin manyetik dirençleri ihmal edilirse basitleştirilmiş model elde edilir. Böylece manyetik akı ve kullanılabilir akı şöyle olur [2]:

Buradan yola çıkarak tork ve elektromotor kuvvetin maksimum değeri şöyle bulunabilir [2][3]:

.. math::

    T=N_mk_dk_pB_gN_{tpp}i\left(R_o^2-R_i^2\right) \\
    e_{max}=N_mk_dk_pB_gN_{tpp}\left(R_o^2-R_i^2\right)\omega_m

Burada;

:math:`N_m`	kutup sayısı

:math:`k_d`	sargı dağılım katsayısı

:math:`k_p`	sargı adım katsayısı

:math:`N_{tpp}`	kutup başına, faz başına tur sayısı

:math:`\omega_m`	rotor açısal hızı

:math:`R`	yarıçap



Permanent Magnet Model
----------------------

Permanent magnet model consists of a reluctance (magnetic resistance) and a magneto motive force (mmf) :cite:`sadeghierad:2009detail`.

.. figure:: ../img/pm-magnetic-circuit-model.png
    :align: center
    :scale: 100 %
    :name: pm-magnetic-circuit-model

    : Permanent Magnet Model (a) Thevenin Equivalent Model, (b) Norton Equivalent Model.

Formulations for Thevenin Equivalent Model

.. math::

    \begin{align}
        R_m &= \frac{l_m}{\mu_0\mu_{rm}A_m} \\
        F_m &= \phi_rR_m \\
        \phi_r &= {B_rA}_m
    \end{align}

Formulations for Norton Equivalent Model

.. math::

    \begin{align}
        \phi_m &= B_m A_m \\
        &= B_r A_m+\mu_0\mu_{rm}H_m A_m \\
        &=\phi_r+\frac{F_m}{R_m}
    \end{align}

Leakage Flux Model
------------------

In general, leakage flux is existed two different fashion in permanent magnet machines. Self-leakage flux is existed between permanent magnet and back iron. The other one is seen between two adjacent permanent magnets. In :numref:`pm-leakage-flux-model`, 1a and 1b are self-leakage flux paths of magnet and 2 is the leakage flux path between two magnets.

.. figure:: ../img/pm-leakage-flux-model.png
    :align: center
    :scale: 100 %
    :name: pm-leakage-flux-model

    : PM Flux Leakage Model.

Self-leakage flux and leakage flux between two PMs are shown :math:`R_{L1}` and :math:`R_{L2}` respectively in magnetic circuit model.

.. figure:: ../img/pm-leakage-flux-circuit-model.png
    :align: center
    :scale: 100 %
    :name: pm-leakage-flux-circuit-model

    : PM Flux Leakage Circuit Model.


Self-leakage flux equations :cite:`wu:1995design`:

.. math::

    \begin{align}
        R_{L1}&=R_{LA}||R_{LB} \\
        R_{LA} &= \frac{p}{\mu_0 k_{pp} \left( \left(D_i - l_m\right) \ln{ (\frac{l_m+2g}{l_m}) } +2g \right)} \\
        R_{LB} &= \frac{9p/2}{\mu_0 k_{pp} \left( \left(3D_o + 2l_m\right) \ln{ (\frac{l_m+3g}{l_m}) } -6g \right)}
    \end{align}

Leakage flux between two PMs is :cite:`sadeghierad:2009detail`:

.. math::

    R_{L2} = \frac{2\pi(1-k_{pp})}{\mu_0 l_m p \ln{(D_o/D_i)} }
    

Rotor Back-Iron Model
---------------------

An important part of the machine is rotor back-iron. For instance, machines with two-rotor AFPM machine has back-iron at the end of the PMs. The formula :math:`B(H)` used in a FEM software to model the back steel is defined as follows :cite:`sadeghierad:2008leakage`: 

.. math::

    B\left(H\right)=\mu_0H+\frac{2J_S}{\pi}\arctan{\left(\frac{\pi(\mu_r-1)\mu_0H}{2J_S}\right)}

Coefficient :math:`J_S` is determined from B-H graphics (:numref:`back-iron-model`) below:

.. figure:: ../img/back-iron-model.png
    :align: center
    :scale: 100 %
    :name: back-iron-model

    : Back-Iron Model.

Nonlinear reluctance of back-iron can be calculated by

.. math::

    R_{iron}=\frac{F_i}{\phi_i}=\frac{H_il_i}{B_iA_i}

Lombard et al., presented another method for calculating the back iron model. In this method the iron permeability is used to calculate the reluctance of iron. The magnetic permeability of the back-iron is initially calculated as iterative to provide the flux density equation of the back-iron and the B-H curve. The magnetic permeability of the back-iron is used to calculate the reluctance :cite:`lombard:1999analysis`. 

.. math::

    B_g(peak)=\left(\frac{4R_m}{4R_m+4R_g+R_{iron}}\right)B_r

Air Gap Model
-------------

In electrical machines, the flux generally forms a path between two high magnetic permeable materials. Since the permeability of the air is low, fringing effect is seen on the edges of the material. To calculate the reluctance of the air gap, this fringing effect should be taken into account depending on the desired precision. Three different approaches can be used to model the flux path in the air gap as shown in :numref:`air-gap-model-1`. 

.. figure:: ../img/air-gap-model-1.png
    :align: center
    :scale: 100 %
    :name: air-gap-model-1

    : Air gap model.

The simplest model is that completely ignores the effect of the fringing as in the :numref:`air-gap-model-1` a. Here is the reluctance:

.. math::

    R_{g1} = \frac{g}{\mu_0 A}

When the air gap dimensions that the :math:`g/A` ratio between the two materials is smaller, then, a refine model (:numref:`air-gap-model-1` b) exists when the length g is added to the periphery A giving a larger area :math:`A'` :cite:`hanselman:2006`.

.. math::

    R_{g2} = \frac{g}{\mu_0 A'}

Finally, it is assumed that the fringe flux follows a circular arc from the edge of a block, travels along a straight line through the space, followed by a circular arc to the other block as shown in :numref:`air-gap-model-2`. This circular-arc straight-line modeling can compute the flux flow with an analytical expression that is more realistic than any of the first two models :cite:`hanselman:2006`.

.. figure:: ../img/air-gap-model-2.png
    :align: center
    :scale: 100 %
    :name: air-gap-model-2

    : Air gap model in detail.

.. math::

    P_f=\int_{0}^{X}{\frac{\mu_0l}{g+\pi x}dx}=\frac{\mu_0l}{\pi}\ln{\left(1+\frac{\pi X}{g}\right)}

.. math::

    R_{g3} = \frac{\pi}{\mu_0 l \ln{(1+\frac{\pi X}{g})} }

The unknown variable :math:`X` is the distance of the fringe effect from the edges and is not dependent on a variable. Generally, a few times of the air gap is selected. The total air gap reluctance change very little if it is increased for :math:`10g`.

.. --------------------------------------------------------------------
.. --------------------------------------------------------------------
.. --------------------------------------------------------------------

.. rubric:: Tezde yazılmış son güncel hal: 20190802

The analysis of systems with one or more closed magnetic flux path loops can be done with a magnetic circuit. An example of a magnetic circuit model of a two rotor and a coreless stator AFPM machine is shown in Fig. 3.1.

.. figure:: ../img/afpm-magnetic-circuit-model.png
    :align: center
    :scale: 80 %
    :name: afpm-magnetic-circuit-model

    : Magnetic circuit model of a two rotor and a coreless stator afpm machine.

Fig. 3.1 : Magnetic circuit model of a two rotor and a coreless stator afpm machine.

For accurate analysis with the magnetic circuit model, the model of each element should be obtained in detail. Sadeghierad et al. investigated magnetic circuit model elements of a high-speed AFPM generator [sadeghierad:2008], [sadeghierad:2009]. Zheng et al. investigated a one rotor one stator AFPM machine with using magnetic circuit model. Then a simplified model was obtained that ignores the back-iron reluctances [zheng:2005].
