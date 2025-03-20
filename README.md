Consultas SQL - Locadora de Carros


Este projeto contém uma série de consultas SQL realizadas sobre o banco de dados locadora, hospedado em uma instância MySQL no Google Cloud Platform (GCP).

O objetivo do projeto é realizar a análise dos dados de clientes, carros e aluguéis da locadora por meio de consultas SQL.

1. Pré-Requisitos
2. 
Antes de rodar as consultas, você precisará dos seguintes pré-requisitos:

Conta no Google Cloud Platform (GCP) com instância de MySQL configurada.

MySQL configurado e acessível na instância GCP.

Python 3.x e pacotes necessários instalados no seu ambiente local ou no Google Colab.

Biblioteca mysql-connector-python instalada para Python, caso esteja utilizando um ambiente Python local ou Colab.
Instalação dos pacotes

Para instalar as dependências, você pode usar o seguinte comando:



pip install mysql-connector-python pandas

2. Configuração de Conexão MySQL no Google Cloud
3. 
2.1. Obtenção do IP da Instância MySQL
   
No Console do Google Cloud, acesse a seção "Instâncias de Banco de Dados".

Localize a instância de banco de dados MySQL que você deseja conectar.

Copie o IP público ou IP interno (dependendo da sua configuração de rede) da instância.

2.2. Credenciais de Conexão

Certifique-se de ter as credenciais de acesso, incluindo:

Usuário: O nome de usuário do MySQL (geralmente root por padrão).

Senha: A senha associada ao seu usuário MySQL.

Database: O nome do banco de dados MySQL que você deseja acessar (exemplo: locadora).

3. Configuração da Conexão com MySQL no Python/Colab
4. 
No código Python/Colab, a conexão com o banco de dados MySQL pode ser feita com a biblioteca mysql-connector-python.
Aqui está um exemplo de código de

configuração de conexão no seu ambiente Python:


Exemplo de Conexão MySQL no Google Colab/Python

import mysql.connector
import pandas as pd

# Dados de conexão
host = '34.170.104.203'  # Substitua pelo IP da sua instância MySQL na GCP
user = 'root'  # Substitua pelo seu nome de usuário MySQL
password = ''  # Substitua pela sua senha MySQL
database = 'locadora'  # Nome do seu banco de dados

# Conectando-se ao banco de dados
connection = mysql.connector.connect(
    host=host,
    user=user,
    password=password,
    database=database  # Nome do banco de dados
)

# Criando o cursor
cursor = connection.cursor()



Conclusão
Este projeto foi desenvolvido para fornecer insights sobre os dados da locadora de carros e ajudar a entender o comportamento dos clientes e carros de uma locadora por meio de consultas SQL.

O uso de Google Cloud Platform para hospedar o banco de dados MySQL e Google Colab para execução das consultas SQL é uma maneira eficaz de realizar essa análise em nuvem.



