# Apontamentos Aprendizagem e Decisões Inteligentes

Apontamentos da cadeira de ADI da Universidade do Minho 2022

# Sistemas de Aprendizagem

*Machine Learning Algorithm*

Paradigma de computação em que a característica essencial do sistema se revela pela sua capacidade de aprender de modo **autónomo** e **independente**


## Aprendizagem por Reforço *Reinforcement Learning*

Paradigma de aprendizagem que, apesar de não ter informação sobre os resultados pretendidos, permite efetuar uma avaliação sobre os resultados produzidos são bons ou maus.

O algoritmo atribui uma certa recompensa a uma determinada ação que seja mais desejada e atribui uma penalização a ações não desejadas



-  Jogos com Inteligencia Artificial
-  Aquisição de aptidões
-  Tarefas de aprendizagem
-  Decisões em tempo real

-----------
## Aprendizagem sem Supervisão *Unsupervised Learning*

Paradigma de aprendizagem em que **não são conhecidos** resultados sobre os casos, apenas os enunciados dos problemas, tornando necessário a escolha de técnicas de aprendizagem que avaliem o funcionamento interno do sistema

Não existem dados previos para comparar com os atuais


**Associação**

Quando se pretende organizar os dados em grupos coerentes (agrupar clientes que compram bebidas açucaradas)

- Visualização (Big Data)
- Compreensão de significados
- Descoberta de estruturas
- Seleção de atributos

**Segmentação** aka ***Clustering***

Quando se pretende conhecer regras que associem o comportamento demonstrado pelos dados (pessoas que compram bebidas açucaradas não compram bebidas alcoolicas)

- Segmentação de clientes
- Marketing
- Sistemas de recomendação


--------------

## Aprendizagem com supervisão *Supervised Learning*

Paradigma de aprendizagem em que os casos que se usam para aprender contêm informação acerca dos resultados pretendidos, sendo possivel estabelecer uma relação entre os valores **pretendidos** e os valores **produzidos** pelo sistema.

**Classificação**

Resultados são discretos(homem,azul,bom)

- Diagnostico
- Deteção de Fraude
- Classificação de imagem
- Fidelização de clientes

**Regressão**

Resultados são continuos(variação da temperatura, dinheiro necessário)
- Crescimento populacional
- Previsão de mercados
- Previsão meteorológica
- Esperança média de vida

--------------------
--------------

# Metodologias e Análise de Dados

## CRISP-DM

1. Estudo do negócio
2. Estudo dos Dados
3. Preparação dos Dados
4. Modelação
5. Avaliação
6. Desenvolvimento

## Data Mining

Processo de extrair conhecimento e relações complexas de grandes volumes de dados


--------------
--------------

# Preparação de Dados

Transformar um dataset de forma a que a informação neles contida esteja adequadamente exposta à ferramenta de extração de conhecimento

*Tarefas na preparação de dados*
- Discretização/Enumeração
- Limpeza
- Integração
- Transformação
- Redução

*Tipos de dados*
- Nominais

Nomes, Codigos de indetificação

- Categorias
Cor dos olhos, Sexo

- Ordinais

tipo de clasificação(mau,bom,excelente), temperatura(frio,morno,quente)

- Intervalos

É possível calcular a distãncia entre 2 valores. Grau de temperatura, dinheiro lucrado.

- Racios

Os valores podem ser utilizados para determinar um rácio significativo entre eles -> Salário , Balanço Bancário


## Discretização de dados

**Equal width binning**
Divide a game de valores em N intervalos de igual largura, resultando numa grelha unifrome

**Equal height binning**
Divide a gama de valores em N intervalos, contendo, cada um, **aproximadamente** a mesma quantidade de valores

--------
## Limpeza de Dados

**Como tratar a ausencia de dados**

- Ignorar o registo onde falta os dados
- Ignorar apenas o atributo onde falta os dados
- Preencher manualmente
- Preencher com um valor medio
- Preencher com o valor mais frequente
<h2>
DEVE SEMPRE SER EVITADA A DISTORÇÃO DE DADOS
</h2>

-------------

## Integração de Dados

Os dados que caracterizam o problema podem ter proveniencias diversas

Integração requer o **conhecimento do negocio**

## Transformação

- Alisamento(smoothing)
- Agregação
- Generalização
- Construção de Atributos
- Uniformização
- Deteção de valores atípicos

Nomiadamente outliers, valores que estão muito distantes da média 

---------
## Redução de dados

Obter uma representação reduzida do volume de dados, mas produzindo os mesmos( ou quase os mesmo ) resultados analiticos

------------

-------------

# Avaliação de Modelos

## Árvores de Decisão *Decision Tree*

Grafo hierarquizado *(arvore)* em que:

* Cada ramo representa a seleção entre um conjunto de alternativas
* Cada folha representa uma decisão


Podem ser usadas para **classificação**

* Decidir sobre se almoçar ou não
* Classificar um conjunto de imagens(carro,mota,camião)

Podem ser usadas para **regressão**
* Prever o preço do petroleo ou gás
* Estimar a temperatura para amanhã
  
------------

## Paradigmas de criação de modelos de decisão

**Top down aproach**

* O modelo é construido a partir do conhecimento de especialistas
* O todo é dividido em *partes*

