# 📊 NexaCRM — Análise de Eficiência Comercial e Alocação de Capacidade

Este repositório contém o estudo completo de eficiência comercial da **NexaCRM**, cobrindo desde a auditoria e tratamento da base bruta (`NexaCRM_CRM_RAW.xlsx`), a geração da base tratada e documentada (`NexaCRM_CRM_TRATADA.xlsx`), até o desenvolvimento do **Dashboard Executivo Interativo** em HTML/CSS/JS.

---

## 🎯 Objetivo do Projeto

Identificar em quais segmentos (**SMB**, **Mid-Market** e **Enterprise**) e canais (**Inbound**, **Outbound** e **Partners**) a empresa deve concentrar capacidade comercial adicional para crescer com a máxima eficiência econômica, considerando receita realizada, taxa de conversão, margem percentual e tempo de ciclo de vendas.

---

# Relatório de Análise Comercial e Tomada de Decisão

Este documento consolidado detalha o processo analítico passo a passo que fundamenta as decisões estratégicas de alocação de capacidade comercial. 

---
A análise foi conduzida em duas etapas principais:

1. **Análise Macro por Segmento:** Avaliação comparativa entre os segmentos **SMB**, **Mid-Market** e **Enterprise**.
2. **Análise Micro por Segmento × Canal de Aquisição:** Cruzamento de dados focado na busca de grupos de alta eficiência econômica e operacional, respeitando o critério de volume estatisticamente representativo (amostras $\ge 100$ oportunidades encerradas).

---

## Etapa 1: Análise Macro por Segmento

### 1. Quadro Comparativo Inicial

| Segmento | Volume (Won+Lost) | Receita Won | Conversão (%) | Margem (%) | Ciclo Médio Won (dias) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **SMB** | 818 | R\$ 3,55 mi | 29,83% | 40,20% | 25,1 |
| **Mid-Market** | 651 | R\$ 8,44 mi | 25,81% | 52,05% | 35,1 |
| **Enterprise** | 363 | R\$ 14,94 mi | 17,91% | 37,24% | 70,1 |

---

### 2. Evidências Observadas (Passo a Passo)

* **Enterprise:** Concentra a maior receita realizada (**R\$ 14,94 mi**, equivalente a aproximadamente **63%** da receita *Won* total). Contudo, registra a menor taxa de conversão (**17,91%**) e o maior ciclo de vendas (**70,1 dias**).
* **Mid-Market:** Apresenta o melhor equilíbrio entre eficiência e retorno econômico. É o segmento com a **maior margem** (**52,05%**), possui receita expressiva (**R\$ 8,44 mi**), conversão intermediária (**25,81%**) e ciclo sustentável (**35,1 dias**).
* **SMB:** Destaca-se pela **maior velocidade** (**25,1 dias**) e **maior taxa de conversão** (**29,83%**). No entanto, o ticket médio inferior resulta em receita total significativamente menor (**R\$ 3,55 mi**), além de uma margem (**40,20%**) abaixo do *Mid-Market*.
* **Desconexão Volume vs. Receita:** O volume de oportunidades encerradas é inversamente proporcional ao volume financeiro gerado: *Enterprise* tem menos da metade do volume de *SMB* (363 vs. 818), mas gera mais de 4 vezes sua receita.

---

### 3. Hipóteses Levantadas

1. **Enterprise Ticket & Complexidade:** O ticket médio elevado compensa a baixa conversão na receita total, mas a alta complexidade das negociações dilata o ciclo comercial e eleva os custos de serviço (reduzindo a margem).
2. **Eficiência do Mid-Market:** A combinação de margem elevada com ciclo intermediário sinaliza uma relação comercial altamente eficiente para atração e fechamento.
3. **Escala Limitada do SMB:** A velocidade e a taxa de conversão do SMB indicam um processo de venda fluido, porém o menor valor unitário impõe um teto para o crescimento da receita absoluta.

---

### 4. Decisão de Nível Macro: Priorização de Capacidade

* **Mid-Market (Prioridade de Alocação):** Identificado como o candidato ideal para recebimento de capacidade comercial incremental devido ao seu equilíbrio entre taxa de conversão, margem e tempo de ciclo.
* **Enterprise (Manutenção e Eficiência):** Não deve sofrer cortes de capacidade devido ao seu peso na receita total, mas requer uma revisão pontual de processos antes de receber novos investimentos.
* **SMB (Preservação da Eficiência):** Manutenção da estrutura atual focada na otimização de custos e processos.

---

## Etapa 2: Aprofundamento por Segmento × Canal de Aquisição

Para garantir a acurácia das recomendações e evitar decisões baseadas em ruídos amostrais, foi estabelecido o **filtro de prudência analítica**: apenas grupos com **pelo menos 100 oportunidades encerradas** foram considerados para a recomendação prioritária.

---

### 1. Quadro Comparativo Detalhado (Segmento × Canal)

