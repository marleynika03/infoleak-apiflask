📖 Sobre o Projeto

Este projeto é um protótipo de um servidor Flask para simular a coleta de dados em um ambiente de laboratório de segurança ofensiva (Pentest), com fins exclusivamente educacionais.

A ideia é criar uma API REST que receba dados como user, hostname, IP, simulando o comportamento de ferramentas utilizadas em laboratórios de Pentest, onde uma aplicação maliciosa (spyware) envia dados capturados da máquina para esse servidor.

⚠️ Aviso de Ética e Responsabilidade

Este projeto não contém nem promoverá código de spyware real, shells reversos ou ferramentas ofensivas funcionais.

O propósito é educacional, voltado ao estudo de APIs REST, testes com Pytest e práticas simuladas de coleta de dados em laboratórios isolados.

⚙️ Tecnologias Utilizadas

Python 3.13.0

Flask

Flask SQLAlchemy

PostgreSQL 9.5+

Pytest

Insomnia (para testes manuais)

Git e GitHub

Ngrok (opcional, para testes externos)

🚀 Como Funciona

O servidor roda um endpoint /leak que aceita requisições POST contendo informações da máquina.

Os dados são validados e armazenados em um banco PostgreSQL.

A API também oferece endpoints para listar e deletar registros.

Os testes automatizados garantem que os endpoints funcionem corretamente.

🖥️ Instalação e Execução
1. Clone o repositório

git clone https://github.com/marleynika03/infoleak-apiflask.git


2. Crie e ative o ambiente virtual
   
python -m venv venv

venv\Scripts\activate

4. Instale as dependências
   
pip install -r requirements.txt

6. Configure o PostgreSQL em database.py
   
app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql://usuario:senha@localhost:5432/infodb'

8. Execute o servidor
   
flask run

📡 Endpoints da API

Método	Rota	Descrição

POST	/leak	Recebe dados coletados e armazena

GET	/dados	Retorna todos os dados armazenados

DELETE	/apagar/<id>	Apaga um dado específico por ID

🧪 Testes Automatizados

Testes localizados no arquivo tests/test_endpoints.py.

Para rodar:
pytest tests\test_endpoints.py

Casos testados:

POST /leak: Verifica envio e resposta correta

GET /dados: Verifica listagem de registros

DELETE /apagar/<id>: Testa exclusão com confirmação de retorno

🕵️ Possíveis Casos de Uso

Simulação de coleta de dados em ambientes de laboratório de Pentest

Demonstração prática de APIs REST com Flask

Treinamento de testes com Pytest e integração com PostgreSQL

📝 Licença

Este projeto está sob a licença MIT. Sinta-se livre para estudar, modificar e reutilizar com os devidos créditos.

### ⚖️ Termos de uso

Este projeto é fornecido **exclusivamente para fins educacionais**. O autor **não se responsabiliza** pelo uso indevido deste código. O uso fora de ambientes autorizados ou controlados pode constituir crime, conforme a legislação aplicável.
