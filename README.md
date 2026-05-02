# 🎮 Pipeline ETL: Campeões de League of Legends

Este projeto realiza um processo de **ETL (Extract, Transform, Load)** para coletar dados atualizados dos campeões de *League of Legends* a partir da API da Riot Games (Data Dragon), processá-los utilizando Pandas e armazená-los em um banco de dados relacional MariaDB.

---

## 🛠 Tecnologias Utilizadas

* **Linguagem:** Python 3.9+
* **Manipulação de Dados:** Pandas
* **Conectividade:** SQLAlchemy, PyMySQL
* **Banco de Dados:** MariaDB
* **API:** Riot Games Data Dragon API

## 🚀 O Pipeline

O processo é dividido em três etapas claras:

1. **Extração (Extract):** Coleta da última versão disponível do jogo e requisição dos dados de todos os campeões em formato JSON.

2. **Transformação (Transform):**
   - Achatamento (flattening) dos dados aninhados.
   - Limpeza de colunas desnecessárias.
   - Tradução de terminologias (Tags de campeões e nomes de colunas).
   - Conversão de tipos de dados para garantir compatibilidade com SQL.

3. **Carga (Load):** Ingestão dos dados estruturados em uma tabela no banco de dados MariaDB (`campeoes`).

## 📋 Como Executar

### Pré-requisitos

Certifique-se de ter o Python instalado e um servidor MariaDB rodando.

### Instalação

1. Clone o repositório:
   ```bash
   git clone [https://github.com/GChandrone/lol-champion-etl-pipeline.git](https://github.com/GChandrone/lol-champion-etl-pipeline.git)
   cd lol-champion-etl-pipeline

2. Instale as dependências:
   ```bash
   pip install pandas sqlalchemy pymysql python-dotenv requests

3. Configure o arquivo .env:

   Crie um arquivo chamado .env na raiz do projeto com suas credenciais:
   ```bash
   DB_USER=seu_usuario
   DB_SENHA=sua_senha
   DB_HOST=localhost
   DB_PORT=3306
   DB_NAME=nome_do_seu_banco

5. Execute o script:
   ```bash
   python ETL.ipynb

## 📊 Objetivo

Este dataset estruturado permite a criação de dashboards no Power BI ou Tableau para análises de balanceamento, comparação de atributos de campeões (vida, dano, dificuldade) e muito mais.

Desenvolvido por Gabriel da Cunha
