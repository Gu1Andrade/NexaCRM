# 📊 NexaCRM — Análise de Eficiência Comercial e Alocação de Capacidade

Este repositório contém o estudo completo de eficiência comercial da **NexaCRM**, cobrindo desde a auditoria e tratamento da base bruta (`NexaCRM_CRM_RAW.xlsx`), a geração da base tratada e documentada (`NexaCRM_CRM_TRATADA.xlsx`), até o desenvolvimento do **Dashboard Executivo Interativo** em HTML/CSS/JS.

---

## 🎯 Objetivo do Projeto

Identificar em quais segmentos (**SMB**, **Mid-Market** e **Enterprise**) e canais (**Inbound**, **Outbound** e **Partners**) a empresa deve concentrar capacidade comercial adicional para crescer com a máxima eficiência econômica, considerando receita realizada, taxa de conversão, margem percentual e tempo de ciclo de vendas.

---

🏷️ Padronização de Segmentos:Agrupamento de 9 grafias inconsistentes para apenas 3 padrões oficiais: SMB (900), Mid-Market (700) e Enterprise (400).📢 Padronização de Canais:Normalização de variações nos canais de aquisição para Inbound (911), Outbound (673) e Partners (416).⚠️ Tratamento de Nulos & Outliers:Preservação de 70 valores ausentes em commercial_cost sem imputação artificial.Identificação de 14 oportunidades atípicas em Enterprise, mantidas na análise financeira por representarem negócios reais, mas sinalizadas via flag enterprise_outlier_review.🎯 Filtro de Conversão:Cálculo das métricas focado estritamente em 1.832 oportunidades encerradas (Won e Lost), desconsiderando 168 registros Open.📊 Principais Descobertas da Análise1. Comparativo por SegmentoSegmentoVolume (Won+Lost)Ganhas (Won)Receita Fechada (Won)ConversãoMargem %Ciclo Médio🏢 SMB818244R$ 3.551.20029,83% 🟢40,20%25,1 dias ⚡🏬 Mid-Market651168R$ 8.442.10025,81%52,05% 💜35,1 dias🏙️ Enterprise36365R$ 14.936.500 💰17,91% 🔴37,24%70,1 dias ⏳2. Análise Cruzada: Segmento × Canal (Filtro: Volume ≥ 100)Ao cruzar os dados, o grupo Mid-Market × Partners destacou-se como a oportunidade de maior eficiência para a alocação de capacidade:Plaintext🏆 GRUPO PRIORITÁRIO: Mid-Market × Partners
├── 📈 Margem Média: 55,09% (A maior da empresa)
├── 🎯 Taxa de Conversão: 33,88%
├── ⚡ Ciclo Média: 29,8 dias (vs 36,5 dias no Inbound)
└── 💰 Receita Gerada: R$ 3.244.800
Grupo (Segmento × Canal)VolumeGanhas (Won)Receita Total (Won)ConversãoMargem %Ciclo Médio🎯 Mid-Market × Partners18362R$ 3.244.80033,88%55,09%29,8 diasMid-Market × Inbound29181R$ 3.911.20027,84%51,40%36,5 diasSMB × Inbound442150R$ 2.160.90033,94%41,08%24,2 diasMid-Market × Outbound17725R$ 1.286.10014,12%46,33%43,6 diasSMB × Outbound25265R$ 910.10025,79%35,44%29,0 diasSMB × Partners12429R$ 480.20023,39%45,28%21,2 diasEnterprise × Inbound10322R$ 5.185.50021,36%37,57%70,7 diasEnterprise × Outbound17824R$ 5.225.80013,48%33,50%76,5 dias💡 Evidências & Recomendações Estratégicas📌 Evidências EncontradasEnterprise gera receita, mas drena esforço: Representa 55,5% da receita realizada (R$ 14,94 mi), porém exige um tempo de ciclo muito longo (70,1 dias) e entrega a menor conversão (17,91%).Outbound ineficiente: O canal Outbound apresenta taxas de conversão baixas em todos os segmentos (13,48% em Enterprise, 14,12% em Mid-Market e 25,79% em SMB).🚀 Ações RecomendadasPiloto de Expansão: Realizar um piloto alocando capacity comercial focado no grupo Mid-Market × Partners, utilizando Mid-Market × Inbound como grupo de controle.Qualificação Severa em Enterprise: Aplicar metodologias rígidas (como MEDDIC ou BANT) para eliminar negociações sem FIT antes de consumirem tempo da equipe comercial.Automação no SMB: Manter a operação de SMB sob modelos Low-Touch ou Inside Sales automatizado para preservar a alta velocidade de fechamento (25,1 dias).🖥️ Como Visualizar o DashboardO dashboard interativo está publicado via GitHub Pages e pode ser acessado diretamente pelo link:👉 https://gu1andrade.github.io/NexaCRM/Caso queira executar localmente:


