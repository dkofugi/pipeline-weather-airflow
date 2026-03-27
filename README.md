# 🌦️ Pipeline de Dados Climáticos com Airflow

## 📌 Visão Geral

Este projeto consiste em um pipeline de dados automatizado utilizando Apache Airflow para extrair dados climáticos de uma API externa, processá-los e armazená-los em arquivos estruturados para análise.

O pipeline é executado semanalmente e organiza os dados em diferentes arquivos CSV, separando informações de temperatura e condições climáticas.

---

## ⚙️ Tecnologias Utilizadas

* Python
* Apache Airflow
* Pandas
* API REST (Visual Crossing Weather)

---

## 🔄 Fluxo do Pipeline

1. **Criação de Diretório**

   * Uma pasta é criada dinamicamente com base na data de execução.

2. **Extração de Dados**

   * Os dados climáticos são coletados de uma API externa.

3. **Transformação de Dados**

   * Os dados são processados e separados em:

     * Dados de temperatura
     * Dados de condições climáticas

4. **Carga de Dados**

   * Os dados processados são salvos em arquivos CSV.

---

## 📁 Estrutura do Projeto

```
├── dags/
│   └── dados_climaticos.py
├── README.md
└── requirements.txt
```

---

## 📊 Dados Gerados

O pipeline gera os seguintes arquivos:

* `dados_brutos.csv`
* `temperaturas.csv`
* `condicoes.csv`

---

## ⏱️ Agendamento

* Execução semanal (toda segunda-feira)
* Gerenciado pelo agendador do Airflow

---

## 🚀 Como Executar

1. Instale as dependências:

```
pip install -r requirements.txt
```

2. Inicie o Airflow:

```
airflow standalone
```

3. Acesse a interface do Airflow e ative a DAG

---

## 🔐 Segurança

A chave da API não deve ser armazenada diretamente no código.
Utilize variáveis de ambiente:

```
export API_KEY=sua_chave_aqui
```

---


## 👨‍💻 Autor

Danilo Kofugi
Futuro Engenheiro de Dados
