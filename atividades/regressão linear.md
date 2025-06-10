# Projeto 1: Venda de Sorvete
O conjunto de dados disponibilizado em https://www.kaggle.com/datasets/sakshisatre/ice-cream-sales-dataset

apresenta a quantidade de sorvetes vendidos em função da temperatura do dia, em °C.  A fim de evitar desperdícios tanto de trabalho, tempo de preparo e ingredientes, deseja-se um modelo preditivo que seja capaz de fornecer a quantidade de sorvetes a serem vendidos em função da temperatura. Utilizando  técnica de Regressão Linear e as ferramentas:
   Excel
   Linguagem Python no ambiente Google Colab com AI Gemini
elabore e compare os modelos preditivos para a situação pedida.

## **Pratica**

### Excel 

No Excel bastou a utilização dos dados em um gráfico de dispersão, ativar a linha de tendência para podermos habilitar a opção equação e valores para poder identificar padrões e tendências nos dados, permitindo que você faça previsões futuras.

O numero fornecido pelo Excel

```
Y = 21.442*X + 44.297
```

Sabendo que Y= mx + B temos as seguintes tendências:

![Image](https://github.com/user-attachments/assets/81821b93-275a-4e98-a513-e57355628a50)

|temperatura | Vendas  | Tendência de Vendas |
|----------| ------------- | ------------- |
|15°| 378 | 365 |
|20°| 469 | 473 |
|25°| 608 | 580  |
|30°| 697 | 687 |
|40°| 927 | 910 |


Utilizando a Formula _proj.linear_ obtivemos o mesmo valor, e com uma confiabilidade de 0,9 de 1
 
 
![Image](https://github.com/user-attachments/assets/9ffc406e-4dd7-4911-983f-b24bfee6f932)  

[planilha.xlsx](https://github.com/user-attachments/files/20445405/Ice.Cream.and.popcorn.xlsx)

### Google Colabs

No Google Colabs após a importação com a API do kaggle utilizamos os seguintes prompts para IA do google programar:

![Image](https://github.com/user-attachments/assets/e6a44f75-3ce8-43ea-aabe-fec07447cbe2)

>Ler ice cream do path e transformar em dataframe
>Me fale os valores da linha linear de revenue
>criar um gráfico de dispersão relacionando temperature e revenue

Após isso foi retornado o seguinte gráfico

![Image](https://github.com/user-attachments/assets/74e49c79-ac3c-46dc-9f99-fe4b4b6f2c8c)

O numero fornecido pelo Google colabs

```
Y = 21.441*X + 44.296
```

Valores praticamente idênticos ao Excel, levando aos mesmos resultados.

[link do Google Colab](https://colab.research.google.com/drive/1L_I2JFzoAKUuvN_cZcMNAJwWJe-W748M?usp=sharing)

# Projeto 2: Consumo de cerveja

Os dados (amostra) foram coletados em São Paulo — Brasil, em uma área universitária, onde acontecem algumas festas com turmas de alunos de 18 a 28 anos (média). O conjunto de dados utilizado  possui 7 variáveis, sendo uma variável dependente, com período de um ano.
A partir dos dados disponibilizados em:  https://www.kaggle.com/datasets/dongeorge/beer-consumption-sao-paulo
foram elaborados modelos realizam previsões sobre o consumo de cerveja, utilizando a técnica de Regressão Linear.

   Excel (Consumo_cerveja.xlsx em anexo)
   Linguagem Python no ambiente Google Colab com AI Gemini (cerveja.ipynb em anexo)

Responda:
Os dois modelos são iguais? Explique se houver diferenças e o motivo de elas existirem?
Qual modelo você usaria? Por quê?

Compare os resultados obtidos com aqueles apresentados em:
https://ivanildo-batista13.medium.com/regress%C3%A3o-linear-m%C3%BAltipla-em-python-eb4b6603a3. Há diferenças entre os modelos? Explique.

## **Pratica**


### Excel 

No Excel bastou a utilização dos dados em um gráfico de dispersão, sendo esses os números fornecidos pelo excel:
```
Consumo por temperatura média 
Y=655.79*X+877.6
```

```
Consumo por precipitação
Y=21.664*X+22804
```

```
Consumo por Finais de Semana
Y=3513.7*X+21690
```


![Image](https://github.com/user-attachments/assets/c22a408c-189f-41a8-86fa-bfce68aae2ed)

|temperatura | Vendas  | Tendência de Vendas |
|----------| ------------- | ------------- |
|15°| 23055 | 11252 |
|20°| 23375 | 14019 |
|25°| 22696 | 17272  |
|28°| 24886 | 19370.878 |


![Image](https://github.com/user-attachments/assets/e57fde4a-64ba-488e-802a-3c9ad1002c44)

| temperatura | precipitação | Vendas  | Tendência de Vendas |
|----------|------------------|------------- | ------------- |
|15°| 16.6 |  20738 | 11304.66 |
|20°| 28.6 | 23375 | 14019 |
|25°| 16.6 | 29637 | 19633 |
|28°| 0 | 30524 | 877.6 |

![Image](https://github.com/user-attachments/assets/286f5b4f-3f1e-4751-ad81-8ade109143c3)

| temperatura | final de semana | Vendas  | Tendência de Vendas |
|----------|------------------|------------- | ------------- |
|15°| 1 |  372297 | 11304.66 |
|20°| 1 | 24827 | 490041 |
|25°| 1 | 30943 | 611176 |
|28°| 1 | 3769| 699847 |

### Google Colab

No Google Colab após a importação com a API do kaggle utilizamos os seguintes prompts para IA do google programar:
>Ler beer-consumption do path e transformar em dataframe.
> Criar um gráfico de dispersão relacionando os dados variáveis, como temperatura, Precipitação e Final de Semana com o consumo de cerveja.
>Gere uma regressão linear entre o consumo de cerveja e temperatura média.
>Gere uma regressão linear entre o consumo de cerveja e precipitação.
>Gere uma regressão linear entre o consumo de cerveja e final de semana.

Após isso foi retornado os seguintes gráficos.

![Image](https://github.com/user-attachments/assets/d8d830ff-7f46-49aa-849a-1a3a5b7ca832)

|temperatura | Vendas  | Tendência de Vendas |
|----------| ------------- | ------------- |
|15°| 23055 | 21.0278 |
|20°| 23375 | 24.3616 |
|25°| 22696 | 28.28 |
|28°| 24886 | 30.808 |

![Image](https://github.com/user-attachments/assets/d76694b9-ce6a-43d7-b3ef-b714886d284a)

| temperatura | precipitação | Vendas  | Tendência de Vendas |
|----------|------------------|------------- | ------------- |
|15°| 16.6 |  20738 | 26873 |
|20°| 28.6 | 23375 | 272006 |
|25°| 16.4 | 26836 | 21486 |
|28°| 0 | 24886 | 27.734 |

![Image](https://github.com/user-attachments/assets/4e60f09e-6024-40d5-9d47-02c164dde4d4)


| temperatura | final de semana | Vendas  | Tendência de Vendas |
|----------|------------------|------------- | ------------- |
|15°| 1 |  24227 | 101,2228 |
|20°| 1 | 31663 | 124,642 |
|25°| 1 | 26836 | 149.0452 |
|28°| 1 | 30524 | 164,7892  |

**Conclusão:**

No Excel ambos valores estão com uma confiabilidade extremamente baixa.

![Image](https://github.com/user-attachments/assets/0f879da0-7e01-4013-bc70-f3d645f98b3c)

Já no google colab também não temos essa verificação o que torna ambos dados não confiáveis, sendo assim difícil tomar uma decisão certeira. 

Por questões do Excel mostrar o nível de confiabilidade dele utilizaria ele, ou buscaria outra forma para ter indicadores melhores.

# Projeto 3: Venda de casas
A partir de  um conjunto de dados de características conhecidas dos imóveis, disponível em https://www.kaggle.com/greenwing1985/housepricing
elaborar um modelo que realize previsões sobre os preços de imóveis, utilizando a técnica de Regressão Linear. Para isso, use:

   Excel
   Linguagem Python no ambiente Google Colab com AI Gemini
Dados

preços - Preços do imóveis
área - Área do imóvel
garagem - Número de vagas de garagem
banheiros - Número de banheiros
lareira - Número de lareiras
mármore - Se o imóvel possui acabamento em mármore branco (1) ou não (0)
andares - Se o imóvel possui mais de um andar (1) ou não (0)

## **Pratica**

### Excel 

Para os dados sobre as casas por ser uma planilha muito extensa, o Excel não suportou gerar gráficos sendo necessário a realização desses gráficos pelo Power Bi.

Com a utilização da formula __PROJ.LIN__ chegamos a esses valores:

![Image](https://github.com/user-attachments/assets/eaa68cba-349c-421c-804b-2f86db95b7f2)

A confiabilidade também foram bem baixa desses dados, o que torna meio incerta a utilização do mesmo.

![Image](https://github.com/user-attachments/assets/d2fcfac7-0bda-4abf-aee0-164bc5f450b9)

![Image](https://github.com/user-attachments/assets/7ceecfd1-3f87-458f-bf7d-4749af6887ae)

![Image](https://github.com/user-attachments/assets/f6c74206-a442-4938-96a2-eb36a51ccb7a)

### Google Colab

No Google Colab após a importação com a API do kaggle utilizamos os seguintes prompts para IA do google programar:
>Ler greenwing1985/housepricing do path e transformar em dataframe.
>Gerar um gráfico de dispersão de cada um desses topicos separados Prices com Area  , Prices com Garage, Prices com Baths, Prices  com White Marble, Prices com Black Marble, Prices com Indian Marble, prices com Floors
>Usando o DataFrame df: gerar mapa de correlação entre o preço das casas
>gerar modelo de regressão linear  para o preço das casas

Após isso foi retornado os seguintes gráficos.

![Image](https://github.com/user-attachments/assets/8a0ced82-ec9d-48cb-9f8b-2a96c13340f0)

![Image](https://github.com/user-attachments/assets/7eb4f6fa-9296-43ca-8e2f-b12f1ab15249)

![Image](https://github.com/user-attachments/assets/30e7e074-e11c-4f53-9b01-af706c496c0b)

![Image](https://github.com/user-attachments/assets/5da41ef8-f82c-4a77-84f9-e6e7cd48212b)

![Image](https://github.com/user-attachments/assets/3a5d1995-7a48-45f8-9ada-f12d659b57a7)

![Image](https://github.com/user-attachments/assets/f3d38ad4-93f0-4e36-a49e-ec69ef9dd1c8)

![Image](https://github.com/user-attachments/assets/78228e9b-8ed4-47a0-85d2-7941f5a74303)

![Image](https://github.com/user-attachments/assets/383726e5-a527-4dc4-8cc3-e87829a17fba)

