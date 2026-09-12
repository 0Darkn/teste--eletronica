README.mdPara dimensionar e calcular uma bobina ligada a uma fonte de 220 V com 1500 W de potência, é fundamental separar o comportamento do circuito em Corrente Contínua (DC) e Corrente Alternada (AC).
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

