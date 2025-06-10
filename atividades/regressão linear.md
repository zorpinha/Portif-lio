# Projetos de Regressão Linear 📊

Este portfólio apresenta uma série de análises de dados onde apliquei a técnica de **Regressão Linear** para construir modelos preditivos. Os projetos foram desenvolvidos utilizando **Microsoft Excel** e **Python** no ambiente **Google Colab**, com o auxílio da IA do **Google Gemini** para otimizar o fluxo de trabalho.

---

## 🍦 Projeto 1: Análise de Vendas de Sorvete

**🎯 Objetivo:** Desenvolver e comparar modelos preditivos para estimar a quantidade de sorvetes vendidos com base na temperatura do dia (°C), visando otimizar a produção e evitar desperdícios.

**💾 Conjunto de Dados:** [Ice Cream Sales Dataset](https://www.kaggle.com/datasets/sakshisatre/ice-cream-sales-dataset)

**🛠️ Ferramentas:**
* Excel
* Python (Google Colab) com Gemini AI

### **Análise e Resultados**

#### 📈 Excel

No Excel, utilizei um gráfico de dispersão para visualizar a relação entre temperatura e vendas. Ao ativar a linha de tendência, obtivemos a equação do modelo e o coeficiente de determinação ($R^2$), permitindo uma análise preditiva inicial.

A equação da reta de regressão fornecida pelo Excel foi:

```
Y = 21.442*X + 44.297
```

Onde:
* **Y** = Vendas de Sorvete
* **X** = Temperatura em °C

**Previsões do Modelo (Excel):**
![Gráfico de Dispersão no Excel](https://github.com/user-attachments/assets/81821b93-275a-4e98-a513-e57355628a50)

| Temperatura | Vendas Reais | Vendas Previstas (Tendência) |
|-------------|--------------|------------------------------|
| 15°C        | 378          | 365                          |
| 20°C        | 469          | 473                          |
| 25°C        | 608          | 580                          |
| 30°C        | 697          | 687                          |
| 40°C        | 927          | 910                          |

Utilizando a fórmula `PROJ.LIN`, o mesmo resultado foi confirmado, com um **coeficiente de determinação ($R^2$) de aproximadamente 0.9**, indicando uma alta confiabilidade do modelo.

![Fórmula PROJ.LIN no Excel](https://github.com/user-attachments/assets/9ffc406e-4dd7-4911-983f-b24bfee6f932)

**Arquivo:** [planilha.xlsx](https://github.com/user-attachments/files/20445405/Ice.Cream.and.popcorn.xlsx)

#### 🐍 Google Colab com Gemini AI

No Google Colab, importei os dados via API do Kaggle e utilizei prompts para que a IA Gemini gerasse o código Python para a análise.

**Prompts Utilizados:**
![Prompts para o Gemini](https://github.com/user-attachments/assets/e6a44f75-3ce8-43ea-aabe-fec07447cbe2)  

> Ler ice cream do path e transformar em dataframe
> Me fale os valores da linha linear de revenue
> criar um gráfico de dispersão relacionando temperature e revenue

O modelo gerado e o gráfico resultante foram:  
  
**Gráfico de Dispersão (Google Colab):**  
![Gráfico de Dispersão no Google Colab](https://github.com/user-attachments/assets/74e49c79-ac3c-46dc-9f99-fe4b4b6f2c8c)  

**Equação do Modelo (Google Colab):**
```
Y = 21.441*X + 44.296
```

**Conclusão do Projeto 1:** Os resultados do Excel e do Google Colab foram virtualmente idênticos, validando a forte correlação linear positiva entre o aumento da temperatura e o aumento das vendas de sorvete.

**Notebook:** [Link para o Google Colab](https://colab.research.google.com/drive/1L_I2JFzoAKUuvN_cZcMNAJwWJe-W748M?usp=sharing)

---

## 🍺 Projeto 2: Análise de Consumo de Cerveja

**🎯 Objetivo:** Elaborar modelos de regressão linear para prever o consumo de cerveja em uma área universitária de São Paulo, baseado em fatores como temperatura, precipitação e se o dia é um final de semana.

**💾 Conjunto de Dados:** [Beer Consumption - Sao Paulo](https://www.kaggle.com/datasets/dongeorge/beer-consumption-sao-paulo)

**🛠️ Ferramentas:**
* Excel
* Python (Google Colab) com Gemini AI

### **Análise e Resultados**

#### 📊 Excel

No Excel, foram criados modelos de regressão linear simples para cada variável independente em relação ao consumo de cerveja.

**Equações dos Modelos (Excel):**
* **Consumo vs. Temperatura Média:** `Y = 655.79*X + 877.6`
* **Consumo vs. Precipitação:** `Y = 21.664*X + 22804`
* **Consumo vs. Fim de Semana:** `Y = 3513.7*X + 21690`

**Gráficos e Análises (Excel):**  
* **Temperatura:**  
    ![Consumo por Temperatura](https://github.com/user-attachments/assets/c22a408c-189f-41a8-86fa-bfce68aae2ed)  
* **Precipitação:**  
    ![Consumo por Precipitação](https://github.com/user-attachments/assets/e57fde4a-64ba-488e-802a-3c9ad1002c44)  
* **Fim de Semana:**  
    ![Consumo por Fim de Semana](https://github.com/user-attachments/assets/286f5b4f-3f1e-4751-ad81-8ade109143c3)  

**Conclusão (Excel):** A análise de confiabilidade (R²) no Excel mostrou valores extremamente baixos para esses modelos, indicando que as variáveis isoladamente não explicam bem o consumo de cerveja.
![Baixa Confiabilidade no Excel](https://github.com/user-attachments/assets/0f879da0-7e01-4013-bc70-f3d645f98b3c)

#### 🤖 Google Colab com Gemini AI

No Colab, a IA foi instruída a gerar gráficos e modelos de regressão para cada variável.

**Prompts Utilizados:**
> Ler beer-consumption do path e transformar em dataframe.
> Criar um gráfico de dispersão relacionando os dados variáveis, como temperatura, Precipitação e Final de Semana com o consumo de cerveja.
> Gerar uma regressão linear para cada variável.

**Gráficos Gerados (Google Colab):**
* **Temperatura:**
    ![Regressão Temperatura Colab](https://github.com/user-attachments/assets/d8d830ff-7f46-49aa-849a-1a3a5b7ca832)
* **Precipitação:**
    ![Regressão Precipitação Colab](https://github.com/user-attachments/assets/d76694b9-ce6a-43d7-b3ef-b714886d284a)
* **Fim de Semana:**
    ![Regressão Fim de Semana Colab](https://github.com/user-attachments/assets/4e60f09e-6024-40d5-9d47-02c164dde4d4)

**Conclusão do Projeto 2:** Ambos os métodos (Excel e Colab) produziram modelos com baixo poder preditivo quando analisando as variáveis de forma isolada. Isso sugere que um modelo de **Regressão Linear Múltipla**, que considera o efeito combinado das variáveis, seria muito mais apropriado para este problema. A falta de uma verificação de confiabilidade clara no output básico do Colab torna difícil a tomada de decisão, mas o Excel, ao mostrar o baixo $R^2$, já sinaliza a ineficácia do modelo simples.

---

## 🏡 Projeto 3: Previsão de Preços de Imóveis

**🎯 Objetivo:** Elaborar um modelo de regressão linear para prever os preços de imóveis a partir de um conjunto de características conhecidas, como área, número de garagens, banheiros, etc.

**💾 Conjunto de Dados:** [House Pricing](https://www.kaggle.com/greenwing1985/housepricing)

**🛠️ Ferramentas:**
* Excel / Power BI
* Python (Google Colab) com Gemini AI

### **Análise e Resultados**

#### 🏢 Excel / Power BI

Devido à extensão do conjunto de dados, o Excel não conseguiu gerar os gráficos. A análise foi focada na fórmula `PROJ.LIN` e os gráficos foram feitos no Power BI.

**Análise no Excel:** A fórmula `PROJ.LIN` foi utilizada para extrair os coeficientes e as estatísticas do modelo de regressão múltipla.
![Fórmula PROJ.LIN para Casas](https://github.com/user-attachments/assets/eaa68cba-349c-421c-804b-2f86db95b7f2)

A confiabilidade ($R^2$) do modelo também se mostrou baixa, indicando que o modelo linear pode não ser o mais adequado ou que transformações nas variáveis podem ser necessárias.
![Confiabilidade Baixa do Modelo](https://github.com/user-attachments/assets/d2fcfac7-0bda-4abf-aee0-164bc5f450b9)
![Estatísticas do Modelo 1](https://github.com/user-attachments/assets/7ceecfd1-3f87-458f-bf7d-4749af6887ae)
![Estatísticas do Modelo 2](https://github.com/user-attachments/assets/f6c74206-a442-4938-96a2-eb36a51ccb7a)

#### 💻 Google Colab com Gemini AI

No Colab, a IA foi utilizada para explorar as relações entre as variáveis e o preço, além de construir o modelo de regressão.

**Prompts Utilizados:**
> Ler greenwing1985/housepricing do path e transformar em dataframe.
> Gerar um gráfico de dispersão de cada um desses topicos separados Prices com Area , Prices com Garage, etc.
> Usando o DataFrame df: gerar mapa de correlação entre o preço das casas
> gerar modelo de regressão linear para o preço das casas

**Visualizações Geradas (Google Colab):**
* **Gráficos de Dispersão:**  
    * Preço vs. Área: ![Preço x Área](https://github.com/user-attachments/assets/8a0ced82-ec9d-48cb-9f8b-2a96c13340f0)  
    * Preço vs. Garagem: ![Preço x Garagem](https://github.com/user-attachments/assets/7eb4f6fa-9296-43ca-8e2f-b12f1ab15249)  
    * Preço vs. Banheiros: ![Preço x Banheiros](https://github.com/user-attachments/assets/30e7e074-e11c-4f53-9b01-af706c496c0b)  
    * Preço vs. Mármore Branco: ![Preço x Mármore Branco](https://github.com/user-attachments/assets/5da41ef8-f82c-4a77-84f9-e6e7cd48212b)  
    * Preço vs. Mármore Preto: ![Preço x Mármore Preto](https://github.com/user-attachments/assets/3a5d1995-7a48-45f8-9ada-f12d659b57a7)  
    * Preço vs. Mármore Indiano: ![Preço x Mármore Indiano](https://github.com/user-attachments/assets/f3d38ad4-93f0-4e36-a49e-ec69ef9dd1c8)  
    * Preço vs. Andares: ![Preço x Andares](https://github.com/user-attachments/assets/78228e9b-8ed4-47a0-85d2-7941f5a74303)  

* **Mapa de Correlação:** O mapa de calor é uma ferramenta visual excelente para entender rapidamente quais variáveis têm maior impacto no preço.  
    ![Mapa de Correlação](https://github.com/user-attachments/assets/383726e5-a527-4dc4-8cc3-e87829a17fba)  

**Conclusão do Projeto 3:** O Google Colab demonstrou ser uma ferramenta muito mais poderosa para a análise exploratória de dados multivariados, especialmente com a ajuda da IA para gerar visualizações complexas como o mapa de correlação. Embora os modelos lineares iniciais tenham apresentado baixa confiabilidade, a análise no Colab abre caminho para engenharia de features, transformação de dados e a aplicação de algoritmos mais complexos para obter previsões mais precisas.
