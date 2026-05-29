# 📚 Caderno Temático com NotebookLM

## FastAPI na Prática: Construindo APIs Assíncronas com Python

## Sobre o Projeto

Durante meus estudos de desenvolvimento backend, desenvolvi uma API bancária utilizando FastAPI, PostgreSQL e SQLAlchemy. Enquanto construía o projeto, percebi que precisava consultar constantemente documentações, exemplos e conceitos relacionados a programação assíncrona, validação de dados e arquitetura de APIs REST.

Para organizar esse conhecimento, utilizei o NotebookLM como ferramenta de apoio aos estudos, centralizando documentações e realizando perguntas direcionadas aos problemas que surgiram durante o desenvolvimento.

O objetivo deste caderno é registrar o processo de aprendizado e consolidar os principais conceitos estudados.

---

# 🎯 Objetivos de Estudo

Ao iniciar este estudo, defini os seguintes objetivos:

* Entender como o FastAPI processa requisições assíncronas.
* Aprender a utilizar o SQLAlchemy Async.
* Compreender o papel do Pydantic na validação de dados.
* Explorar boas práticas para construção de APIs REST.
* Organizar um material de consulta para projetos futuros.

---

# 📖 Fontes Utilizadas

As fontes abaixo foram adicionadas ao NotebookLM para servir como base das consultas realizadas.

### FastAPI Official Documentation

https://fastapi.tiangolo.com

Documentação principal do framework.

### Pydantic Documentation

https://docs.pydantic.dev

Utilizada para compreender modelos e validações.

### SQLAlchemy Documentation

https://docs.sqlalchemy.org

Referência para integração com banco de dados.

### Python AsyncIO Documentation

https://docs.python.org/3/library/asyncio.html

Base para estudo de programação assíncrona.

### PostgreSQL Documentation

https://www.postgresql.org/docs/

Utilizada para consultas relacionadas ao banco de dados.

---

# 🤖 Engenharia de Prompts

Uma das partes mais interessantes do processo foi perceber que a qualidade das respostas dependia diretamente da qualidade das perguntas.

## Prompt 1

### Pergunta

Como funciona o async/await dentro do FastAPI e por que ele melhora a performance da aplicação?

### Resultado

O NotebookLM explicou o funcionamento do loop de eventos e como operações de I/O podem ser executadas sem bloquear outras requisições.

### Aprendizado

Entendi que utilizar async não deixa o código "mais rápido", mas permite que a aplicação atenda mais requisições simultaneamente.

---

## Prompt 2

### Pergunta

Qual a diferença prática entre Session e AsyncSession no SQLAlchemy?

### Resultado

Recebi uma explicação detalhada sobre o funcionamento de ambas e exemplos de uso.

### Dificuldade Encontrada

Inicialmente a resposta ficou muito teórica.

### Ajuste Realizado

Reformulei para:

"Explique Session e AsyncSession considerando uma API FastAPI conectada ao PostgreSQL."

A resposta ficou muito mais próxima da minha realidade.

---

## Prompt 3

### Pergunta

Quais erros são mais comuns ao utilizar SQLAlchemy assíncrono?

### Resultado

Foram apresentados problemas relacionados ao gerenciamento de conexões, await ausente e sessões abertas incorretamente.

### Aplicação Prática

Consegui identificar erros semelhantes que aconteceram durante o desenvolvimento da API bancária.

---

## Prompt 4

### Pergunta

Analise esta arquitetura e sugira melhorias para escalabilidade.

### Resultado

Recebi sugestões sobre separação de camadas, organização dos schemas e reutilização de dependências.

### Observação

Esse foi um dos usos mais úteis do NotebookLM, pois as respostas estavam diretamente relacionadas às fontes carregadas.

---

# 📑 Miniguia de Estudos

## O que é FastAPI?

FastAPI é um framework moderno para desenvolvimento de APIs utilizando Python e tipagem estática.

Principais vantagens:

* Alta performance
* Documentação automática
* Validação de dados integrada
* Suporte nativo a operações assíncronas
* Facilidade de manutenção

---

## Conceitos Mais Importantes

### Rotas

São os endpoints responsáveis por receber requisições HTTP.

Exemplo:

```python
@app.get("/accounts")
async def list_accounts():
    return []
```

### Pydantic

Responsável pela validação dos dados recebidos e enviados pela API.

Exemplo:

```python
class UserCreate(BaseModel):
    name: str
    email: str
```

### Async/Await

Permite que operações de banco de dados e serviços externos não bloqueiem outras requisições.

### Dependency Injection

Facilita a reutilização de componentes como autenticação e conexão com banco.

---

# 📚 Glossário

## API REST

Arquitetura baseada em recursos acessados através do protocolo HTTP.

## Endpoint

URL disponibilizada pela API.

## Pydantic

Biblioteca utilizada para validação de dados.

## AsyncIO

Biblioteca nativa do Python para programação assíncrona.

## ORM

Ferramenta que permite trabalhar com banco de dados utilizando objetos Python.

## SQLAlchemy

ORM utilizado para comunicação com o PostgreSQL.

## JWT

Método amplamente utilizado para autenticação baseada em tokens.

---

# 🚀 Prompts Reutilizáveis

Durante os estudos, alguns prompts produziram resultados muito úteis e podem ser reutilizados futuramente.

### Revisão Técnica

Explique este conceito considerando uma aplicação FastAPI em produção.

### Resolução de Problemas

Quais erros comuns podem ocorrer neste cenário e como evitá-los?

### Arquitetura

Analise esta estrutura de projeto e sugira melhorias seguindo boas práticas.

### Banco de Dados

Explique como ocorre a comunicação entre FastAPI, SQLAlchemy e PostgreSQL.

### Preparação para Entrevistas

Gere perguntas de entrevista para desenvolvedor backend Python sobre este tema.

---

# Conclusão

A experiência com o NotebookLM mostrou que a ferramenta é mais útil quando utilizada como apoio ao raciocínio e não apenas como geradora de respostas.

Ao concentrar documentações e materiais de referência em um único ambiente, foi possível obter explicações contextualizadas para dúvidas reais que surgiram durante o desenvolvimento da API bancária.

O resultado foi um processo de estudo mais organizado e uma compreensão mais sólida dos conceitos envolvidos na construção de APIs modernas com FastAPI.
