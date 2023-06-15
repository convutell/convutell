# Bemvindo ao convutell

Este é o guia de documentação do Convutell, uma ferramenta de automatização de scripts Python e SQL, desenvolvida utilizando as tecnologias Python, Docker, FastAPI e MongoDB. O Convutell é ideal para tarefas de engenharia de dados, RPA (Automação de Processos Robóticos) e ETL (Extração, Transformação e Carga).

## Comando para executar localmente

* `docker build -t nome_do_projeto:latest .` -  Constrói a imagem do projeto.
* `docker run -d -p 8000:8000 nome_do_projeto:latest` - Inicia o servidor de documentação com recarregamento em tempo real.

## Estrutura do projeto

    Dockerfile    # The configuration file docker.
    convutell/
        logs/
        config/
        app.py
        service.py  # Application execution configuration file.
        ...      
Para obter informações detalhadas sobre o Convutell e como usá-lo, consulte a documentação completa em mkdocs.org.