# boock
Gerenciamento de API biblioteca pessoal

"""
This function takes in a list of numbers and returns the sum of all the numbers in the list.

Parameters:
- numbers (list): A list of numbers.

Returns:
- sum (int): The sum of all the numbers in the list.
"""
# API de Gerenciamento de Livros

Esta API permite gerenciar uma biblioteca pessoal de livros. Ela fornece endpoints para adicionar, listar, atualizar e excluir livros.

## Adicionar um Livro

Endpoint: `/livros/adicionar`

Método: `POST`

Parâmetros:
- `titulo` (string): O título do livro.
- `autor` (string): O autor do livro.
- `ano` (int): O ano de publicação do livro.

Exemplo de requisição:
```python
import requests

url = "http://localhost:5000/livros/adicionar"
payload = {
    "titulo": "O Senhor dos Anéis",
    "autor": "J.R.R. Tolkien",
    "ano": 1954
}
response = requests.post(url, json=payload)
print(response.json())
```

## Listar Livros

Endpoint: `/livros`

Método: `GET`

Exemplo de requisição:
```python
import requests

url = "http://localhost:5000/livros"
response = requests.get(url)
print(response.json())
```

## Atualizar um Livro

Endpoint: `/livros/{id}`

Método: `PUT`

Parâmetros:
- `id` (int): O ID do livro a ser atualizado.
- `titulo` (string): O novo título do livro.
- `autor` (string): O novo autor do livro.
- `ano` (int): O novo ano de publicação do livro.

Exemplo de requisição:
```python
import requests

url = "http://localhost:5000/livros/1"
payload = {
    "titulo": "Novo Título",
    "autor": "Novo Autor",
    "ano": 2022
}
response = requests.put(url, json=payload)
print(response.json())
```

## Excluir um Livro

Endpoint: `/livros/{id}`

Método: `DELETE`

Parâmetros:
- `id` (int): O ID do livro a ser excluído.

Exemplo de requisição:
```python
import requests

url = "http://localhost:5000/livros/1"
response = requests.delete(url)
print(response.json())
```

    ```