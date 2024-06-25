# API para tradução HTML - Projeto Pessoal

API para tradução para o inglês e português ou vice-versa. A API foi desenvolvida em Python, utilizando a biblioteca Argos-Translate para realizar a tradução e a biblioteca FastAPI para criar a API.

A API foi desenvolvida para um projeto pessoal, onde eu precisava traduzir algumas partes do meu portfólio de forma dinâmica. Pórem notei que para conseguir rodar a API consumiria muita CPU, então decidi não utilizar a API e fui procurar por outra solução que foi a DeepL.

Quando mais rápido for a CPU do seu dispositivo, mais rápido será a tradução, então só recomendo com textos pequenos.

## Aviso - Antes de rodar a aplicação

É necessário fazer o download dos pacotes de traduções e mover eles para a pasta `languages`. Os pacotes podem ser abaixados neste [link](https://drive.google.com/drive/folders/11wxM3Ze7NCgOk_tdtRjwet10DmtvFu3i).

Os pacotes de tradução são:

- `en-pt.argosmodel` para tradução do inglês para português
- `pt-en.argosmodel` para tradução do português para inglês

## Dependências

- Argos-Translate
- FastAPI
- Uvicorn

## Rotas

A API possui as seguintes rotas:

- `/translate`: recebe o parametro `source` e o `target` com o idioma de origem e o idioma de destino, e ainda o parametro `elements_text` com um elemento ou uma lista de elementos para serem traduzidos.
- `/helloworld`: retorna uma mensagem 'Hello World!'.

## Como rodar a aplicação

Para rodar a aplicação, é necessário ter o Python instalado e instalar as dependências do projeto. Para instalar as dependências, execute o comando:

```bash
pip install -r requirements.txt
```

Depois de instalar as dependências, descomente as linhas abaixo no arquivo `main.py`:

```python
# if __name__ == "__main__":
#     import uvicorn

#     uvicorn.run(app, host="localhost", port=8080)
```

e depois execute o comando:

```bash
python3 main.py
```

A aplicação estará rodando em `http://localhost:8080`.