**Bottom up aproach**
* Construido pela indentificação de relações entre os atributos do *dataset*
* Induzido por *generalização* dos dados

-------
## Avaliação de dados

* Dados de Treino

Conjunto de dados para ajustar o modelo

* Dados de validação

Conjunto de dados usados para fornecer uma avaliação imparcial de um ajuste do modelo, no conjunto de dados de treino

* Dados de teste

Conjunto de dados usado para fornecer uma avaliação imparcial de um modelo final ajustado ao conjunto de dados de treino

-----------
## Hold-out Validation

**Metodo de particionamento de dados**

Divide o conjunto de dados em dados de treino e dados de teste

------
## Cross validation

**Metodo de particionamento de dados**

Consite em dividir o conjunto de dados em k partes -> *k folds*

A cada iteração, o metodo utiliza k-1 partes para treino e 1 parte para teste

O processo repete-se k vezes

----------
---------

# Técnicas de Regressão

## Metodo dos minimos quadrados

## Regressão Linear Multipla

Usada para determinar o efeito de diversas variaveis independentes *x1, x2, x3...* numa variavel independente ***y***.

## Regressão Logistica

A variavel dependente é de natureza binária

A regressão logistica é uma tecnica de classificação
* Emprestimo(SIM/NAO)
* Vinho(Branco/Rose/Tinto)

------------------
---------------
# Métricas de Qualidade

Servem para analisar o desempenho do modelo

* Erro médio Absoluto
* Erro médio Quadrado
* Precisão
* F1-Score

---------------
## Matrizes de confusão

Tabela utilizada para descrever o desempenho de um modelo de classificação

-------------
## Precisão

É uma medida de exatidão, não interessa se os valores são corretos apenas se não variam muito entre si.

------------
## Accuracy

Quantidade de previsões corretas dividido pela quantidade total de observações

------------
## AUC Curve

Um modelo cuja previsões estão 100% erradas tem uma AUC de 0

Um modelo cuja previsões estão 100% certas tem uma AUC de 1

--------
--------

# Arvores de Decisão Machine Learning

## Entropia

Ganho de informação

Este métrica mede a redução esperada na entropia

O atributo com a maior redução de entropia é a melhor escolha para ser nodo-> *para reduzir a profundidade da àrvore*

O atributo que tiver o maior ganho é aquele que deve ser usado para ser o **nodo raiz** da arvore, pois apresenta o maior ganho de informação possivel

## Pros and cons

Pros
* Facilmente compreensiveis
* Podem ser convertidas para regras
* Manipulas missing values
* Configuracao simples

Cons
* Inadequadas para problemas caracterizados por muitas interacos entre os atributos
* Falta de poder expressivo 
* Não isenta a réplicas de subárvores

---------
---------

# Segmentação

Segmentação ou *Clustering* é um processo através do qual se particiona um conjunto de **dados em segmentos** ou *clusters* de menor dimensão, que agrupam conjuntos de dados similares

**Segmento**
* são similares entre si , dentro de um mesmo segmento
* são diferentes dos valores/ objetos de outros segmentos

Medidas de **similaridade**
* distância Euclidiana ou de Manhattan para atributos continuos
* coeficiente de Jacqard para atributos discretos/binários

## Exemplos de Aplicação

Marketing

* ajuda na descoberta de grupos de cliente para desenvolver estratégias de comercialização

Seguradoras
* Identificação de grupos de utentes que representam maior risco de contratação

## Metodos de Segmentação

Particionamento
* Criar várias partições e adotar um critério de avaliação

Hierarquização
* decompor hierarquicamente o conjunto de dados

## Método k-means

**Vantagens**
* Relativamente eficiiente
* Termina com ótimos locais

**Desvantagens**
* Só é possivel executar quando se consegue calcular a média
* É necessário identificar o numero de segmentos *à priori*
* Incapacidade de lidar com ruido nos dados
* Inadequado para determinar segmentos concavos


## Redes Neuronais Artificiais

Uma RNA é definida por uma estrutura interligada de unidades computacionais, designadas neurónios, com capacidade de aprendizagem

-----------------
### Neurónio

* Unidade computacional de composição da Rede Neural Artificial

* Identificado pela sua posição na rede

* Caraterizado pelo valor do estado

------------
### Axónio

* Via de comunicação entre os neurónios
* Pode ligar qualquer neurónio, incluido o próprio
* As ligações podem variar ao longo do tempo
* A informação circula em ***um só sentido***

-----------------

### Sinapses

* Ponto de ligação entre axónios e neurónios.
* O valor da sinapse determina o peso (*importancia*) do sinal a entrar no neurónio -> **excitativo**, **inibidor** ou **nulo**
* A variação no tempo determina a aprendizagem da RNA

----------
### Ativação

* O valor de ativação é representado por **um único valor**
* O valor de ativação **varia com o tempo**
* A gama de valores varia com o modelo adotado

-------
### Transferencia

* O valor de transferencia de um neurónio determina o valor que é colocado na saída -> *tranferido através do axónio*
* É calculado como uma funçao do valor de ativação
  
---------
### Regras de aprendizagem

O treino de uma RNA corresponde à aplicação de regras de aprendizagem, por forma a fazer variar os pesos das ligações *sinapses*