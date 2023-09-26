# 1. Introdução

Atualmente um dos maiores problemas enfrentados pelas empresas de TI, que particularmente realizam serviços de empréstimo de equipamentos é conseguir realizar uma gerência adequada dos seus estoques de equipamentos, seja ele sua localização, condição ou até mesmo um histórico de empréstimo, sendo esse a causa de diversos transtornos causados pela ausência de um gerenciamento consistente. Através deste sistema, a empresa será capaz de monitorar a quantidade de equipamentos disponíveis, quantos estão emprestados, bem como o local onde cada equipamento se encontra nos diversos setores da empresa. 


### 1.1 Entidades Encontradas
Na primeira análise, quais foram as entidades encontradas?
As entidades encontradas no problema apresentado foram:
- Periferico
- Empresa
- Categoria
- Responsavel
- Emprestimo
- Setores 

### 1.2 Contexto das Entidades
Na primeira análise, objetivos das entidades.
- Entidade _Periferico_: Responsável por armazenar todos os periféricos que a empresa que utilizará o sistema possui para cadastrar seus periféricos que estarão disponiveis para empréstimo.
- Entidade _Categoria_: Responsável por armazenar qual a categoria do equipamento cadastrado.
- Entidade _Empresa_: Responsável por armazenar a empresa para qual o equipamento foi emprestado
- Entidade _Setores_: Responsável por armazenar os setores da empresa para os periféricos foram destinados
- Entidade _Responsavel_: Responsável por armazenar todos os responsáveis da empresa. O responsável será encarregado de receber o periférico.
- Entidade _Emprestimo_: Responsável por armazenar o controle de periféricos emprestados.


### 1.3  Levantamento Inicial Entidades x Atributos

Na primeira análise, quais foram os atributos iniciais encontrados?

#### Periferico
- Id - PK
- Nome
- Quantidade
- Categoria_

#### Empresa
- Id
- Nome
- Setores
- CNPJ
  
#### Setores

- Id
- Tipo_Setor
- Nome_Periferico
- Tipo_Periferico

#### Emprestimo
- Id_Equipamento
- Id_Empresa
  
#### Categoria
- Id
- Nome_cat
- Desc_cat
#### Responsavel
- Nome
- CPF
- CNPJ_Empresa

## 2. Relacionamentos
