# 📊 NexaCRM — Análise de Eficiência Comercial e Alocação de Capacidade

Este repositório contém o estudo completo de eficiência comercial da **NexaCRM**, cobrindo desde a auditoria e tratamento da base bruta (`NexaCRM_CRM_RAW.xlsx`), a geração da base tratada e documentada (`NexaCRM_CRM_TRATADA.xlsx`), até o desenvolvimento do **Dashboard Executivo Interativo** em HTML/CSS/JS.

---

## 🎯 Objetivo do Projeto

Identificar em quais segmentos (**SMB**, **Mid-Market** e **Enterprise**) e canais (**Inbound**, **Outbound** e **Partners**) a empresa deve concentrar capacidade comercial adicional para crescer com a máxima eficiência econômica, considerando receita realizada, taxa de conversão, margem percentual e tempo de ciclo de vendas.

---

## 🗂️ Estrutura do Repositório

```text
.
├── index.html                  # Dashboard executivo interativo em HTML/CSS/JS (Chart.js)
├── NexaCRM_CRM_RAW.xlsx        # Base original recebida do CRM (dados brutos)
├── NexaCRM_CRM_TRATADA.xlsx    # Base limpa e padronizada com aba de documentação
├── dashboard_segmentos.png     # Gráficos da análise comparativa por segmento
├── dashboard_segmento_canal.png# Gráficos da análise cruzada (Segmento x Canal)
└── README.md                   # Documentação do repositório
🧹 Tratamento de Dados e Regras de Negócio
Ação de Tratamento	Descrição / Critério Adotado
Padronização de Segmentos	Agrupamento de 9 grafias distintas para apenas 3 padrões: SMB (900), Mid-Market (700) e Enterprise (400).
Padronização de Canais	Normalização de variações para Inbound (911), Outbound (673) e Partners (416).
Tratamento de Nulos	Preservados 70 valores ausentes em commercial_cost sem imputação artificial.
Sinalização de Outliers	14 negociações de alto valor em Enterprise marcadas no campo enterprise_outlier_review sem exclusão.
Filtro de Conversão	Cálculo da taxa restrito às oportunidades Won e Lost, excluindo 168 registros Open.
Métricas Definidas
Receita (R$): Soma de contract_value apenas em oportunidades com estágio Won.

Taxa de Conversão (%):  
Won+Lost
Won
​
 , excluindo o estágio Open.

Margem (%):  
∑contract_value
∑(contract_value−service_cost)
​
  apenas em oportunidades Won.

Ciclo Médio (Dias): Média de days_to_close apenas em oportunidades Won.

Volume Encerramento: Soma total de oportunidades fechadas (Won+Lost).

📈 Resumo das Análises e Resultados
1. Comparativo por Segmento
Segmento	Volume (Won+Lost)	Ganhas (Won)	Receita Fechada (Won)	Conversão	Margem %	Ciclo Médio
SMB	818	244	R$ 3.551.200	29,83%	40,20%	25,1 dias
Mid-Market	651	168	R$ 8.442.100	25,81%	52,05%	35,1 dias
Enterprise	363	65	R$ 14.936.500	17,91%	37,24%	70,1 dias
2. Cruzamento Segmento × Canal (Filtro: Volume ≥ 100)
Oportunidade Prioritária — Mid-Market × Partners:

Volume: 183 oportunidades encerradas.

Taxa de Conversão: 33,88% (uma das maiores da base).

Margem %: 55,09% (a maior entre todos os grupos representativos).

Ciclo Médio: 29,8 dias (muito mais rápido que o Inbound do Mid-Market, que exige 36,5 dias).

Receita Gerada: R$ 3.244.800.

💡 Evidências, Hipóteses e Recomendações
📌 Evidências Observadas
O segmento Enterprise responde por 55,5% da receita fechada total (R$ 14,94 mi), mas exige o maior tempo de ciclo (70,1 dias) e possui a menor taxa de conversão (17,91%).

O grupo Mid-Market × Partners apresenta a melhor combinação de margem (55,09%), conversão (33,88%) e velocidade de fechamento (29,8 dias) entre os grupos com amostra suficiente.

O canal Outbound possui as menores taxas de conversão em todos os segmentos (13,48% em Enterprise, 14,12% em Mid-Market e 25,79% em SMB).

🔬 Hipóteses
O canal de parceiros (Partners) no Mid-Market atrai oportunidades de maior aderência operacional, reduzindo o custo de serviço e encurtando a tomada de decisão.

O canal Outbound pode estar operando com baixa qualificação prévia de prospectos, gerando esforço comercial sem o retorno correspondente em conversão.

🚀 Recomendações
Alocação Incremental: Realizar um piloto controlado dedicando capacidade comercial adicional ao grupo Mid-Market × Partners, utilizando Mid-Market × Inbound como grupo de controle.

Qualificação Severa em Enterprise: Implementar metodologias de qualificação mais rígidas (ex: BANT/MEDDIC) em Enterprise para evitar o desgaste da equipe em negociações longas com baixa chance de conversão.

Automação no SMB: Manter a operação de SMB sob modelos low-touch / Inside Sales automatizado para preservar sua alta velocidade (25,1 dias) sem inflar os custos de aquisição.

💻 Como Visualizar o Dashboard Interativo
Clone o repositório ou faça o download dos arquivos:

Bash
git clone [https://github.com/seu-usuario/nexacrm-eficiencia-comercial.git](https://github.com/seu-usuario/nexacrm-eficiencia-comercial.git)
Abra o arquivo index.html diretamente no seu navegador de preferência (Google Chrome, Edge, Firefox, Safari).

O dashboard carrega os dados e renderiza os gráficos interativos da Chart.js sem necessidade de servidor local ou instalação de dependências.

🛠️ Tecnologias Utilizadas
Python / Pandas: Limpeza, transformação, verificação estatística e cálculo de KPIs.

HTML5 & CSS3: Interface responsiva em layout executivo dark/moderno.

githubpages: Visualizações de dados dinâmicas e interativas.


