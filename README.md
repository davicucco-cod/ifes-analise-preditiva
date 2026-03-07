# 📊 Sistema Preditivo e Matriz de Risco - IFES

Este repositório contém o **código-fonte e a metodologia de Extração, Transformação e Carga (ETL)** desenvolvidos para o **Trabalho de Conclusão de Curso (TCC)**.

O objetivo do projeto é **mitigar a assimetria informacional enfrentada por candidatos ao Instituto Federal do Espírito Santo (IFES)** através de **análise de dados e projeções estatísticas**, permitindo estimar notas de corte e identificar oportunidades estratégicas de candidatura.

---

# 🖥️ Demonstração Visual

## 📈 Dashboard de Regressão Linear

<img width="998" height="823" alt="image" src="https://github.com/user-attachments/assets/d0412363-59ef-4b07-a9b0-706e69dbb8dd" />

<img width="998" height="826" alt="image" src="https://github.com/user-attachments/assets/05c9aa52-0b68-4023-a540-581f7db677ae" />

<img width="1018" height="822" alt="image" src="https://github.com/user-attachments/assets/fa9c7eb1-9032-47a6-b25c-a8b5d3f5bbc5" />

<img width="1028" height="825" alt="image" src="https://github.com/user-attachments/assets/62e3f42b-d201-4097-825b-7f8182532ee3" />

---

## 🎯 Matriz de Oportunidade e Risco

<img width="991" height="829" alt="image" src="https://github.com/user-attachments/assets/0bbb2444-2794-4b58-bae3-98df8e8626be" />

---

# 🧰 Tecnologias Utilizadas

## Engenharia de Dados (ETL)

- Python 3.10+
- pandas (Manipulação e Data Wrangling)
- pdfplumber / tabula-py (Extração de dados não estruturados)
- psycopg2 (Conexão com PostgreSQL)

## Banco de Dados (Nuvem)

- Supabase (BaaS PostgreSQL)

## Front-end (Aplicação Web)

- HTML5
- Vanilla JavaScript
- Tailwind CSS
- Chart.js

---

# 🏗️ Arquitetura da Solução

O projeto segue uma arquitetura **End-to-End**, dividida em três camadas principais.

## 1️⃣ Data Pipeline (ETL em Python)

- Extração de dados não estruturados de **dezenas de arquivos PDF oficiais** (editais de 2022 a 2025).
- Limpeza e normalização utilizando **pandas** e **expressões regulares (regex)**.
- Geração de uma **Tabela de Ouro** contendo KPIs normalizados para a **escala atual de 400 pontos**.

## 2️⃣ Cloud Database (BaaS)

Os dados processados são enviados via script Python para um banco de dados relacional **PostgreSQL hospedado na plataforma Supabase**.

## 3️⃣ Front-end Analítico (Single Page Application)

Interface web interativa que:

- Consome dados via **API pública do Supabase**
- Aplica **Regressão Linear Simples (OLS)** no lado do cliente
- Utiliza **distribuição t de Student (95% de confiança)** para estimar margens de erro
- Simula **cenários otimista e pessimista**
- Renderiza uma **Matriz Multifatorial de Risco vs Oportunidade**, agrupando cursos em **4 quadrantes estratégicos**

---

# 📁 Estrutura do Repositório

```
📦 ifes-analise-preditiva
 ┣ README.md
 ┃  Documentação do projeto
 ┣ microdados_ifes.ipynb
 ┃  Scripts de extração e tratamento (ETL)
 ┗ index.html
    Aplicação Web (Single Page Application)
```

---

# 🚀 Como Visualizar o Simulador

A aplicação é **100% serverless**, não sendo necessário servidor local.

## 1. Clone o repositório

```bash
git clone https://github.com/SEU_USUARIO/ifes-analise-preditiva.git
```

## 2. Acesse a pasta do projeto

```bash
cd ifes-analise-preditiva
```

## 3. Abra o simulador no navegador

Abra o arquivo **index.html** em qualquer navegador moderno:

- Google Chrome  
- Firefox  
- Microsoft Edge  

A aplicação conectará automaticamente à **API pública de leitura do Supabase**.

---

# 📊 Fonte dos Dados

Todos os dados utilizados neste projeto são **dados públicos**, provenientes dos:

**Editais de Resultados Finais dos Processos Seletivos  
Cursos Técnicos Integrados ao Ensino Médio**

Publicados no portal oficial do **Instituto Federal do Espírito Santo (IFES)**.

---

# 🔬 Reprodutibilidade e Ciência Aberta

Este repositório foi disponibilizado com o objetivo de:

- Garantir **transparência metodológica**
- Promover **pesquisa reprodutível**
- Permitir auditoria dos **métodos estatísticos utilizados**

Os cálculos de:

- Desvio padrão
- Regressão linear
- Intervalos de confiança

estão totalmente documentados e expostos no código do **front-end**.

---

# 📄 Licença

Este projeto está licenciado sob a **Licença MIT**.

Você pode:

- Clonar
- Modificar
- Distribuir

Desde que **mantidos os créditos ao autor original**.

---

# 👨‍💻 Autor

**Davi Duarte Cucco**

🎓 Faculdade Descomplica  

🔗 LinkedIn  
https://www.linkedin.com/in/davi-duarte-cucco/
