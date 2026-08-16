<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=2E86C1&center=true&vCenter=true&width=500&lines=Gabriel+Damasceno;Engenharia+de+Dados;Pipelines+end-to-end+%7C+Python+%2B+SQL" alt="Typing SVG" />

Análise e Desenvolvimento de Sistemas — Fatec Mogi das Cruzes · São Paulo, Brasil

</div>

4+ anos atuando em ecossistemas de dados para tomada de decisão financeira e análise de risco — motores de decisão de crédito, validação em produção e shadow mode. Hoje aplico essa vivência para construir pipelines de dados end-to-end e automações com IA generativa aplicadas a problemas reais de negócio.

<br>

## 🚀 Projeto em destaque

### CâmbioTech — Reconciliação de Ordens FX vs. Mercado *(link a atualizar)*

Pipeline de dados end-to-end que simula o problema de uma corretora de câmbio: reconciliar ordens executadas internamente contra taxas oficiais de mercado para detectar anomalias de precificação e exposição cambial não coberta, dentro de janelas de reporte diário.

```mermaid
flowchart LR
    A[Alpha Vantage API] --> C[Python · Ingestão]
    B[(Fonte Transacional)] --> C
    C --> D[(MinIO · Bronze)]
    D --> E[dbt · Staging]
    E --> F[dbt · Mart]
    F --> G[(Postgres)]
    H[Airflow] -.orquestra.-> C
    H -.orquestra.-> E
    H -.orquestra.-> F
```

- **Ingestão:** dois serviços em Python — consumo de API externa real (Alpha Vantage, com controle de rate limit e quota) e leitura de fonte transacional imperfeita
- **Bronze/Landing zone:** MinIO (S3-compatible), populado via `docker compose up`
- **Transformação:** modelagem em camadas (staging → mart) com dbt, incluindo testes de qualidade de dados
- **Orquestração:** DAG no Airflow cobrindo o fluxo completo de ingestão a mart
- **CI/CD:** GitHub Actions com `dbt seeds` para proteger a quota da API em pipeline de CI
- **Resiliência:** simulação de incidente de produção (breaking change na API) resolvida via branch de hotfix, com plano de rollback documentado

<div align="left">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" />
<img src="https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white" />
<img src="https://img.shields.io/badge/Postgres-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MinIO-C72E49?style=for-the-badge&logo=minio&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
</div>

<br>

### Alertas Inteligentes — LLM + Automação de Observabilidade

Automação que integra Claude (LLM) via Make.com para traduzir alertas técnicos do Datadog em resumos claros e acionáveis no Slack — reduzindo o tempo de triagem de incidentes ao filtrar ruído e destacar o que realmente exige ação da equipe.

<div align="left">
<img src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/Make.com-6D00CC?style=for-the-badge&logo=make&logoColor=white" />
<img src="https://img.shields.io/badge/Datadog-632CA6?style=for-the-badge&logo=datadog&logoColor=white" />
<img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" />
</div>

<br>

## 🛠️ Stack

<div align="left">
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Redshift-8C4FFF?style=for-the-badge&logo=amazonredshift&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" />
<img src="https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white" />
<img src="https://img.shields.io/badge/Postgres-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MinIO-C72E49?style=for-the-badge&logo=minio&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
</div>

<br>

## 📊 Atividade

<div align="left">
<img src="https://github-readme-stats.vercel.app/api?username=Damazordon&show_icons=true&theme=transparent&hide_border=true&count_private=true" height="165" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Damazordon&layout=compact&theme=transparent&hide_border=true" height="165" />
</div>

<br>

## 📬 Contato

<div align="left">
<a href="https://www.linkedin.com/in/damazordon/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:gabrielgabridma@gmail.com.br"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</div>
