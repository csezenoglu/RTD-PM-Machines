Design
======

.. note:: makaleden : 2018 Coreless AFPM Pulsed Alternator With Low Internal Inductance 

\section{Design of AFPM Generator}
Design of coreless AFPM generator for LIL is carried out with these requirements:
\begin{itemize}
\item 
The projectile speed should be high. Therefore, the frequency of the generator should be high.
\item
In order to ensure the acceleration of the projectile in a section of the barrel, rising time of the current of the generator should be small (high $di/dt$), so inductance of the stator winding should be small.
\item
Instant power of the generator should be high because of the heavy projectile. 
\end{itemize}

First design step is to obtain required frequency of stator current of the generator. Increasing pole number is the basic method of raising frequency in electrical machines. Although it is possible in the AFPM machines, there is a limitation that is the rotor diameter is greater when the number of poles is increased. The rotor diameter does not increase much because of the mechanical constraints. When the magnet size is made smaller, three-phase stator windings cannot fit into the one pole. A novel wave winding configuration can overcome this problem. Pole number is increased with making smaller magnet size and contrary to conventional AFPM generator; one phase winding is placed between two rotors. Then, multistage design is carried out to obtain three-phase machine as seen in Fig.\ref{seperated_winding_vs_convensional_afpm_machine}.

The AFPM generator has 40 poles and four rotors. Rectangular shaped NdFeB magnets are used. Two outer rotors have surface mounted, and two inner rotors have buried magnets. The inner rotors are non-magnetic stainless steel because of minimizing the leakage flux. Due to the buried magnets, both sides of the middle rotors have the air gaps. Therefore, induced voltage of the middle stator is lower than the outer stators. Increasing thickness of the magnets at the middle rotors can help overcome this problem which is ignored in this work.

Based on all these requirements and suggested solutions, initial geometric parameters are determined and shown in TABLE \ref{initial_parameters}.

\subsection{Winding Resistance and Inductance}
Winding resistance is calculated by analytically and the resistance of a phase is 73.61 m$\Omega$. Then, every phase measured by LCR meter that are seen in TABLE \ref{resistance_inductance}.

Inductance of a coreless machine is difficult to formulate clearly \cite{2005wang_odoa:1381506}, and it is noted that coreless axial flux machines have very low inductance (below 100 $\mu$H) due to lack of iron in the stator \cite{2012de_liaf:6111544}. Furthermore, there are no published works about inductance of wave windings. Accordingly, inductance of the wave winding is determined by software. Then, inductance of every phase measured by LCR meter at 1 kHz that are seen in TABLE \ref{resistance_inductance}. 

\subsection{Induced Voltage}
The RMS value of the induced voltage by the magnets on the terminals of the stator is given by \cite{2000elhasan_mdoh:908897}
\begin{equation}
\label{induced_voltage}
E_{RMS} = 0.353 k_w p N \omega_{m} B_g (R_{o}^2 - R_{i}^2)
\end{equation}
where $k_w=0.5$ is the winding factor, $p$ is the number of pole, $N$ is number of turns per phase, $\omega$ is angular velocity, $B_g$ is magnetic flux density in the air gap and $R_o$ and $R_i$ are outer and inner radius of the effective area of rotors. Induced RMS voltage is calculated 170.34 V.  

Initial Parameters of Geometry

Magnet Dimensions & 40x10x5 mm
Number of Poles per Rotor & 40
Outer Radius of Magnets & 180 mm
Inner Radius of Magnets & 140 mm
Winding Type & Wave
Number of Turns per Phase & 10
Thickness of a Winding Layer & 0.8 mm
Thickness of a Insulation Layer & 0.1 mm
Thickness of The Stator & 10 mm

Calculation and Measurement Results of Resistance and Inductance

Resistance & PH1 & PH2 & PH3
Measured & 82.15 m$\Omega$ & 82.46 m$\Omega$ & 82.51 m$\Omega$ 
Calculated & \multicolumn{3}{}{73.61 m$\Omega$}
Inductance & PH1 & PH2 & PH3
Measured & 90.02 $\mu$H & 84.56 $\mu$H & 91.02 $\mu$H 
Calculated & \multicolumn{3}{}{90.05 $\mu$H} 

\subsection{Output Power}
Output power of the generator is calculated as \cite{2000elhasan_mdoh:908897}
\begin{equation}
\label{output_power}
P_O = 3 E_{RMS} I_P
\end{equation}
where $I_P$ is the current flowing generator windings and assumed unity power factor. The current is related to time constant of RL equivalent circuit that is $\tau=L/R$. Time constant of the proposed machine is approximately 50 $\mu$s that is proper for LIL applications. Therefore, it can be possible to achieve 500 kW peak power under a millisecond.


