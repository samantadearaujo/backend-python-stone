##### Projeto Final - Central de Erros

Este repositório é para  o projeto final do AceleraDev da Codenation Python - Stone.

Depois de 10 semanas, ministrada por Élysson Mendes Rezende.

###### Objetivo

Em projetos modernos é cada vez mais comum o uso de arquiteturas baseadas em serviços ou microsserviços. Nestes ambientes complexos, erros podem surgir em diferentes camadas da aplicação (backend, frontend, mobile, desktop) e mesmo em serviços distintos. Desta forma, é muito importante que os desenvolvedores possam centralizar todos os registros de erros em um local, de onde podem monitorar e tomar decisões mais acertadas. Neste projeto vamos implementar um sistema para centralizar registros de erros de aplicações.

A arquitetura do projeto é formada por:

###### Backend - API

criar endpoints para serem usados pelo frontend da aplicação
criar um endpoint que será usado para gravar os logs de erro em um banco de dados relacional
a API deve ser segura, permitindo acesso apenas com um token de autenticação válido

###### Observações

Se a aceleração tiver ênfase no backend (Java, Python, C#, Go, PHP, etc) a equipe deve obrigatoriamente implementar a API. A implementação do frontend não é necessária

###### TOKEN

*Para gerar o token é necessaŕio usar: 
https://backend-python-stone.herokuapp.com/api/get_token

USERNAME: DEMO
PASSWORD: Dem@1234


###### Documentação API

Requisições para a API devem seguir os padrões:
| Método | Descrição | Exemplo
|---|---|---|
| `GET` | Retorna informações todos os registros | api/agents/ |
| `GET` | Retorna informações um registro | api/agents/:id |
| `POST` | Utilizado para criar um novo registro. | api/agents/ |

###### Publicação da API

    "agents": "https://backend-python-stone.herokuapp.com/api/agents/",
    "events": "https://backend-python-stone.herokuapp.com/api/events/",
    "levels": "https://backend-python-stone.herokuapp.com/api/levels/",
    "environment": "https://backend-python-stone.herokuapp.com/api/environment/"

![Captura de tela de 2020-07-20 20-06-58](https://user-images.githubusercontent.com/57687300/87976267-bc504780-cac4-11ea-9f15-41798e6880f2.png)
![Captura de tela de 2020-07-20 20-07-28](https://user-images.githubusercontent.com/57687300/87976269-bce8de00-cac4-11ea-9cb1-7685f444b066.png)

###### Estrutura 
```
├─ Procfile
├─ README.md
├─ api
│  ├─ __init__
│  ├─ serializers.py
│  ├─ urls.py
│  └─ views.py
├─ logs
│  ├─ __init__.py
│  ├─ admin.py
│  ├─ apps.py
│  ├─ migrations
│  │  ├─ 0001_initial.py
│  │  └─ __init__.py
│  ├─ models.py
│  ├─ tests.py
│  └─ views.py
├─ manage.py
├─ projectlogserros
│  ├─ __init__.py
│  ├─ asgi.py
│  ├─ settings.py
│  ├─ urls.py
│  └─ wsgi.py
├─ requirements.txt
└─ staticfiles

```
