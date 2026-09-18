# Evidências de cálculo — dois cenários

## Dados comuns do teste

- Consumo médio de referência: **500 kWh/mês**
- Atendimento solicitado: **100%**
- HSP: **5,00 h/dia**
- Dias considerados: **30**
- Fator global de desempenho: **80%**
- Módulo: **Canadian Solar CS6W-550MS — 550 Wp**
- Inversor: **Growatt SPH 6000TL3-BH-UP — 6.000 W**

### Memória de cálculo

**Energia mensal pretendida**

`E_FV = C_m × f`

`E_FV = 500 × 1,00 = 500 kWh/mês`

**Potência FV calculada**

`P_FV = E_FV / (HSP × D × η)`

`P_FV = 500 / (5 × 30 × 0,80) = 4,17 kWp`

**Quantidade de módulos**

`N = teto(4,17 × 1000 / 550)`

`N = 8 módulos`

**Potência efetivamente instalada**

`P_instalada = 8 × 550 / 1000 = 4,40 kWp`

**Geração mensal estimada**

`Geração = 4,40 × 5 × 30 × 0,80 = 528 kWh/mês`

---

## Cenário A — sem baterias

- Módulos: 8 × R$ 1.350,00 = **R$ 10.800,00**
- Inversor híbrido: 1 × R$ 5.900,00 = **R$ 5.900,00**
- Baterias: **R$ 0,00**
- Demais custos: **R$ 0,00**
- **Total estimado: R$ 16.700,00**
- Geração estimada: **528 kWh/mês**
- Potência instalada: **4,40 kWp**

> Mesmo sem armazenamento, o exercício pode usar o inversor híbrido do dataset; a bateria permanece opcional e o custo é zero.

---

## Cenário B — com baterias

### Premissa adicional

- Autonomia desejada: **12 horas**
- Bateria: Growatt ARK 2.5H-A1
- Capacidade nominal por módulo: **2,56 kWh**
- DoD: **90%**
- Eficiência de bateria adotada: **95%**
- Mínimo de módulos adotado no dataset para o sistema HV: **3 módulos**

### Memória de cálculo

**Consumo diário**

`E_d = 500 / 30 = 16,67 kWh/dia`

**Energia para 12 horas**

`E_autonomia = 16,67 × (12/24) = 8,33 kWh`

**Capacidade nominal necessária**

`C_bat = 8,33 / (0,90 × 0,95) = 9,74 kWh`

**Capacidade útil de cada módulo**

`C_útil = 2,56 × 0,90 = 2,304 kWh`

**Quantidade**

`N_bat = teto(9,74 / 2,304) = 5 módulos`

**Capacidade instalada**

`5 × 2,56 = 12,80 kWh`

**Capacidade útil instalada**

`12,80 × 0,90 = 11,52 kWh`

**Tensão nominal do banco**

`5 × 51,2 = 256 V`

A faixa operacional aproximada do banco de 5 módulos é **236–284 V**, compatível com a faixa de bateria adotada para o inversor híbrido no dataset.

### Orçamento

- Módulos: **R$ 10.800,00**
- Inversor: **R$ 5.900,00**
- Baterias: 5 × R$ 22.000,00 = **R$ 110.000,00**
- Demais custos: **R$ 0,00**
- **Total estimado: R$ 126.700,00**
- Geração estimada: **528 kWh/mês**
- Potência instalada: **4,40 kWp**
- Armazenamento nominal: **12,80 kWh**
- Armazenamento útil: **11,52 kWh**

## Observação

Os valores de preço são referências coletadas em fornecedor brasileiro na data registrada nos datasets e podem mudar conforme disponibilidade e condições comerciais.

Os cenários são pré-dimensionamentos acadêmicos e não substituem projeto elétrico executivo, estudo de sombreamento, definição de strings, proteções, estrutura, aterramento e demais verificações de uma instalação real.
