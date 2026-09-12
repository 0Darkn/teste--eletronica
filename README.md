README.mdPara dimensionar e calcular uma boClaro. Vou estruturar em Markdown, com as fórmulas e um exemplo numérico. Há uma distinção importante: uma bobina de 220 V, 60 Hz e 2500 W não permite determinar a indutância apenas com esses três valores; é necessário conhecer, por exemplo, o número de espiras, secção do núcleo, comprimento do circuito magnético e densidade de fluxo. Para 2500 W, também precisamos saber se os 2500 W são potência ativa, aparente ou a potência nominal da carga.

Bobina de cobre com núcleo de ferro — 220 V / 60 Hz / 2500 W

1. Dados

Consideremos inicialmente:

Tensão RMS:       V = 220 V
Frequência:       f = 60 Hz
Potência:         P = 2500 W
Material:         cobre + núcleo de ferro

A frequência angular é:

\[
\omega = 2\pi f
\]

Portanto:

\[
\omega = 2\pi \times 60
\]

\[
\boxed{\omega \approx 377\ rad/s}
\]


---

2. Corrente para 2500 W

Se considerarmos uma carga puramente resistiva, com fator de potência:

\[
\cos(\varphi)=1
\]

então:

\[
P=V I
\]

Logo:

\[
I=\frac{P}{V}
\]

\[
I=\frac{2500}{220}
\]

\[
\boxed{I\approx11,36\ A}
\]

Portanto, 11,36 A é a corrente correspondente a 2500 W a 220 V para fator de potência 1.


---

3. Bobina em corrente alternada — AC

Uma bobina ideal apresenta uma reatância indutiva:

\[
X_L=\omega L
\]

ou:

\[
\boxed{X_L=2\pi fL}
\]

onde:

$X_L$ = reatância indutiva em Ω

$f$ = frequência em Hz

$L$ = indutância em H

$\omega$ = frequência angular em rad/s


A corrente é:

\[
I=\frac{V}{X_L}
\]

Substituindo:

\[
I=\frac{V}{2\pi fL}
\]

Assim podemos determinar a indutância:

\[
\boxed{L=\frac{V}{2\pi fI}}
\]


---

4. Exemplo: determinar L

Se, apenas para efeito de cálculo, quisermos que a bobina limite a corrente a 11,36 A a 220 V / 60 Hz:

\[
L=\frac{220}{2\pi\times60\times11,36}
\]

\[
\boxed{L\approx0,0515\ H}
\]

ou:

\[
\boxed{L\approx51,5\ mH}
\]

Atenção: este valor não significa que uma bobina real de 2500 W deva ter 51,5 mH. É apenas o resultado matemático de impor 11,36 A numa indutância ideal.


---

5. Autoindução

A lei fundamental da autoindução é:

\[
\boxed{v_L(t)=L\frac{di(t)}{dt}}
\]

Isto significa que uma variação da corrente produz uma tensão na própria bobina.

A energia armazenada no campo magnético é:

\[
\boxed{E=\frac{1}{2}LI^2}
\]

Para:

\[
L=0,0515\ H
\]

e:

\[
I=11,36\ A
\]

temos:

\[
E=\frac{1}{2}\times0,0515\times11,36^2
\]

\[
\boxed{E\approx3,32\ J}
\]


---

6. Bobina ligada a DC

Em corrente contínua (DC), a frequência é:

\[
f=0
\]

Consequentemente:

\[
X_L=2\pi fL
\]

fica:

\[
\boxed{X_L=0}
\]

para o estado estacionário de uma bobina ideal.

Isto é muito importante:

> Uma bobina não funciona em DC da mesma forma que em AC.



No instante em que ligamos a tensão DC, a bobina inicialmente se opõe à variação da corrente.

A equação é:

\[
V=L\frac{di}{dt}
\]

portanto:

\[
\boxed{\frac{di}{dt}=\frac{V}{L}}
\]

Para uma bobina ideal de 51,5 mH ligada diretamente a 220 V DC:

\[
\frac{di}{dt}=\frac{220}{0,0515}
\]

\[
\boxed{\frac{di}{dt}\approx4272\ A/s}
\]

Ou seja, aproximadamente:

\[
\boxed{4,27\ A/ms}
\]

Uma bobina real não pode ser ligada diretamente a 220 V DC sem considerar a resistência do fio, aquecimento, saturação do núcleo e corrente máxima.


---

7. Bobina real — resistência do cobre

Uma bobina real possui resistência elétrica.

A resistência do fio de cobre pode ser calculada por:

\[
\boxed{R=\rho\frac{\ell}{A}}
\]

onde:

$R$ = resistência em Ω

