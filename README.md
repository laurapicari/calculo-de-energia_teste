# calculo-de-energia_teste# Sistema de Dimensionamento Energético Residencial — Sprint Fotovoltaica

## O que foi implementado

- Continuidade do cadastro de imóvel e histórico de consumo.
- Uso da média mensal registrada como consumo de referência.
- Percentual configurável de atendimento.
- HSP/recurso solar por dataset e opção de entrada manual.
- Cálculo da energia FV mensal.
- Cálculo da potência FV necessária.
- Dataset de módulos fotovoltaicos.
- Cálculo da quantidade e potência efetivamente instalada.
- Dataset de inversores.
- Filtros básicos de potência, corrente e MPPT.
- Opção sem bateria.
- Opção com bateria e autonomia em horas.
- Dataset de baterias.
- Cálculo da capacidade nominal e capacidade instalada.
- Verificação básica da tensão do banco de baterias.
- Orçamento de módulos + inversor + baterias + demais custos.
- Memória de cálculo e observações acadêmicas.
- Documentação da Sprint, Tasks, dependências e fontes.

## Cenário de teste sugerido

Cadastre um imóvel em São Paulo e registre, por exemplo:

- Janeiro: 500 kWh
- Fevereiro: 520 kWh
- Março: 480 kWh

Depois execute a opção 8.

Teste:
1. 100% de atendimento, sem bateria.
2. 100% de atendimento, com bateria e 12 horas de autonomia.

## Importante

Os preços dos datasets são valores didáticos para composição do orçamento da atividade. Não são cotações de mercado.

O resultado é pré-dimensionamento acadêmico. Em uma implantação real devem ser analisados, entre outros fatores, área disponível, orientação/inclinação, sombreamento, strings, limites elétricos do inversor, proteções, aterramento, estrutura, normas e requisitos da distribuidora.
