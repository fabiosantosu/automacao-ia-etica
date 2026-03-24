# Arquitetura do Workflow

A estrutura de automação foi desenhada para garantir escalabilidade e baixo custo de manutenção.

![Diagrama de Workflow](Workflow_Automacao_Qualificacao_Leads.jpg)

## Fluxo de Dados (Triagem de Leads)

1. **Gatilho (Webhook):** Captura instantânea de Nome, E-mail, Empresa e Mensagem do formulário do site.
2. **Processamento (OpenAI):** O motor de IA recebe os dados brutos e aplica a lógica de qualificação qualitativa.
3. **Saída (Google Sheets):** Registro automático dos dados originais anexados à classificação (Status e Prioridade) gerada pela IA.

## Componentes Técnicos
* **Conectividade:** Integração via Webhook para eliminação de latência.
* **Motor de Decisão:** Modelo GPT-4o configurado para retornar dados estruturados.
* **Repositório de BI:** Planilha mestre organizada para facilitar a criação de dashboards de performance de vendas.
