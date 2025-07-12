# 🧠 Hackathon DATAS – UFABC 2025

Este projeto foi desenvolvido no Hackathon do curso de Ciência de Dados da Universidade Federal do ABC (UFABC) com o objetivo de investigar desigualdades no acesso ao ensino superior e construir uma aplicação preditiva para estimar a nota e a chance de aprovação de candidatos ao SISU.

## 📁 Estrutura do Projeto

```
hackathon-datas-main/
├── data-analytics/                # Notebook com EDA e análise estatística
│   └── Análise.ipynb
├── ufabc-score-predictor/        # Núcleo técnico e aplicação
│   ├── dados/                    # Bases de dados brutas e tratadas
│   ├── modelos_xgboost/          # Modelos treinados (.pkl)
│   └── src/                      # Módulos do projeto
│       ├── application/          # App Streamlit
│       ├── data_prep/            # Pré-processamento
│       ├── train_models/         # Treinamento dos modelos
│       └── utils/                # Funções auxiliares
├── requirements.txt
└── README.md
```

---

## 🎯 Objetivo

- Analisar o perfil socioeconômico dos candidatos à UFABC via ENEM/SISU
- Visualizar desigualdades educacionais e raciais nos dados de ingresso
- Modelar a nota esperada por curso/modalidade
- Calcular a probabilidade de aprovação
- Criar uma aplicação interativa para simulação

---

## 📊 Dados Utilizados

- Dados da PROGRAD/UFABC: classificação e status de matrícula por curso
- Microdados do ENEM (INEP 2023)
- Dados abertos do SISU/MEC

---

## 🧪 Modelos e Técnicas Aplicadas

- Regressão com `XGBoost Regressor`
- Classificação com `XGBoost Classifier`
- GridSearchCV para tuning de hiperparâmetros
- Aplicação de sigmoide customizada para gerar uma **probabilidade de aprovação interpretável**
- Testes estatísticos (ANOVA, correlação) na análise exploratória
- Agrupamento por curso/modalidade para modelagem especializada

---

## 🚀 Aplicação Interativa

Interface desenvolvida com **Streamlit**:
- Entrada: modalidade, turno, campus e curso
- Saída: nota prevista, probabilidade de aprovação, feedback personalizado
- Uso de modelo real com base nos dados históricos da universidade

Para executar:
```bash
streamlit run ufabc-score-predictor/src/application/app_streamlit.py
```

---

## 📈 Análise Exploratória (EDA)

O notebook `data-analytics/Análise.ipynb` apresenta:
- Análise da nota por modalidade e turno
- Diferença entre ampla concorrência e cotas
- Visualizações de distribuição, corte, e classificação hipotética
- Reflexões críticas sobre desigualdade no acesso ao ensino superior

---

## 📄 Documentação Adicional

📘 **Apresentação oficial:**  
*Análise dos Fatores Socioeconômicos no Ingresso à UFABC (2025)*  
(Disponível em `/docs` ou linkado no repositório)

Inclui:
- Contexto institucional e político
- Metodologia passo a passo
- Resultados e visualizações explicadas
- Conclusões com base em dados e evidência estatística

---

## 🧰 Requisitos

Instalar dependências:

```bash
pip install -r requirements.txt
```

---

## 👥 Equipe

Desenvolvido por:
- Ana Carolina Siqueira Parra
- Heitor Hiroyuki Shirai
- Isac do Nascimento Vieira
- João Marco Jorge Franciscon

---

## 📌 Licença

Projeto de código aberto para fins educacionais, analíticos e sociais.