| Segmento × Canal | Volume Encerrado | Conversão (%) | Margem (%) | Ciclo Médio (dias) | Receita Won | Status Amostral |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Mid-Market × Partners** | **183** | **33,88%** | **55,09%** | **29,8** | **R\$ 3,24 mi** | $\ge 100$ (Elegível) |
| **Mid-Market × Inbound** | 291 | 27,84% | 51,40% | 36,5 | R\$ 3,91 mi | $\ge 100$ (Elegível) |
| **SMB × Inbound** | 442 | 33,94% | 41,08% | 24,2 | R\$ 2,16 mi | $\ge 100$ (Elegível) |
| **Mid-Market × Outbound** | 177 | 14,12% | 46,33% | 43,6 | R\$ 1,29 mi | $\ge 100$ (Elegível) |
| **SMB × Outbound** | 252 | 25,79% | 35,44% | 29,0 | R\$ 0,91 mi | $\ge 100$ (Elegível) |
| **SMB × Partners** | 124 | 23,39% | 45,28% | 21,2 | R\$ 0,48 mi | $\ge 100$ (Elegível) |
| **Enterprise × Inbound** | 103 | 21,36% | 37,57% | 70,7 | R\$ 5,19 mi | $\ge 100$ (Elegível) |
| **Enterprise × Outbound** | 178 | 13,48% | 33,50% | 76,5 | R\$ 5,23 mi | $\ge 100$ (Elegível) |
| *Enterprise × Partners* | *82* | *23,17%* | *41,17%* | *61,2* | *R\$ 4,53 mi* | $< 100$ (Desconsiderado) |

---

### 2. Oportunidade Prioritária Selecionada: **Mid-Market × Partners**

#### A. Evidência Observada
O grupo **Mid-Market × Partners** apresentou o melhor desempenho conjunto nos quatro critérios estabelecidos:
* **Volume robusto:** 183 oportunidades encerradas.
* **Alta conversão:** 33,88% (uma das maiores da base).
* **Maior margem:** 55,09% (a maior entre todos os grupos válidos).
* **Ciclo ágil:** 29,8 dias (significativamente mais rápido que *Mid-Market × Inbound* com 36,5 dias).
* **Retorno por oportunidade:** Aprox. **R\$ 9,77 mil em margem bruta por oportunidade encerrada** ($\text{Valor do Contrato} - \text{Custo do Serviço}$).

#### B. Hipótese
O canal *Partners* no segmento *Mid-Market* traz leads pré-qualificados com melhor adequação ao produto (*product-market fit*), resultando em processos de decisão mais curtos, menor custo de suporte/implementação e maior valor percebido.

#### C. Ação Experimental Recomendada
Execução de um **piloto controlado de expansão de capacidade**:
1. Aumentar gradualmente a capacidade comercial dedicada ao canal *Partners* no *Mid-Market*.
2. Manter o grupo *Mid-Market × Inbound* como grupo de controle/referência.
3. Monitorar novas oportunidades durante período fixo, controlando variáveis como região, vendedor e produto.

#### D. Métrica de Sucesso
* **Métrica Principal:** Margem bruta gerada por oportunidade encerrada.
* **Métricas Secundárias:** Manutenção das taxas de conversão ($\ge 33\%$), margem ($\ge 50\%$) e ciclo ($\le 30 \text{ dias}$).

#### E. Principal Limitação
* **Natureza Observacional:** A análise indica associação, não causalidade direta. O desempenho superior pode decorrer de fatores não isolados (ex.: experiência dos parceiros específicos, mistura regional de clientes).
* **Tamanho Amostral:** Embora o filtro de 100 observações traga segurança prudencial, não constitui garantia estatística absoluta contra variações do mercado.

---

## 3. Síntese do Contexto Geral para Tomada de Decisão

```
                        [ALOCAÇÃO DE CAPACIDADE COMERCIAL]
                                       |
       +-------------------------------+-------------------------------+
       |                               |                               |
[MID-MARKET × PARTNERS]     [MID-MARKET × INBOUND]          [SMB × INBOUND]
 Oportunidade Prioritária       Grupo de Referência            Alta Velocidade
 (Maior Margem e Ciclo Curto)   (Volume e Receita Sólida)      (Menor Margem Relativa)
```

1. **Mid-Market × Partners (Foco Principal):** Prioridade máxima para teste experimental e expansão de recursos comerciais.
2. **Mid-Market × Inbound (Referência):** Mantém-se como a espinha dorsal de receita do Mid-Market (R\$ 3,91 mi), servindo como grupo de controle para o experimento.
3. **SMB × Inbound (Eficiência de Volume):** Apresenta excelente velocidade (24,2 dias) e conversão (33,94%), mas possui margem menor (41,08%), sendo mantido para volume.
4. **Enterprise (Revisão Qualitativa):** Foco em eficiência de processo antes de qualquer expansão, visando reduzir o ciclo médio superior a 70 dias.

4. Visualização Interativa do Dashboard

Para explorar visualmente os indicadores, aplicar filtros dinâmicos por segmento, canal e acompanhar as métricas em tempo real, acesse o dashboard interativo no link abaixo:

👉 Acessar Dashboard [NexaCRM](https://gu1andrade.github.io/NexaCRM/)
