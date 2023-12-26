# Deep-K-Means
## Agrupamento Conjunto e Aprendizado de Representações

Este repositório implementa a abordagem Deep k-Means (DKM), abordando os desafios conjuntos de agrupamento e aprendizado de representações. A suposição subjacente é que representações fiéis aos dados a serem agrupados e adaptadas ao algoritmo de agrupamento podem resultar em um desempenho de agrupamento melhor, especialmente quando ambas as tarefas são realizadas simultaneamente.

## Variantes do Deep k-Means

Duas variantes são exploradas nos experimentos: Annealing (DKMa) e Pretrained (DKMp).

- **DKMa:** Utiliza uma estratégia de recuo para α sem pré-treinamento. A evolução de α segue uma sequência recursiva projetada para gastar mais iterações em valores menores, preservando uma inclinação suave.

  αₙ₊₁ = 2¹/log(ₙ)² * αₙ com mₐ = α₁ = 0.1

- **DKMp:** Inicializado pelo pré-treinamento de um autoencoder, seguido pelo agrupamento conjunto com um α constante (mₐ = Mₐ = 1000). Um α elevado resulta em atribuições de cluster rígidas.

A lógica por trás dessas escolhas é fornecer flexibilidade na adaptação de α para obter resultados aprimorados de agrupamento.

Leia mais sobre o método [aqui](https://arxiv.org/pdf/1806.10069.pdf).

