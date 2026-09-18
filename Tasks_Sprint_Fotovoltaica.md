# Tasks e Dependências

| ID | Task | Dependência | Evidência |
|---|---|---|---|
| T39 | Recuperar consumo médio do imóvel | PB03 | código |
| T40 | Validar percentual de atendimento | — | código/teste |
| T41 | Calcular energia FV mensal | T39/T40 | memória de cálculo |
| T42 | Calcular potência FV | T41 | memória de cálculo |
| T44 | Criar dataset de módulos | — | `paineis.csv` |
| T46 | Calcular quantidade de módulos | T42/T44 | saída do sistema |
| T48 | Criar dataset de inversores | — | `inversores.csv` |
| T49 | Validar potência/corrente/MPPT | T46/T48 | saída do sistema |
| T52 | Criar dataset de baterias | — | `baterias.csv` |
| T53 | Calcular consumo diário/autonomia | T39 | saída do sistema |
| T54 | Calcular capacidade nominal | T53/T52 | saída do sistema |
| T56 | Validar tensão do banco | T54/T49 | saída do sistema |
| T57 | Executar cenários sem/com bateria | T56 | documentação |
| T58 | Compor orçamento | T46/T49/T56 | saída do sistema |
| T61 | Documentar fontes/premissas | todas | `README.md` |