$\rho$ = resistividade do cobre

$\ell$ = comprimento do fio em m

$A$ = área da secção do fio em m²


Para cobre a aproximadamente 20 °C:

\[
\rho\approx1,724\times10^{-8}\ \Omega m
\]

A resistência provoca perdas:

\[
\boxed{P_{Cu}=I^2R}
\]

Também podemos escrever:

\[
\boxed{P_{Cu}=VI}
\]

quando estamos considerando apenas a componente resistiva.


---

8. Modelo elétrico da bobina real

Uma bobina real pode ser representada aproximadamente por:

R
  ───/\/\/\/───LLLL───
       cobre    L

A impedância é:

\[
\boxed{Z=R+jX_L}
\]

com:

\[
X_L=2\pi fL
\]

O módulo da impedância é:

\[
\boxed{|Z|=\sqrt{R^2+X_L^2}}
\]

E a corrente:

\[
\boxed{I=\frac{V}{|Z|}}
\]


---

9. Fator de potência

Numa bobina real:

\[
\boxed{\cos\varphi=\frac{R}{|Z|}}
\]

A potência aparente é:

\[
\boxed{S=VI}
\]

A potência ativa é:

\[
\boxed{P=VI\cos\varphi}
\]

E a potência reativa indutiva:

\[
\boxed{Q=VI\sin\varphi}
\]

Também:

\[
\boxed{Q=I^2X_L}
\]

e:

\[
\boxed{P=I^2R}
\]


---

10. Cálculo correto para 2500 W

Se os 2500 W forem realmente potência ativa:

\[
P=2500\ W
\]

não podemos simplesmente usar:

\[
I=\frac{2500}{220}
\]

se a carga for uma bobina com fator de potência diferente de 1.

Devemos usar:

\[
\boxed{P=VI\cos\varphi}
\]

portanto:

\[
\boxed{I=\frac{P}{V\cos\varphi}}
\]

Por exemplo, se:

\[
\cos\varphi=0,8
\]

então:

\[
I=\frac{2500}{220\times0,8}
\]

\[
\boxed{I\approx14,20\ A}
\]


---

11. Cálculo da indutância através da corrente

Conhecendo a corrente e a resistência da bobina:

\[
Z=\frac{V}{I}
\]

e:

\[
Z^2=R^2+X_L^2
\]

portanto:

\[
\boxed{X_L=\sqrt{\left(\frac VI\right)^2-R^2}}
\]

Como:

\[
X_L=2\pi fL
\]

temos:

\[
\boxed{
L=
\frac{
\sqrt{\left(\frac VI\right)^2-R^2}
}{
2\pi f
}
}
\]

Esta é uma das fórmulas mais úteis para determinar a indutância de uma bobina real em AC.


---

12. Cálculo da indutância através do núcleo de ferro

Para uma bobina com núcleo magnético, uma aproximação básica é:

\[
\boxed{L=\frac{\mu N^2 A}{l}}
\]

onde:

$L$ = indutância em H

$\mu$ = permeabilidade magnética do núcleo

$N$ = número de espiras

$A$ = área da secção do núcleo em m²

$l$ = comprimento médio do circuito magnético em m


A permeabilidade é:

\[
\boxed{\mu=\mu_0\mu_r}
\]

onde:

\[
\mu_0=4\pi\times10^{-7}\ H/m
\]

e $\mu_r$ é a permeabilidade relativa do material.

No ferro real, $\mu_r$ não é constante: depende do material, da frequência e principalmente da densidade de fluxo. Por isso, a fórmula acima é uma aproximação.


---

13. Relação entre tensão, espiras, frequência e fluxo

Para uma bobina alimentada por AC senoidal:

\[
\boxed{V_{RMS}=4,44fN A B_{max}}
\]

Logo:

\[
\boxed{
N=\frac{V_{RMS}}
{4,44fAB_{max}}
}
\]

Esta fórmula é fundamental para dimensionar uma bobina ou enrolamento com núcleo de ferro.

Para:

\[
V=220V
\]

e:

\[
f=60Hz
\]

fica:

\[
\boxed{
N=\frac{220}
{4,44\times60\times A\times B_{max}}
}
\]

Mas ainda precisamos saber:

área do núcleo $A$

densidade máxima de fluxo $B_{max}$


Sem essas informações não é possível calcular corretamente o número de espiras.


---

14. Autoindução — resumo das principais fórmulas

Lei da autoindução

\[
\boxed{v=L\frac{di}{dt}}
\]

Indutância

\[
\boxed{L=\frac{v}{di/dt}}
\]

Reatância indutiva

\[
\boxed{X_L=2\pi fL}
\]

