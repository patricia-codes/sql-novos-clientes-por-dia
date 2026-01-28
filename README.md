# 📊 Case SQL — Total de Novos Clientes por Dia

## 📌 Descrição
Este case tem como objetivo calcular o **total de novos clientes cadastrados por dia**, considerando um **mês informado pelo usuário**.

A análise foi desenvolvida no **Metabase**, utilizando filtros dinâmicos para simular um cenário real de BI, onde usuários podem selecionar o período desejado sem alterar a query.

A proposta representa um caso comum em análises de dados, no qual é necessário acompanhar a evolução diária de novos cadastros para apoiar decisões estratégicas.

---


## 🎯 Objetivo da Análise
Responder à seguinte pergunta:

> **Quantos novos clientes foram cadastrados por dia em um determinado mês?**

Esse tipo de análise pode ser utilizado para:
- Monitorar crescimento diário
- Identificar picos ou quedas de aquisição
- Avaliar impacto de campanhas ou ações comerciais

---

## 🗂️ Base de Dados

**Tabela:** `People`

| Coluna     | Descrição                    |
|-----------|------------------------------|
| created_at | Data de cadastro do cliente |

> Base de dados utilizada apenas para fins educacionais (Sample Database).

---

## 🧠 Estratégia Utilizada
1. Filtrar os registros pelo **mês informado pelo usuário**
2. Extrair a data (dia) a partir do campo `created_at`
3. Agrupar os registros por dia
4. Contar o total de clientes cadastrados em cada dia
5. Ordenar os resultados cronologicamente

---
## 🧾 Query SQL

```sql
SELECT
    DATE(created_at) AS dia,
    COUNT(*) AS total_novos_clientes
FROM People
GROUP BY dia
ORDER BY dia;

```
---
## 📊 Dashboard no Metabase

Dashboard interativo desenvolvido no Metabase com filtro dinâmico por mês.

![Dashboard de Novos Clientes](total_novos_clientes.png)

---

## 📈 Principais Insights
- Identificação de dias com maior volume de novos clientes
- Detecção de padrões de crescimento ao longo do mês
- Apoio a análises de sazonalidade ou impacto de campanhas
- Possibilidade de identificar períodos com maior eficiência de aquisição


---

## 🛠️ Tecnologias Utilizadas
- SQL
- Banco de dados relacional (Sample Database)

---

## 📌 Observação Final
Projeto desenvolvido com foco em **aprendizado e prática de SQL aplicado a problemas reais de negócio**.
