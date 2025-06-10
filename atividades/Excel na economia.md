# Guia: Aplicando Matemática Econômica no Excel

Este guia demonstra como traduzir conceitos e fórmulas da matemática econômica para a aplicação prática em planilhas do Excel, facilitando a análise de custos, receitas, lucros e projeções.

## 📈 A Lógica: Traduzindo a Teoria para a Planilha

O primeiro passo é entender que cada célula no Excel pode representar uma variável de uma fórmula econômica. A tabela abaixo ilustra essa correspondência:

| Teoria Econômica (Fórmula) | Variável Comum | Célula (Exemplo) | Fórmula no Excel |
| :--- | :---: | :---: | :--- |
| Preço | $P$ | `B2` | `=19.90` |
| Quantidade | $Q$ | `C2` | `=100` |
| Custo Fixo | $CF$ | `D2` | `=5000` |
| Custo Variável Unitário | $CV_{u}$ | `E2` | `=8.50` |
| Receita Total ($P \times Q$) | $RT$ | `F2` | `=B2*C2` |
| Custo Total ($CF + CV_{u} \times Q$) | $CT$ | `G2` | `=D2+(E2*C2)` |
| Lucro ($\pi = RT - CT$) | $\pi$ | `H2` | `=F2-G2` |

---

## 🍦 Aplicação Prática: O Caso dos Sorvetes e Panelas

Vamos usar uma planilha de exemplo para demonstrar os cálculos.

**Estrutura da Planilha:**
| Coluna A | Coluna B | Coluna C | Coluna D | Coluna E |
| :--- | :--- | :--- | :--- | :--- |
| **Produto** | **Preço de Venda (P)** | **Qtd. Vendida (Q)** | **Custo Fixo (CF)** | **Custo Variável Unit. (CVu)**|
| Panela | R$ 80,00 | 150 | R$ 10.000,00 | R$ 35,00 |
| Sorvete (pote)| R$ 25,00 | 800 | R$ 10.000,00 | R$ 12,00 |

### 1. Cálculo de Receita Total (RT)
A fórmula matemática é `$RT = P \times Q$`. Para calcular a receita de "Panela" na linha 2, crie uma nova coluna (ex: Coluna F) e insira:

* **Fórmula em `F2`:** `=B2*C2`
* **Resultado:** R$ 12.000,00

### 2. Cálculo de Custo Total (CT)
A fórmula matemática é `$CT = CF + (CV_{u} \times Q)$`. Para calcular o custo total de "Panela", crie uma nova coluna (ex: Coluna G) e insira:

* **Fórmula em `G2`:** `=D2+(E2*C2)`
* **Resultado:** R$ 15.250,00

> **💡 Dica Importante:** Se o Custo Fixo (`CF`) for o mesmo para todos os produtos, coloque-o em uma única célula (ex: `D2`) e use uma **referência absoluta ($)** na fórmula para "travá-la". Assim, ao arrastar a fórmula para baixo, ela sempre usará o valor da célula `$D$2`.
>
> Exemplo: `= $D$2 + (E2*C2)`

### 3. Cálculo do Lucro (π)
A fórmula matemática é `$\pi = RT - CT$`. Para calcular o lucro de "Panela", crie uma nova coluna (ex: Coluna H) e insira:

* **Fórmula em `H2`:** `=F2-G2`
* **Resultado:** -R$ 3.250,00 (prejuízo)

---

## 🚀 Indo Além: Conceitos Avançados no Excel

### Ponto de Equilíbrio (Break-Even Point)
O **Ponto de Equilíbrio** ocorre quando o Lucro é zero, ou seja, a Receita Total é igual ao Custo Total (`$RT = CT$`). A fórmula para encontrá-lo em quantidade de unidades é:

$$ Q_{pe} = \frac{CF}{(P - CV_{u})} $$

No Excel, para o produto "Panela", o cálculo seria:
* **Fórmula:** `=D2/(B2-E2)`
* **Resultado:** `10000 / (80 - 35)` = **222,22 unidades**. Isso significa que é preciso vender aproximadamente 223 panelas para começar a ter lucro.

### Criando Gráficos para Visualização
Para visualizar o Ponto de Equilíbrio:
1.  Crie uma tabela auxiliar com uma coluna para **Quantidade (Q)** e calcule a **Receita Total** e o **Custo Total** para cada quantidade.
2.  Selecione os três novos conjuntos de dados.
3.  No menu, vá em **Inserir > Gráficos > Gráfico de Linha**.
4.  O ponto onde a linha de `Receita Total` cruza a linha de `Custo Total` é o seu Ponto de Equilíbrio visual.

### Análise de Sensibilidade com "Atingir Meta"
E se você quisesse saber quantas panelas precisa vender para atingir um lucro de **R$ 5.000,00**?
1.  Certifique-se de que sua célula de Lucro (ex: `H2`) contém a fórmula `=F2-G2`.
2.  No menu, vá em **Dados > Teste de Hipóteses > Atingir Meta...**
3.  Preencha a caixa de diálogo:
    * **Definir célula:** `H2` (a célula do lucro)
    * **Para valor:** `5000` (o lucro desejado)
    * **Alterando célula:** `C2` (a célula da quantidade)
4.  Clique em **OK**. O Excel encontrará a quantidade necessária automaticamente.

---

## ✅ Conclusão
O Excel é uma ferramenta fantástica para dar vida à teoria econômica, permitindo que você modele cenários, analise dados e tome decisões mais informadas com agilidade. Comece com estas fórmulas básicas e explore as ferramentas mais avançadas para aprofundar suas análises.

[Planilha com as perguntas e respostas](https://github.com/user-attachments/files/20633083/Graf_K_panela_sorvetes_produtos.xlsx)

