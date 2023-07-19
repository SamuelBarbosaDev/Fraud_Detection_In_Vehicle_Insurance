# Fraud Detection In Vehicle Insurance

### Índice

- [Fraud Detection In Vehicle Insurance](#fraud-detection-in-vehicle-insurance)
    - [Índice](#índice)
    - [Contextualização:](#contextualização)
    - [Metodologia Aplicada:](#metodologia-aplicada)
  - [Entendimento do Negócio:](#entendimento-do-negócio)
  - [Entendimento dos Dados:](#entendimento-dos-dados)
    - [Variáveis:](#variáveis)
    - [Verificando as Dimensões do DataFrame:](#verificando-as-dimensões-do-dataframe)
    - [Describe:](#describe)
    - [Verificando Valores Nulos:](#verificando-valores-nulos)
    - [Verificando Tipos:](#verificando-tipos)
    - [Distribuição de Churn:](#distribuição-de-churn)
  - [Preparação dos Dados:](#preparação-dos-dados)
    - [Train-test split:](#train-test-split)
    - [Construção Do Pipeline De Pré-Processamento:](#construção-do-pipeline-de-pré-processamento)
  - [Modelagem:](#modelagem)
    - [Selecionando Os Modelos:](#selecionando-os-modelos)
    - [Construção Do Pipeline:](#construção-do-pipeline)
  - [Avaliação:](#avaliação)
  - [Implantação:](#implantação)
  - [Pré-requisitos para executar o projeto:](#pré-requisitos-para-executar-o-projeto)
    - [Instale o Pacote Anaconda:](#instale-o-pacote-anaconda)
    - [Ambiente virtual e Dependências:](#ambiente-virtual-e-dependências)


### Contextualização:
Com o objetivo de reduzir custos, uma seguradora está reformulando o processo de análise de fraudes em acionamentos de seguros de automóveis. Essas fraudes ocorrem quando o solicitante aciona o seguro alegando um acidente e danos que não ocorreram de fato, mas foram simulados de alguma forma.

O processo de análise de fraudes consome tempo e esforço dos analistas da empresa. Portanto, normalmente, é realizado em uma amostra aleatória de todos os acionamentos recebidos. No entanto, a seguradora busca maior acertividade em suas decisões e deseja evitar o maior número possível de fraudes.

Nosso papel como cientistas de dados é desenvolver um modelo capaz de identificar possíveis fraudes para cada novo acionamento de seguro. Dessa forma, a equipe de analistas poderá focar em possíveis casos de fraude e não mais em uma amostra aleatória.

### Metodologia Aplicada:
A análise foi realizada utilizando o modelo CRISP-DM, o CRISP-DM (Cross Industry Standard Process for Data Mining) é um modelo padrão de processo para projetos de mineração de dados que define um conjunto de fases e tarefas que devem ser executadas para desenvolver soluções de mineração de dados efetivas.

![CRISP-DM](/core/img/CRISP-DM.png)

O modelo CRISP-DM é uma abordagem sistemática e estruturada para a mineração de dados que ajuda as empresas a desenvolver soluções de mineração de dados de maneira eficiente e eficaz, reduzindo o tempo e os custos do projeto.

## Entendimento do Negócio:
Utilize um modelo de classificação para mapear qual o perfil de usuários tem mais chance parar de utilizar os serviços da empresa.
Compreender quem é o perfil que está aumentando o churn do seu negócio é essencial para tomar ações que reduzam essas perdas, seja alterando critérios na venda ou modificando o produto.

## Entendimento dos Dados:
### Variáveis:
| Coluna               | Descrição                                                                             |
| -------------------- | ------------------------------------------------------------------------------------- |
| Month                | Mês do acidente                                                                       |
| WeekOfMonth          | Semana do mês do acidente                                                             |
| DayOfWeek            | Dia da semana do acidente                                                             |
| Make                 | Marca do veículo                                                                      |
| AccidentArea         | Área do acidente                                                                      |
| DayOfWeekClaimed     | Mês do acionamento do seguro                                                          |
| MonthClaimed         | Semana do mês do acionamento do seguro                                                |
| WeekOfMonthClaimed   | Dia da semana do acionamento do seguro                                                |
| Sex                  | Sexo do segurado                                                                      |
| MaritalStatus        | Estado civil                                                                          |
| Age                  | Idade                                                                                 |
| Fault                | Responsável pelo acidente (quem cometeu o erro)                                       |
| PolicyType           | Tipo de apólice                                                                       |
| VehicleCategory      | Categoria do veículo                                                                  |
| VehiclePrice         | Preço do veículo                                                                      |
| FraudFound_P         | Se há fraude(1) ou não(0)                                                             |
| PolicyNumber         | Número de apólice                                                                     |
| RepNumber            | Numeração entre 1 e 16                                                                |
| Deductible           | Custo do seguro                                                                       |
| DriverRating         | Classificação do motorista                                                            |
| Days_Policy_Accident | Total de dias entre aquisição do seguro e ocorrência do acidente                      |
| Days_Policy_Claim    | Total de dias entre a contratação do seguro e a comunicação do acidente.              |
| PastNumberOfClaims   | Número de reclamações anteriores feitas pelo proprietário do veículo                  |
| AgeOfVehicle         | Idade do veículo                                                                      |
| AgeOfPolicyHolder    | Idade do titular do seguro                                                            |
| PoliceReportFiled    | Se o sinsitro foi comunicado à polícia                                                |
| WitnessPresent       | Se houve testemunhas                                                                  |
| AgentType            | Interno é quando a fraude é praticada por pessoas que trabalham na seguradora         |
| NumberOfSuppliments  | São danos ao veículo não registrados no momento da reclamação                         |
| AddressChange_Claim  | Se o proprietário do seguro se mudou após comunicar um acidente e quanto tempo depois |
| NumberOfCars         | Número de carros envolvidos no acidente                                               |
| Year                 | Ano em que ocorreu o acidente                                                         |
| BasePolicy           | Tipo de seguro, igual a PolicyType           

### Verificando as Dimensões do DataFrame:
![Data Frame](/core/img/shape.png)

### Describe:
![Data Frame](/core/img/describe.png)

### Verificando Valores Nulos:
![Data Frame](/core/img/nulos.png)

### Verificando Tipos:
![Data Frame](/core/img/tipos.png)

### Distribuição de Churn:
![Data Frame](/core/img/distribuição.png)

## Preparação dos Dados:

### Train-test split:
![Data Frame](/core/img/train_test_split.png)

### Construção Do Pipeline De Pré-Processamento:
![Data Frame](/core/img/pre_processamento.png)

## Modelagem:

### Selecionando Os Modelos:
![Data Frame](/core/img/selecionando_os_modelos.png)

### Construção Do Pipeline:
![Data Frame](/core/img/pipeline.png)

![Data Frame](/core/img/pipeline_display.png)



## Avaliação:
Com o objetivo de reduzir custos, a seguradora está reformulando o processo de análise de fraudes em acionamentos de seguros de automóveis. Utilizamos técnicas de balanceamento de dados, como Random Oversampling, SMOTE, ADASYN e Random Undersampling.

Criamos um pipeline de pré-processamento e um pipeline para cada modelo e técnica de balanceamento. No final, o pipeline de regressão logística em conjunto com a técnica de oversampling aleatório apresentou o melhor desempenho, com um F1 de 0.64.

No entanto, esta é a versão 0.1.0 do projeto, e há vários pontos que serão atualizados em versões futuras. Com isso em mente, listamos algumas possíveis atualizações que podem ser feitas no futuro:

- **Exploração dos dados:** Analisar os dados com mais detalhes para entender melhor as características dos clientes churn e identificar padrões ou insights relevantes. Isso pode ajudar a identificar variáveis-chave que afetam o churn e a orientar a seleção de recursos e técnicas de pré-processamento mais adequadas.

- **Engenharia de recursos:** Considerar a possibilidade de criar novas variáveis ou transformar as existentes para capturar melhor a informação relevante para a previsão do churn. Isso pode envolver a criação de variáveis agregadas, razões ou categorizações mais refinadas.

- **Seleção de recursos:** Utilizar técnicas de seleção de recursos para identificar as variáveis mais relevantes para o problema de churn. Isso pode ajudar a simplificar o modelo, reduzir o ruído e melhorar a generalização.

- **Experimentação com diferentes modelos:** Embora a regressão logística tenha apresentado bom desempenho, vale a pena explorar outros algoritmos de classificação, como árvores de decisão, random forest, gradient boosting, SVM, entre outros. Cada algoritmo tem suas próprias características e pode se adaptar melhor ao seu conjunto de dados específico.

- **Ajuste de hiperparâmetros:** Experimentar ajustar os hiperparâmetros do seu modelo para otimizar o desempenho. O ajuste correto dos hiperparâmetros pode melhorar significativamente o desempenho do modelo.

- **Validação cruzada:** Utilizar técnicas de validação cruzada para avaliar o desempenho do modelo de forma mais robusta. Isso envolve dividir o conjunto de dados em conjuntos de treinamento e teste em várias iterações para obter estimativas mais confiáveis do desempenho do modelo.

- **Outras métricas de avaliação:** Além do F1-score, considerar outras métricas de avaliação, como precisão, recall, matriz de confusão, curva ROC e área sob a curva (AUC-ROC). Essas métricas podem fornecer uma visão mais completa do desempenho do modelo em diferentes aspectos.

- **Validação externa:** Se possível, validar o desempenho do seu modelo em um conjunto de dados externo ou em um ambiente de produção. Isso ajuda a verificar se o desempenho observado é generalizável e se o modelo está realmente fornecendo insights úteis para a empresa.

## Implantação:
Iniciando a etapa de implementação do modelo em produção.

## Pré-requisitos para executar o projeto:
Abaixo, listarei os requisitos necessários para que o projeto funcione corretamente.

### Instale o Pacote Anaconda:
Você pode baixá-lo em: <https://www.anaconda.com/download/> 

### Ambiente virtual e Dependências:
Criando ambiente virtual:
```
conda create -n .tcc python=3.10.6
```

Entrando no ambiente virtual:
```
conda activate .tcc
```

Instale as dependências:
```
pip install -r core/requirements.txt
```

---
Linkedin: <https://www.linkedin.com/in/samuel-barbosa-dev/> 

E-mail: <samueloficial@protonmail.com>