Yüksek Hızlı Makine Tasarımı
----------------------------


Yüksek hızlı makine tasarımındaki temel zorluklar şöyledir [Pullen et al., 1996]:

-	Yüksek hızlı makinelerde çap küçülmektedir. Hacim ve yüzey küçüldüğü için soğutma özelliği azalmaktadır. 
-	Rulmanlar, rotor dinamiği ve balans çok önemlidir.
-	Toleranslar boyut ile doğrusal değişmemektedir.
-	Yüksek hız ve akımdan ötürü fırça yapısı kullanılamamaktadır.
-	Yüksek frekans yüksek eddy akımı kayıpları ve demir kayıpları meydana getirir. Ayrıca sürücü elektroniğini zorlaştırır.
-	Yüksek hava sürtünme kayıpları oluşur.
 
Pullen, K. R., M. R. Etemad, and A. Fenocchi. "The high speed axial flux disc generator-unlocking the potential of the automotive gas turbine." (1996): 8-8.

Kutup Sayısı ve Frekans
------------------------

(Senkron üreteçler isimli dokümandan)

Senkron bir üretecin kutup sayısı dönüş hızına ve istenilen frekansa bağlıdır. Örneğin bir stator iletkeni başarılı bir şekilde rotorun N ve S kutuplarını süpürüyor. Eğer N kutbu iletkenden geçerken pozitif bir gerilim indüklüyorsa, benzer şekilde S kutbundan geçerken de negatif gerilim indüklenir. Böylece, her zaman tam bir kutup çifti iletkeni geçer ve indüklenen gerilim tam bir çevrim yapar. Aynı şekilde stator üzerindeki tüm iletkenler için bu durum geçerlidir. Buradan üreteç frekansını elde edebiliriz.

.. math::

    f=\frac{pn}{120}

Burada,

- f 	indüklenen gerilimin frekansı [Hz]
- p 	rotorun kutup sayısı
- n 	rotorun hızı [rpm]

Kutup Sayısı:
-------------

Eksenel akılı makinelerde kutup sayısının seçimi bilhassa önemlidir. Yüksek sayıda kutup sayısının seçimi şu sebeplerden ötürü düşünülebilir:

-	Makine kütlesinin büyük bir bölümü akı dönüş yolunu içerir. Bu ağırlık kutup sayısıyla ters orantılıdır.
-	Sargı sonu uzunluğunu ve boşluğunu azaltmak için çok sayıda kutup gereklidir. Bu özellikle eksenel uzunluğu kısa olan makinelerde önemlidir. 

Kutup sayısının (ve dolayısıyla elektrik frekansının) artmasıyla birlikte makine tasarımında şu etkenlere dikkat edilmesi gerekir:

-	Sabit duran demir bileşenlerin hepsinde demir kayıplarında artış olacaktır.
-	Hava aralığındaki sargılardaki eddy akımı kayıplarında artış olacaktır.
-	Verilen bir hava aralığı için mıknatıslar arası kaçak akılar artacaktır.
-	Motor sürücüsünün anahtarlama frekansı artacak ve böylece sürücü verimi azalacaktır.

Ayrıca kutup sayısındaki artış her bir kutbun ölçülerini küçültecek ve makineyi bir araya getirmek güçleşecektir [Lovatt et al., 1998]. 
 
H.C. Lovatt, V.S. Ramsden, and B.C. Mecrow, "Design of an inwheel motor for a solar-powered electric vehicle," Proc. IEE-B, vol.145, no.5, pp.402-408, 1998.

Diğer-1
-------

1	Giriş

1.1	Eksenel Akılı Makineler

1.2	Hava nüveli makine

Nüvesiz makinenin üstün yanları şöyle sıralanabilir [Lovatt et al., 1998]:

-	Nüveli yapıdaki demir kayıplarından ötürü verim %96'nın altındadır.
-	Neodyum mıknatıslar ile daha yoğun akı elde edilebilmektedir.
-	Sargı bakırları için daha fazla hacme sahiptir.
-	Yüksek frekanslı makinelerde litz teli kullanılarak eddy akımı kayıpları azaltılabilmektedir.
-	Eksenel akılı makinelerde nüvenin yapımı işi ile kıyaslandığında hava nüveli makinenin hazırlanması daha kolaydır.
-	Ağırlık azdır.
-	Birleştirme esnasında statorda kuvvet oluşmaz.
-	Termal performansı yeterlidir.