Corrente AC

\[
\boxed{I=\frac{V}{X_L}}
\]

Energia magnética

\[
\boxed{E=\frac12LI^2}
\]

Indutância aproximada do núcleo

\[
\boxed{L=\frac{\mu N^2A}{l}}
\]

Tensão RMS de enrolamento

\[
\boxed{V=4,44fNAB_{max}}
\]

Resistência do cobre

\[
\boxed{R=\rho\frac{\ell}{A}}
\]

Perdas no cobre

\[
\boxed{P_{Cu}=I^2R}
\]

Impedância

\[
\boxed{Z=R+j2\pi fL}
\]

Módulo da impedância

\[
\boxed{|Z|=\sqrt{R^2+(2\pi fL)^2}}
\]


---

⚠️ Nota de segurança

220 V e 2500 W são valores perigosos, e uma bobina de 2,5 kW pode trabalhar com correntes elevadas, aquecer bastante e armazenar energia magnética. Além disso, um núcleo de ferro pode saturar, fazendo a corrente aumentar rapidamente. O dimensionamento real deve considerar secção do fio, temperatura, isolamento, núcleo, entreferro, perdas magnéticas, corrente de magnetização e proteção elétrica.

Se quiseres fazer o dimensionamento completo da bobina de 220 V / 60 Hz / 2500 W, preciso de escolher valores para secção do núcleo, tipo de ferro, densidade de fluxo, comprimento magnético e diâmetro do fio. A partir daí podemos calcular número de espiras, diâmetro do fio, comprimento de cobre, resistência, indutância, corrente, perdas e aquecimento, tanto para AC como para DC.bina ligada a uma fonte de 220 V com 1500 W de potência, é fundamental separar o comportamento do circuito em Corrente Contínua (DC) e Corrente Alternada (AC).
Em corrente contínua não existe reatância indutiva: a autoindução (L) não limita a corrente em regime permanente, dependendo exclusivamente da resistência do cobre (R). Em corrente alternada, a indutância gera uma oposição à passagem da corrente chamada reatância indutiva (X_L).
1. Fórmulas Fundamentais
Autoindução (Indutância L)
A autoindução depende da geometria do núcleo e do enrolamento:
 * N: Número de espiras (voltas do fio)
 * \mu_0: Permeabilidade magnética do vácuo (4\pi \times 10^{-7} \text{ H/m})
 * \mu_r: Permeabilidade relativa do ferro (varia tipicamente entre 1000 e 5000)
 * A: Área da secção transversal do núcleo (\text{m}^2)
 * l: Comprimento médio do caminho magnético (\text{m})
Circuito em DC (Corrente Contínua)
Em regime permanente DC, L age como um curto-circuito. A potência é puramente dissipada por efeito Joule na resistência elétrica do fio de cobre (R):
Circuito em AC (Corrente Alternada - 50 Hz / 60 Hz)
Em AC, a impedância total (Z) combina a resistência (R) e a reatância indutiva (X_L):
 * f: Frequência da rede (\text{Hz})
 * \cos(\theta): Fator de potência (\frac{R}{Z})
2. Cálculos Práticos (Para V = 220\text{ V} e P = 1500\text{ W})
Caso A: Bobina projetada para consumir 1500 W em DC
 * Resistência do cobre necessária:
   
 * Corrente contínua:
   
 * Autoindução em DC:
   A autoindução L não limita a corrente contínua no tempo contínuo. Ela define apenas a constante de tempo de energização (\tau = \frac{L}{R}). O valor de L é determinado puramente pela geometria do núcleo magnético (N, A, l, \mu_r), e não pela potência nominal dissipada.
Caso B: Bobina projetada para consumir 1500 W em AC (f = 50\text{ Hz})
Assumindo que a bobina possui uma resistência própria do fio de R = 5\ \Omega para não desperdiçar toda a energia apenas em calor:
 * Impedância necessária para potências ativas:
   Para dissipar 1500\text{ W} na resistência de 5\ \Omega:
   
 * Impedância Total (Z):
   
 * Reatância Indutiva (X_L):
   
 * Autoindução em AC (L):
   
3. Efeito da Saturação do Núcleo de Ferro
O núcleo de ferro magnético aumenta dramaticamente o valor de L devido à permeabilidade relativa (\mu_r). No entanto, sob correntes elevadas, o ferro atinge a saturação magnética (ponto onde a densidade de fluxo B não aumenta mais com o campo H).
Quando o núcleo satura, \mu_r despenca para um valor próximo ao do ar (\mu_r \approx 1), fazendo a autoindução L cair bruscamente e a corrente pico subir de forma perigosa.

