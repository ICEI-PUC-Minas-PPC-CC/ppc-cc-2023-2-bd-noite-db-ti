# 1. Introdução

Atualmente um dos maiores problemas enfrentados pelas empresas de TI, que particularmente realizam serviços de empréstimo de equipamentos é conseguir realizar uma gerência adequada dos seus estoques de equipamentos, seja ele sua localização, condição ou até mesmo um histórico de empréstimo, sendo esse a causa de diversos transtornos causados pela ausência de um gerenciamento consistente. Através deste sistema, a empresa será capaz de monitorar a quantidade de equipamentos disponíveis, quantos estão emprestados, bem como o local onde cada equipamento se encontra nos diversos setores da empresa. 


### 1.1 Entidades Encontradas
Na primeira análise, quais foram as entidades encontradas?
As entidades encontradas no problema apresentado foram:
- Cliente
- Detalhamento
- Periférico
- Emprestimo
- Categoria

### 1.2 Contexto das Entidades

Na primeira análise, objetivos das entidades.

- Entidade _Periferico_: Responsável por armazenar todos os periféricos que a empresa que utilizará o sistema possui para cadastrar seus periféricos que estarão disponiveis para empréstimo e também se o periférico esta disponível ou não.
- Entidade _Categoria_: Responsável por armazenar qual a categoria do equipamento cadastrado.
- Entidade _Cliente_: Responsável por armazenar a empresa para qual o equipamento foi emprestado.
- Entidade _Detalhamento_: Responsável por armazenar o endereço do cliente para qual foi realizado o emprestimo.
- Entidade _Emprestimo_: Responsável por armazenar o controle de periféricos emprestados.


### 1.3  Levantamento Inicial Entidades x Atributos

Na primeira análise, quais foram os atributos iniciais encontrados?

#### CLIENTE
- ID - (FK)
- Nome
- Telefone
- Endereço
- CNPJ

#### DETALHAMENTO
- Rua
- Numero
- CEP
- Bairro
- Complemento
  
#### EMPRÉSTIMO

- ID_EQUIPAMENTO - (FK)
- ID_EMPRESA - (FK)
- DATA_EMPRÉSTIMO
- DATA_DEVOLUÇÃO

#### PERIFÉRICO
- Id - (PK)
- Nome
- Quantidade
- Categoria
- NUM_SERIE
- Marca
- Modelo
  
#### CATEGORIA
- ID - (PK)
- NOME_CAT - (PK)
- DESC_CAT
- 
## 2. Relacionamentos
- Entidade RESPONSÁVEL tem relação com a Entidade EMPRESA
- Entidade EMPRESA tem relação com a Entidade SETORES
- Entidade Setores tem relação com a Entidade PERIFÉRICOS
- Entidade PERIFÉRICOS tem relação com a Entidade CATEGORIA

## 3. Modelo Conceitual
![Capturar](https://github.com/ICEI-PUC-Minas-PPC-CC/ppc-cc-2023-2-bd-noite-db-ti/assets/43485533/5f48f09f-700a-4b27-8e56-d5acacc40731)


## 3. Representação Tabular
- Cliente: Esq_Cliente(<ins>_ID_</ins>, Nome, Telefone, Endereço, CNPJ)
- Equipamento: Esq_Equipamento(<ins>_ID_</ins>, Nome, Quantidade, Categoria, Num_Serie, Marca, Modelo, Disponibilidade)
- Emprestimo: Esq_Emprestimo(<ins>_ID-empresa_</ins>, <ins>_ID-equipamento_</ins>, data_emprestimo, data_devolucao) 
