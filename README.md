# 📊 Sistema Preditivo e Matriz de Risco - IFES

Este repositório contém o **código-fonte e a metodologia de Extração, Transformação e Carga (ETL)** desenvolvidos para o **Trabalho de Conclusão de Curso (TCC)**.  

O objetivo do projeto é **mitigar a assimetria informacional enfrentada por candidatos ao Instituto Federal do Espírito Santo (IFES)** através de **análise de dados e projeções estatísticas**.

---

# 🖥 Demonstração Visual

## 1. Dashboard de Regressão Linear

<img width="998" height="823" alt="image" src="https://github.com/user-attachments/assets/d0412363-59ef-4b07-a9b0-706e69dbb8dd" />

<img width="998" height="826" alt="image" src="https://github.com/user-attachments/assets/05c9aa52-0b68-4023-a540-581f7db677ae" />

<img width="1018" height="822" alt="image" src="https://github.com/user-attachments/assets/fa9c7eb1-9032-47a6-b25c-a8b5d3f5bbc5" />

<img width="1028" height="825" alt="image" src="https://github.com/user-attachments/assets/62e3f42b-d201-4097-825b-7f8182532ee3" />

---

## 2. Matriz de Oportunidade e Risco

<img width="991" height="829" alt="image" src="https://github.com/user-attachments/assets/0bbb2444-2794-4b58-bae3-98df8e8626be" />

---

# 🧰 Tecnologias Utilizadas

## Engenharia de Dados (ETL)

- Python 3.10+
- pandas *(Manipulação e Data Wrangling)*
- pdfplumber / tabula-py *(Extração de dados não estruturados)*
- psycopg2 *(Conexão com PostgreSQL)*

## Banco de Dados (Nuvem)

- Supabase *(BaaS PostgreSQL)*

## Front-end (Aplicação Web)

- HTML5  
- Vanilla JavaScript *(Lógica e Regressão Linear no cliente)*  
- Tailwind CSS *(Estilização responsiva)*  
- Chart.js *(Visualização de Dados e Matriz de Dispersão)*  

---

# 🏗 Arquitetura da Solução

O projeto adota uma **arquitetura End-to-End**, dividida em três camadas principais.

## Data Pipeline (ETL em Python)

- Extração de dados não estruturados de **dezenas de ficheiros PDF oficiais (editais de 2022 a 2025)**.
- Limpeza e normalização (*Data Wrangling*) utilizando **pandas** e **Expressões Regulares (regex)**.
- Geração de uma **"Tabela de Ouro"** contendo **KPIs de desempenho normalizados para a escala atual de 400 pontos**.

## Cloud Database (BaaS)

Os dados higienizados são enviados via **script Python** para um banco de dados relacional **PostgreSQL** alojado na plataforma **Supabase**.

## Front-end Analítico (Single Page Application)

Uma interface Web intuitiva que:

- Consome os dados do **Supabase** via chamadas assíncronas
- Aplica **algoritmos de Regressão Linear Simples (OLS)** no lado do cliente
- Utiliza a **distribuição t de Student (95% de confiança)** para desenhar margens de erro realistas *(Cenários Otimista e Pessimista)*
- Renderiza uma **Matriz Multifatorial de Risco vs Oportunidade**, agrupando cursos em **4 quadrantes estratégicos**

---

# 📁 Estrutura do Repositório

```
📦 ifes-analise-preditiva
 ┣ 📜 microdados_ifes.ipynb   # Script de extração e tratamento (ETL) em Python
 ┣ 📜 index.html              # Aplicação Web Front-end (Single Page Application)
 ┗ 📜 README.md               # Documentação do projeto
```

---

# 🚀 Como Visualizar o Simulador (Front-end)

A componente visual do projeto é **totalmente Serverless**, não sendo necessário servidor local.

## 1. Faça o clone do repositório

```bash
git clone https://github.com/davicucco-cod/ifes-analise-preditiva.git
```

## 2. Abra o simulador

Abra o ficheiro **index.html** em qualquer navegador Web moderno:

- Google Chrome
- Firefox
- Microsoft Edge

A aplicação ligar-se-á automaticamente à **API pública de leitura do Supabase**.

---

# 📊 Fonte dos Dados

Todos os dados brutos processados neste projeto são **de domínio público**, originários dos **Editais de Resultados Finais dos Processos Seletivos (Cursos Técnicos Integrados ao Ensino Médio)** publicados anualmente no portal oficial do **Instituto Federal do Espírito Santo (IFES)**.

---

# 📚 Reprodutibilidade e Ciência Aberta

A disponibilização deste código visa garantir **total transparência metodológica** e encorajar a **Pesquisa Reprodutível no âmbito académico**.

Todos os scripts matemáticos para o cálculo de:

- desvio padrão
- regressão linear

encontram-se **expostos, auditáveis e documentados no ficheiro Front-end**.

---

# 📄 Licença

Este projeto é disponibilizado sob a **Licença MIT**.

Sinta-se à vontade para:

- clonar
- modificar
- distribuir

desde que **mantidos os devidos créditos ao autor original**.

---

# 👨‍💻 Autor

**Davi Duarte Cucco**

🎓 Instituição: Faculdade Descomplica  

🔗 LinkedIn:  
[https://www.linkedin.com/in/davi-duarte-cucco/](https://www.linkedin.com/in/davi-duarte-cucco-8b272a238/)
