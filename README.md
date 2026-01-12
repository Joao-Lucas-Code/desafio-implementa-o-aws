# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 12 de Janeiro de 2026
Empresa: Flor da Terra Farmácia 
Responsável: João Lucas Gomes

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Flor da Terra Farmácia, realizado por João Lucas. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos, otimizar processos operacionais e garantir a segurança financeira do negócio.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto voltadas para o setor financeiro:

### Etapa 1: 
- **Nome da ferramenta:** ![AWS Budgets](https://img.shields.io/badge/AWS-Budgets-FF9900?style=flat&logo=amazon-aws&logoColor=white)
- **Foco da ferramenta:** Controle de custos e previsibilidade financeira.
- **Descrição de caso de uso:** A farmácia utilizará o AWS Budgets para definir limites de gastos mensais com a infraestrutura de nuvem. O gestor financeiro receberá alertas automáticos via e-mail caso os gastos alcancem 80% do teto definido. Isso evita "surpresas" na fatura e permite um planejamento de caixa muito mais rigoroso.

### Etapa 2: 
- **Nome da ferramenta:** ![Amazon S3](https://img.shields.io/badge/Amazon-S3-569A31?style=flat&logo=amazons3&logoColor=white) + **S3 Glacier**
- **Foco da ferramenta:** Armazenamento de baixo custo e conformidade fiscal.
- **Descrição de caso de uso:** Farmácias precisam guardar arquivos de notas fiscais (XMLs) e registros de vendas por vários anos. Em vez de manter servidores físicos caros ou HDs externos inseguros, utilizaremos o Amazon S3. Arquivos antigos serão movidos automaticamente para a classe *Glacier*, que oferece um custo de armazenamento extremamente reduzido para documentos que raramente precisam ser acessados, mas que devem ser mantidos por lei.

### Etapa 3: 
- **Nome da ferramenta:** ![AWS Lambda](https://img.shields.io/badge/AWS-Lambda-FF9900?style=flat&logo=aws-lambda&logoColor=white)
- **Foco da ferramenta:** Redução de custos operacionais (Serverless).
- **Descrição de caso de uso:** Implementaremos o AWS Lambda para automatizar a geração de relatórios de fechamento de caixa diário. Em vez de pagar por um servidor ligado 24h por dia, o código só "acorda", processa os dados de venda e gera o relatório financeiro às 22h (fechamento). A farmácia paga apenas pelos segundos em que o código está rodando, eliminando o custo de servidores ociosos.

---

## Análise de Custo-Benefício (Estimativa)

| Cenário | Infraestrutura Tradicional (On-premise/Física) | Infraestrutura AWS (Nuvem Proposta) |
| :--- | :--- | :--- |
| **Custos de Servidor** | Gastos fixos com hardware, energia e manutenção. | Custo variável (paga apenas pelo que usa - Lambda). |
| **Armazenamento Fiscal** | Compra frequente de HDs e riscos de perda física. | Armazenamento em nuvem ultra barato (S3 Glacier). |
| **Monitoramento** | Manual e reativo (descobre o gasto após o ocorrido). | Automático e Proativo (Alertas do AWS Budgets). |
| **Segurança de Dados** | Backup manual sujeito a falhas humanas. | Redundância global e criptografia automática. |

---

## Conclusão
A implementação de ferramentas na empresa Flor da Terra Farmácia tem como esperado a redução de desperdícios com infraestrutura, a eliminação de riscos de perda de dados fiscais e uma visão clara de gastos futuros. Isso aumentará a eficiência e a produtividade da empresa, permitindo que o gestor financeiro foque em investimentos estratégicos em vez de custos fixos de TI. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias, como o AWS Cost Explorer, para análise de tendências de longo prazo.

## Anexos

* Planilha de estimativa de custos (AWS Pricing Calculator)
* Guia de configuração de alertas de faturamento
* Política de retenção de documentos fiscais (S3 Lifecycle)

Assinatura do Responsável pelo Projeto:

**João Lucas Gomes**
