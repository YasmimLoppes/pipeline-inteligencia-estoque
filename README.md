# pipeline-inteligencia-estoque
Pipeline de Dados para otimização de estoque e reposição preditiva, transformando registros de caixa em inteligência de compras e redução de ruptura.

# 📦 Smart Stock Pipeline: Inteligência de Giro e Reposição

Pipeline de Engenharia de Dados desenvolvido para otimizar o fluxo entre o **fechamento de caixa** e a **reposição de estoque**, baseado em observações reais de operação varejista.

---

## 🎯 O Problema (Contexto Real)
Atuando na linha de frente (caixa), observei um gap crítico: a falta de sincronia entre o volume de vendas em tempo real e a velocidade de reposição das prateleiras. 

**Impactos observados:**
* **Ruptura de Estoque:** O sistema indica saldo, mas a prateleira está vazia (perda de venda).
* **Capital Imobilizado:** Excesso de produtos de baixo giro ocupando espaço nobre.
* **Ineficiência Logística:** Reposição reativa em vez de preditiva.

## 💡 A Solução
Este pipeline automatiza o cruzamento de dados de **Vendas (POS)** e **Inventário**, gerando alertas inteligentes de reposição e classificação de produtos por relevância financeira (**Curva ABC**).

---

## 🏗️ Arquitetura do Pipeline

O projeto segue a estrutura de medalhão (Bronze, Silver, Gold) para garantir a qualidade do dado:

1.  **Ingestão (Bronze):** Extração de logs de vendas do caixa e posição de estoque (CSV/JSON).
2.  **Processamento (Silver):** Limpeza com **Python & Pandas**, normalização de SKUs e cálculo de giro.
3.  **Inteligência (Gold):** Modelagem SQL para definir o "Ponto de Pedido" e priorização por Curva ABC.

---

## 🛠️ Tecnologias e Conceitos de Negócio

* **Linguagem:** Python (Pandas para análise matricial).
* **Banco de Dados:** SQL (Consultas analíticas e joins de movimentação).
* **Conceito de Logística:** Curva ABC (Priorização de estoque por faturamento).
* **Gestão de Estoque:** Cálculo de Estoque Mínimo e Ponto de Ressuprimento.

---

## 🚀 Demonstração de Lógica (Preview)

> *Lógica de Ponto de Pedido Implementada:*
---

## 📊 Insights de Operação (Varejo de Moda)

Com base na execução do pipeline, identificamos que:
* **Prioridade de Reposição:** Itens como 'Moletom Canguru G' e 'Tênis Running' estão abaixo do estoque mínimo (12 unidades), exigindo ação imediata.
* **Saúde Financeira:** O monitoramento contínuo evita que o capital da loja fique imobilizado em excessos ou que vendas sejam perdidas por falta de grade.

> *Este gráfico foi gerado automaticamente pelo script `visualizacao.py` cruzando dados reais de vendas de caixa com inventário físico.*

---

## 🧑‍💻 Sobre o Autor
Desenvolvido por **Yasmin Lopes**, estudante de ADS e Engenheiro de Dados em formação. Utilizo minha experiência prática na operação de varejo para construir soluções de dados que resolvem problemas reais de negócio.

* **LinkedIn:**  www.linkedin.com/in/yasmim-loppes/
* **GitHub:** www.github.com/yasmimloppes
