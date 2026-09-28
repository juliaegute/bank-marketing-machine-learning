# Bank Marketing — Machine Learning

Projeto acadêmico desenvolvido na disciplina de Machine Learning da ESPM, com orientação do professor Antonio Marcos Selmini.

**Autores:** Julia Egute e Pedro Perroni.

## Objetivo:

Comparar modelos de classificação para prever a adesão de clientes a um depósito a prazo e apoiar a priorização de contatos em uma campanha de telemarketing.

## Base de dados

A base fornecida na atividade contém 41.188 registros e 21 colunas, incluindo informações dos clientes, histórico de contatos, indicadores econômicos e a variável-alvo `aderiu`.

Após a remoção de 12 linhas duplicadas, sob a hipótese de registros redundantes, foram utilizados 41.176 registros.

## Modelos e cenários

Foram avaliados três classificadores:

- k-vizinhos mais próximos (k-NN);
- Naive Bayes (GaussianNB);
- Regressão Logística.

A comparação considera dois cenários:

- **Principal:** atributos considerados disponíveis antes da ligação, conforme as hipóteses documentadas no trabalho.
- **Completo:** todos os atributos originais, com as transformações descritas no notebook, para comparação.

## Preparação e avaliação

A preparação utiliza Pipeline para imputação pela mediana, padronização dos atributos numéricos e codificação das categorias.

Foram reservados 30% dos dados para teste, com estratificação e `random_state=42`. Os hiperparâmetros de k-NN e Regressão Logística foram escolhidos por validação cruzada no treino.

A métrica principal é o F1 macro. Também são apresentadas acurácia, precisão, recall e F1 por classe, além das matrizes de confusão.

## Principal resultado

O GaussianNB apresentou o maior F1 macro médio na validação cruzada do cenário principal: **0,6585 ± 0,0059**.

No teste, alcançou F1 macro de **0,6657** e recall de **51,1%** para a classe de adesão. Entretanto, apresentou mais falsos positivos, e sua escolha não comprova maior retorno financeiro para o banco.



Foi utilizado o ChatGPT como apoio na revisão e correção do código, na preparação dos dados, na avaliação dos modelos e na interpretação dos resultados. A ferramenta também auxiliou na organização do notebook, na redação do relatório e na elaboração deste README.
