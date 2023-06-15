# Instalação
lorem

## Intalado apartir do github

Para executar o projeto, é necessário seguir os seguintes passos:

Clonar o [repositório](https://github.com/claytonlovin/convutell) do projeto do Github.

Instalar as dependências através do comando

* `pip install -r requirements.txt`.

O API de integração é construída sobre o FastAPI 0.95.1 e o Python 3.7. Toda adaptação poderá ser realizada em verões subsequentes.

Executar o servidor web com o comando

* `uvicorn app:app --reload`. 

## Instalaçaõ local via Docker

Configure o arquivo Dockerfile para adequar a configuração ideal do seu ambiente. Esta implementação do projeto para a imagem docker está em desevolvimento, portanto cabe avaliar a viabilidade das configuração dispostas.

* `docker build -t nome_do_projeto:latest .`. 

Use o comando abaixo para inicar o seu container.

* `docker run -d -p 8000:8000 nome_do_projeto:latest`.

Optamos por utilizar o Supervisor para monitoramento e controle dos nossos processos. Tanto a API como Processo de ETL será monitorados pelo Supervisor. Toda a configuração será passada para o controle do Supervidor através do arquivo supervisord.conf.


```bash
[program:etl]
command=/opt/venv/bin/python /convutell/etl.py
directory=/convutell
autostart=true
autorestart=true
startretries=3
redirect_stderr=true
stdout_logfile=/convutell/logs/etl/etl.log
stdout_logfile_maxbytes=10MB

``` 