Eksenel akılı makineler sabit tork uygulamaları için mükemmel performansa sahiptir ancak nispeten düşük indüktans değerinden ötürü sabit güç uygulamaları için uygun değildir [Caricchi et al., 1996].
 
H.C. Lovatt, V.S. Ramsden, and B.C. Mecrow, "Design of an inwheel motor for a solar-powered electric vehicle," Proc. IEE-B, vol.145, no.5, pp.402-408, 1998.

Caricchi, F., F. Crescimbini, and A. Di Napoli. "Prototype of innovative wheel direct drive with water-cooled axial-flux PM motor for electric vehicle applications." Applied Power Electronics Conference and Exposition, 1996. APEC'96. Conference Proceedings 1996., Eleventh Annual. Vol. 2. IEEE, 1996.

2004 Axial flux permanent magnet disc machines A review 83
----------------------------------------------------------

A majority of variable speed applications do not require field-weakening applications. However, there exist some applications such as traction drives, washing machines and spindle drives that necessitate field-weakening operation [68], [70-72]. The means to realize field weakening in PM machines by eliminating the effects of d-axis current injection has been a great interest in machine designers and new machine structures are of great importance at this point. There exist several alternative solutions in order to eliminate this problem in conventional PM machines. In particular, advances in materials technology such as PMs and magnetic steel allow the researchers to propose new machine configurations.

Tork üretimi
------------

EASM makinelerinin ölçüleri yarıçapın fonksiyonları şeklinde olduğu için elektromanyetik tork, yarıçapların sürekli dizisi üzerinden üretilir. Çünkü radyal makinelerdeki gibi yarıçap sabit değildir. 

Eksenel akılı makinenin kutuplar arası mesafesi \tau\left(r\right) ve kutup genişliği b_p\left(r\right) yarıçap r’nin birer fonksiyonlarıdır:

.. math::

  \tau\left(r\right)=\frac{2\pi r}{2p}=\ \frac{\pi r}{p}

.. math::

  b_p\left(r\right)=\ \alpha_i\tau\left(r\right)=\ \alpha_i\frac{\pi r}{p}

Denklemlerde görülen \alpha_i ise hava aralığındaki manyetik akı yoğunluğunun ortalama değeri Bavg’nin tepe değeri Bmg’ye oranıdır: 

.. math::

  \alpha_i=\ \frac{B_{avg}}{B_{mg}}   veya   \alpha_i=\ \frac{B_{avg}}{B_{mg}}

Her iki kutup uzaklığı ve kutup genişliği yarıçapın birer fonksiyonudur, \alpha_i parametresi normal olarak yarıçaptan bağımsızdır.

Çizgi akım yoğunluğu da yarıçapın bir fonksiyonudur. Böylece çizgi akım yoğunluğunun tepe değeri:

.. math::

  A_m\left(r\right)=\ \frac{m_1\sqrt2N_1I_a}{p\tau\left(r\right)}=\frac{m_1\sqrt2N_1I_a}{\pi r}	

Diskin üzerindeki yüzeysel (tangential) kuvvet Ampere eşitliği esas alınarak hesaplanabilir:

.. math::

  dF_x=I_a\left(dr\ \times\ B_g\right)=\ A(r)(dS\ \times\ B_g)

Burada I_adr=A(r)dS, eşitlik (4.4)’den A\left(r\right)dS=\ A_m\left(r\right)/\sqrt2 , dr yarıçap elemanı, dS yüzey elemanı ve B_g de hava aralığındaki manyetik akı yoğunluğunun normal vektörüdür (disk yüzeyine dik). Bir EASM disk tip makine pratik olarak yarıçaptan bağımsız olarak B_g’yi sağlar. 

Varsayalım hava aralığındaki manyetik akı yoğunluğu B_{mg}yarıçaptan bağımsız, eşitlik (4.3)’den  dS=2\pi rdr ve B_{avg}=\ \alpha_iB_{mg}olmak üzere eşitlik (4.5) temel alınarak, elektromanyetik tork:
dT_d=rdF_x=r\left[k_{\omega1}A\left(r\right)B_{avg}dS\right]=\ 2\pi\alpha_ik_{\omega1}A(r)B_{mg}r^2dr	(4.6)

Çizgi akım yoğunluğu A(r) statorun etkin yüzeyindeki elektrik yüküdür.


