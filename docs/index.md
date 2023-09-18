# Bemvindo ao convutell

![Texto alternativo](assets/docs/banner1.png)


Este é o guia de documentação do Convutell, uma ferramenta de automatização de scripts Python e SQL, desenvolvida utilizando as tecnologias Python, Docker, FastAPI e MongoDB. O Convutell é ideal para tarefas de engenharia de dados, RPA (Automação de Processos Robóticos) e ETL (Extração, Transformação e Carga).

## Comando para executar localmente

* `sudo docker-compose up -d` -  Construir o container com base no arquivo docker-compose.yml.

## Estrutura do projeto

    Dockerfile    # The configuration file docker.
    convutell/
        logs/
        config/
        app.py
        service.py  # Application execution configuration file.
        ...      
Para obter informações detalhadas sobre o Convutell e como usá-lo, consulte a documentação completa em mkdocs.org.