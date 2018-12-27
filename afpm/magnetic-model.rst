Magnetic Model
==============

Permanent Magnet Model
----------------------

.. rubric:: document1

Mıknatıs seçiminde şu etmenler göz önüne alınabilir [4]:

- Manyetik özellikleri (Br, Hc, BHmaks vb.)
- üksek sıcaklıklarda çalışma yeteneği (SmCo NdFeB'den daha yüksek sıcaklıklarda çalışabilmektedir.)
- Mıknatısın fiyatı (SmCo NdFeB'den daha pahalıdır.)

Sürekli mıknatıslı makinelerde birkaç ortak malzeme kullanılmaktadır. Bunların içinde Nd-Fe-B (Neodyum-demir-bor) ve SmCo (Samaryum-kobalt) mıknatıslardan söz edilebilir. Neodyum mıknatıslarda eddy akımı kayıpları daha azdır, ayrıca neodyum mıknatısın fiyat performans oranı samaryum kobalta göre iyidir [142]. Bu sebeplerden ötürü mıknatıslı makinelerde çoğunlukla neodyum mıknatıs kullanılmaktadır. Mıknatısın modeli bir manyetik direnç (reluctance) ve bir mmk (mmf: magnetomotive force)'den oluşmaktadır[1].

.. rubric:: document2

Permanent magnet model consists of a reluctance (magnetic resistance) and a magneto motive force (mmf) [Sadeghierad, M., et al., 2009].


Figure 1.1 Permanent Magnet Model (a) Thevenin Equivalent Model, (b) Norton Equivalent Model
Formulations for Thevenin Equivalent Model

.. math::

    R_m=\frac{l_m}{\mu_0\mu_{rm}A_m} \\
    F_m=\phi_rR_m \\
    \phi_r={B_rA}_m

Formulations for Norton Equivalent Model

.. math::

    \phi_m=B_mA_m=\left(B_r+\mu_0\mu_{rm}H_m\right)A_m \\
    \phi_m=\phi_r+\frac{F_m}{R_m}

.. rubric:: document3

To move the magnet operating point from its static operating point determined by the external permeance, an external magnetic field must be applied. In a motor, the static operating point lies somewhere in the second quadrant, usually at a PC of 4 or more. When motor windings are energized, the operating point dynamically varies following minor hysteresis loops about the static operating point, as shown in Fig. 2.20. These loops are thin and have a slope essentially equal to that of the demagnetization characteristic. As a result, the trajectory closely follows the straight-line demagnetization characteristic described by

Bm= Br + (XRtMfim (2.17)
 
This equation assumes that the magnet remains in a linear operating region under all operating conditions. Driving the magnet past the remanence into the first quadrant normally causes no harm, as this is in the direction of magnetization. However, if the external magnetic field opposes that developed by the magnet and drives the operating point into the third quadrant past the coercivity, it is possible to irreversibly demagnetize the magnet if a knee in the characteristic is encountered. Using (2.17), it is possible to develop a magnetic circuit model for a PM. Let the rectangular magnet shown in Fig. 2.21a be described by (2.17). Then the flux leaving the magnet is

(f>m = BmAm = BrAm + AmHm

where Am is the cross-sectional area of the magnet face in the direction of magnetization. Using (2.4), (2.5), and (2.6), this equation can be rewritten as

<f>m = <t>r + PmF„ (2.18)

where

4>r = BrA,

is a fixed flux source, and where

Pm = V<rIM)A,

L

(2.19)
(2.20)

is the permeance of the magnet. Conventionally (2.20) is called the magnet leakage permeance, although here it will simply be called the magnet permeance. Equation (2.18) implies that the magnetic circuit model for the magnet is a flux source in parallel with a permeance, as shown in Fig. 2.216. It is important to recognize that this model as sumes that the physical magnet is uniformly magnetized over its cross section and is magnetized in its preferred direction of magnetization. When the magnet shape differs from the rectangular shape shown in Fig. 2.21a, it is necessary to reevaluate its magnetic circuit model. In brushless PM motors having a radial air gap, the magnet shape may appear as an arc, as shown in Fig. 2.22. The magnetic circuit model of this shape can be found by considering it to be a radial stack of differential length magnets, each having a model as given in Fig. 2.216. During magnetization the same amount of flux magnetizes each differential length. As a result, the achieved remanence decreases linearly with increasing radius because the same flux over an increasing area gives a smaller flux density (Hendershot, 1991). Therefore, integration of these differential elements gives a magnet magnetic circuit model of the same form as Fig. 2.216 with

/ W A (221)

m ln(l + IJri)

and

<f>r = BrLdpn (2.22)

where Br is the remanence achieved at and L is the axial length of the magnet into the page. In the common case where lm « rL (2.21) can be simplified by approximating the permeance shape as rectangular with an average cross section. This approximation gives
Pm = fxRtM)Ldp + £ ) (2.23

