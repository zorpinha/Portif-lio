# Portif-lio

# Esse é meu portifólio da fatec

## 1° atividade
Aqui foi minha primeira atividade realizada, uma apresentação sobre mim feita com a Maria Eduarda.

Arquivo da apresentação: [apresentação (1).pptx](https://github.com/user-attachments/files/19452851/apresentacao.1.pptx)

## 2° atividade
Nessa atividade tinhamos como objetivo responder as perguntas feitas através de um banco de dados pelo excel

[Quantidade de alunos estrangeiros por nacionalidade_2° Semestre 2023.xlsx](https://github.com/user-attachments/files/19452834/Quantidade.de.alunos.estrangeiros.por.nacionalidade_2.Semestre.2023.xlsx)

## 3° atividade

Utilziando a mesma tabela de dados anteriormente no excel, tinhamos como objetivo responder as mesmas 3 questões mas dessa vez utilizando o Power Bi
Power BI da Quantidade de alunos estrangeiros por nacionalidade
https://app.powerbi.com/links/6IHF-ALz0o?ctid=cf72e2bd-7a2b-4783-bdeb-39d57b07f76f&pbi_source=linkShare

## 4° atividade

Juntando todos esses conhecimentos foi nos passado a atividade em dupla, entretanto por alguns motivos na faculdade acabamos inserindo uma 3 pessoa por ter perdido sua dupla;

Nossa missão foi escolher um repositório de bancos aberto, fazer a limpeza e adaptação para as 3 perguntas que elaboramos
Assim como na 3° atividade teriamos que responder essa atividade tanto no powerbi quanto no excel.

Foi interessante essa jornada por o Power BI torna muito mais simples esse analise de dados.

## excel

Para respondermos as 3 questões elaboradas no excel, através dos dados do repisitorio que pegamos, precisamos fazer uma extensão desses dados, para podermos relacionar as demais questões.
![image](https://github.com/user-attachments/assets/eb31f159-7721-4c86-8127-ab03f5778a83)

**Utilizando a formula**

=SOMASES(intervalo_soma; intervalo_critérios1; critérios1; [intervalo_critérios2; critérios2];...)
Os criterios utilizados foram o Ano e o nome do produto, e os intervalos os respectivos nomes

Sendo nosso intervalo de soma a coluna de *IMPORTADO / EXPORTADO* e a *DISPÊNDIO / RECEITA* para segunda tabela 
![image](https://github.com/user-attachments/assets/d2ae1234-8149-4546-93b2-30595e0f762e)

A formula final ficou assim, necessitando de varios travamentos, para facilitar o preenchimento na tabela, não precisando ficar fazer reajustes.
=SOMASES(dados!$E:$E;dados!$C:$C;B9;dados!$D:$D;"IMPORTAÇÃO";dados!$A:$A;C$3)


### 1° Qual foi o ano que mais se teve exportação do produto asfalto? 			

A resposta para primeira pergunta foi utilizada a formula Máximo e Procx.
Para acharmos a quantidade máxima de asfalto esportada durante os anos, utilizamos a formula máximo selecionando todos os anos de esportação apenas da linha de asfalto.

![EXCEL_pTgKXRf42d](https://github.com/user-attachments/assets/3c8bc4f1-d1ed-40a1-a049-c28db6699974)

depois precisavamos achar qual ano foi encontrado esse valor, para isso utilizamos o procx.

**=PROCX(pesquisa_valor; pesquisa_matriz; matriz_retorno; [se_não_encontrada]; [modo_correspondência]; [modo_pesquisa])**

![EXCEL_lJ5irJKICo](https://github.com/user-attachments/assets/0d6805dd-118c-47bd-82a4-0c13f133f9df)

*=PROCX(E4;'dados 2'!C25:AB25;'dados 2'!C24:AB24;;0;)*

### 2° Qual foi o ano com maior receita de exportação?			

A segunda questão foram utilizadas as mesmas formulas mudando apenas as areas de seleção, sendo o foco os anos e o total de receita de exportação por ano:

![{4E8BF564-4107-40E6-9C9E-B301036BCB3C}](https://github.com/user-attachments/assets/1c4af758-703a-42b8-9446-a3191e647027)


### 3° Qual produto tem maior consumo de petróleo exportado de 2000 a 2025		

A terceira questão também foram utilizadas as mesmas formulas mudando apenas as areas de seleção, sendo o foco os anos e o total de consumo por ano de exportação por ano:
![{17F3840C-4C6B-4E13-9B92-029FE546641C}](https://github.com/user-attachments/assets/5d44e8ac-c03a-4dbb-8981-62724f8ff786)


## power BI

Já no powerbi foi apenas necessário tratar os dados para que os criterios sejam entendidos corretamente

Antes:
![{F07C6AA3-8B10-4A31-A915-1628B79E0F02}](https://github.com/user-attachments/assets/8a7710e1-d6b9-4316-8fab-ea7ac00ea2b0)

Depois

![image](https://github.com/user-attachments/assets/25aafc6d-b5e4-4f4c-9a4f-24873910a946)

Nessa tabela foi necessária apenas a alteração da formatação de DISPÊNDIO / RECEITA para aparecer em R$

### montagem dos gráficos

Inicialmente iniciamos com dois cartões

![image](https://github.com/user-attachments/assets/7f2d706b-e9f5-457d-9efd-10c1aca88c56)

Para o primeiro cartão aplicamos uma função para que o tornasse mais interarivo

![PBIDesktop_vTEBfvxjXY](https://github.com/user-attachments/assets/f3e69135-a482-46ff-9995-21af0ab303ce)

Para execução dessa função precisamos criar uma nova tabela de medida

![PBIDesktop_tUG3BwEwAO](https://github.com/user-attachments/assets/58e040ca-e1a6-4751-97f6-fb33ee32bf6f)

No campo que apareceu inserimos a seguinte formula

Produtos Selecionados = 
VAR Produtos = VALUES(dados[PRODUTO])
VAR QtdeSelecionados = COUNTROWS(Produtos)
RETURN
SWITCH(
    TRUE(),
    QtdeSelecionados = 1, CONCATENATEX(Produtos, dados[PRODUTO], ", "),
    QtdeSelecionados = 16, "todos",
    QtdeSelecionados > 1, FORMAT(QtdeSelecionados, "0") & " produtos"
)

### Explicando por termos

```
Produtos Selecionados =
Nome dado a tabela de medida.
```

Tudo que for escrito após o **=** é a formula aplicada

```
Var = <nome dado a expressão> = <dado a ser armazenado, ou, expressão>
 A expressão var armazena o resultado de uma expressão como uma variável nomeada.

```

```
VALUES= nome da tabela[coluna a ser retornada]
A formula values retorna uma lista distinta de todos os valores visíveis/selecionados da coluna
```

```
COUNTROWS(lista escolhida)
 A função countrows faz uma contagem de uma lista selecionada
```

A primeira mensão do VAR foi para armazernamos os produtos em uma repartição chamada produto.
> VAR Produtos = VALUES(dados[PRODUTO])

A segunda mensão do var foi para armazenarmos a contagem de produtos que foram separados pelo Var produtos e armazena na repartição que nomeamos de VAR QtdeSelecionados.
> VAR QtdeSelecionados = COUNTROWS(Produtos)

Após darmos essas furnções iniciais, pedidos que toda vez que ele efetue esse processo nos dê um retorno, já que apenas pedimos para ele armazenar dados com ele por isso utilizamos o _RETURN_.

```
SWITCH(
>Ele verifica cada condição de cima pra baixo, simular a um IF e ELSE na programção

* Se for 1 item → mostra o nome com CONCATENATEX
* Se for 16 itens → mostra "todos"
* Se não for nenhuma das duas anteriores → lista os produtos
```

```
CONCATENATEX(tabela, expressão,[Produtos],delimitador)
*ela faz a juntão de varios valores em uma única linha,  separando por vírgula, espaço, traço, ou o que quiser.

A tabela ou conjunto de valores que você quer juntar
expressão	O valor que será concatenado (geralmente uma coluna)
delimitador	O que separa os itens (ex: ", ", " - ", "


QtdeSelecionados = 1, CONCATENATEX(Produtos, dados[PRODUTO], ", "),

A utilização dele é necessária para que não haja repetição do mesmo nome, assim  dando um resultado falho.

```

```
FORMAT(valor, "formato")
A função FORMAT transforma números ou datas em texto formatado

FORMAT(QtdeSelecionados, "0") & " produtos"
Não conseguimos juntar duas informações distintas, sendo uma numero e outra texto, por isso formatamos o numero para que fique em formato de texto.
```

Depois da adição dos gráficos com seus respecivos campos,eixos e tema temos esse resultado:

![PBIDesktop_rVUHpICGYY](https://github.com/user-attachments/assets/ee1e07b4-a767-4eba-b774-6b9b6e46a789)


