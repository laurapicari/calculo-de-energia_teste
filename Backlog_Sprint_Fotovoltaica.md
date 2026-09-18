# Product Backlog — Sprint de Evolução Fotovoltaica

## PB10 — Pré-dimensionamento da geração FV
**User Story:** Como usuário, quero informar o percentual do meu consumo que desejo atender para que o sistema calcule a energia mensal necessária e a potência FV estimada.

**Critérios de aceite**
1. Usar o consumo médio mensal já registrado no imóvel.
2. Permitir percentual entre 1% e 100%.
3. Calcular `E_FV = C_m × f`.
4. Calcular `P_FV = E_FV / (HSP × D × η)`.
5. Exibir unidades e premissas.

**Tasks**
- T39 — Recuperar o consumo médio do imóvel.
- T40 — Implementar entrada e validação do percentual.
- T41 — Implementar cálculo da energia mensal desejada.
- T42 — Implementar cálculo da potência FV.
- T43 — Exibir memória de cálculo.

**Dependências:** PB02/PB03 da versão anterior.

---

## PB11 — Dataset e seleção de módulos
**User Story:** Como usuário, quero escolher módulos de um dataset para que a potência instalada seja formada por equipamentos reais de referência.

**Critérios de aceite**
1. Ler `paineis.csv`.
2. Exibir fabricante, modelo, potência, eficiência e preço.
3. Calcular `N = teto(P_FV × 1000 / P_módulo)`.
4. Exibir potência efetivamente instalada.

**Tasks**
- T44 — Criar schema do dataset.
- T45 — Implementar carregamento CSV.
- T46 — Implementar cálculo de quantidade.
- T47 — Exibir custo dos módulos.

**Dependências:** PB10.

---

## PB12 — Seleção e compatibilidade do inversor
**User Story:** Como usuário, quero que o sistema filtre inversores compatíveis para evitar combinações tecnicamente inválidas.

**Critérios de aceite**
1. Considerar potência FV máxima suportada.
2. Considerar corrente máxima por MPPT.
3. Considerar quantidade de MPPT.
4. Quando houver bateria, selecionar apenas inversores híbridos.

**Tasks**
- T48 — Criar schema de `inversores.csv`.
- T49 — Implementar filtros de compatibilidade.
- T50 — Implementar seleção do menor inversor nominal que atende a solução.
- T51 — Exibir validações técnicas.

**Dependências:** PB11.

---

## PB13 — Armazenamento opcional
**User Story:** Como usuário, quero escolher baterias e informar minha autonomia desejada para dimensionar armazenamento.

**Critérios de aceite**
1. Permitir solução sem baterias.
2. Quando solicitado, calcular `E_d = C_m/30`.
3. Calcular `E_autonomia = E_d × (A/24)`.
4. Calcular capacidade nominal considerando DoD e eficiência.
5. Selecionar quantidade de baterias do dataset.
6. Validar faixa de tensão do banco contra o inversor.

**Tasks**
- T52 — Criar `baterias.csv`.
- T53 — Implementar cálculo de autonomia.
- T54 — Implementar cálculo de capacidade nominal.
- T55 — Implementar quantidade mínima e capacidade instalada.
- T56 — Validar tensão do banco.
- T57 — Testar cenário sem bateria e com bateria.

**Dependências:** PB12.

---

## PB14 — Orçamento e proposta preliminar
**User Story:** Como usuário, quero receber um orçamento rastreável da configuração selecionada.

**Critérios de aceite**
1. Somar módulos, inversor, baterias e demais custos.
2. Mostrar baterias como R$ 0,00 quando não utilizadas.
3. Mostrar potência calculada e instalada.
4. Mostrar geração mensal estimada.
5. Apresentar observação de pré-dimensionamento acadêmico.

**Tasks**
- T58 — Implementar composição do orçamento.
- T59 — Exibir custos por categoria.
- T60 — Exibir total.
- T61 — Documentar fontes e premissas.

**Dependências:** PB11/PB12/PB13.
