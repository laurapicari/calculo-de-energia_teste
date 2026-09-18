# Fontes e premissas — US Base de equipamentos fotovoltaicos

## Critério da US

A US solicita três datasets com, no mínimo, 10 módulos, 8 inversores e 6 baterias, usando produtos reais, preços e especificações rastreáveis, com unidades numéricas padronizadas. fileciteturn0file0L6-L11

## Fornecedor

Os preços foram registrados a partir de páginas/catalogação da **NeoSolar**, fornecedor que comercializa equipamentos no Brasil. A data de coleta gravada nos CSVs é **18/09/2026**.

## Módulos

O dataset `modulos.csv` contém 10 registros. As especificações técnicas usadas incluem potência, Voc, Isc, Vmp, Imp e eficiência. As fontes de produto consultadas incluem páginas NeoSolar para Sunova, ZNSHINE, OSDA, Leapton, Ronma, ReneSola, Luxen e catálogo NeoSolar. Exemplos diretamente verificáveis: Sunova 460 W informa 460 W, Vmp 34,95 V, Imp 13,17 A, Voc 41,85 V, Isc 13,59 A e eficiência 21,30%; Sunova 550 W informa 550 W, Vmp 40,83 V, Imp 13,48 A, Voc 49,60 V, Isc 14,04 A e eficiência 21,30%; ZNSHINE 585 W informa 585 W, Vmp 43 V, Imp 13,61 A, Voc 51,6 V, Isc 14,36 A e eficiência 23,42%; Luxen 710 W informa 710 W, Vmp 40,62 V, Imp 17,48 A, Voc 48,73 V, Isc 18,49 A e eficiência 22,86%.

## Inversores

O dataset `inversores.csv` contém 8 registros e usa os campos mínimos solicitados. Foram priorizados inversores híbridos ou carregadores com dados de entrada FV identificáveis. Exemplos: Deye SUN5K SG04/SG03/SG01, Deye SUN5K US, Deye SUN8K EU, Must PV29-5048HP e Luxpower SNA PRO-EU 6K.

## Baterias

O dataset `baterias.csv` contém 6 registros. Inclui ZTROON, EPEVER, UNIPOWER e Moura. Para baterias LFP ZTROON de 48 V, as páginas/datasheets consultados informam 80% DoD e 6000 ciclos; para Moura 12MS234, a página do fornecedor informa 12 V, 220 Ah C20 e aproximadamente 1800 ciclos a 20% de descarga.

## Observação sobre preços

Os valores registrados representam o preço exibido/catalogado na coleta e **não devem ser tratados como preço fixo**. A US exige preço rastreável, não uma garantia de permanência do preço.

## Compatibilidade no sistema

O código foi atualizado para usar os nomes dos campos da US. A verificação FV considera potência máxima do inversor, tensão máxima de entrada, faixa MPPT, corrente máxima de entrada e quantidade de MPPT, além de estimar uma quantidade de módulos em série compatível com a faixa de MPPT.

## Limitações

O programa continua sendo um pré-dimensionamento acadêmico. A validação executiva deve considerar projeto de strings, temperatura, tensão de circuito aberto em condição de baixa temperatura, corrente de curto-circuito, proteções, cabos, estrutura, sombreamento, normas e requisitos da distribuidora.
