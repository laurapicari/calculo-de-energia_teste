# Fontes e premissas dos datasets

## Recurso solar
- CRESESB — SunData v3.0: ferramenta de apoio ao dimensionamento fotovoltaico, com irradiação diária média mensal em kWh/m².dia e busca por coordenadas.
- Os valores de `hsp_referencia.csv` são referências acadêmicas simplificadas para permitir execução offline. Em implantação real, consultar o SunData para as coordenadas do imóvel e documentar o ponto escolhido.

## Módulos
- Canadian Solar / CSI Solar, família CS6W: fichas técnicas consultadas para potência, eficiência, Vmp, Voc, Imp e Isc.
- O dataset usa três variantes de referência da mesma família para permitir seleção por potência.
- Preços em BRL são **estimativas acadêmicas para o exercício**, não cotações comerciais atuais.

## Inversores
- Growatt SPH TL3 BH-UP: dados técnicos de potência PV máxima, tensão CC, faixa MPPT, número de MPPT, corrente por MPPT e faixa de bateria.
- O modelo SPH 6000TL3-BH-UP é híbrido e foi escolhido como referência para o cenário com armazenamento.
- Preços em BRL são **estimativas acadêmicas para o exercício**, não cotações comerciais atuais.

## Baterias
- Growatt ARK 2.5H-A1: módulo LFP de 2,56 kWh, 51,2 V e DoD de referência de 90%.
- O sistema HV considera mínimo de 3 módulos para o cenário acadêmico, de modo a entrar na faixa de tensão compatível do inversor híbrido selecionado.
- Preço em BRL é **estimativa acadêmica**, não cotação comercial.

## Premissas de cálculo
- `D = 30 dias`.
- `η` é informado pelo usuário; o valor sugerido no programa é 80%.
- Eficiência do armazenamento adotada no cálculo: 95%.
- Geração estimada mensal: `P_instalada × HSP × 30 × η`.
- A solução é um pré-dimensionamento acadêmico e não substitui projeto executivo.

