# cache-with-redis-and-letuce
Aplicação Spring com crud completo fazendo cache nos metodos GET utilizando de Redis e Lettuce. 

## API 
### Requisições
#### Post

```http
  POST http://localhost:8080/basiccrud/test-cache/
```


#### Get by id

```http
  GET http://localhost:8080/basiccrud/test-cache/${id}
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :------------------------- |
| `id` | `Long` | **OBRIGATORIO**. id que deseja obter |

#### Get by name

```http
  GET http://localhost:8080/basiccrud/test-cache/${name}
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | **OBRIGATORIO**. nome que deseja obter  |

#### Delete

```http
  DELETE http://localhost:8080/basiccrud/test-cache/${id}
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :-------------------------------- |
| `id`      | `Long` | **OBRIGATORIO**. id que deseja deletar  |

### Para rodar aplicação

#### Subir o container com redis
```bash
  docker run -it --name redis -p 6379:6379 redis:5.0.3
```

#### Para ver chaves salvas no redis ou deletar

  Conectar com container do redis:
```bash
  docker exec -it redis /bin/sh
```  
  Acessar CLI do Redis: 
```bash  
  redis-CLI
```
  (Caso adicione senha) Autentificar senha definida: 
```bash
  auth {INSIRA AQUI A SENHA}
```
  Lista as chaves criadas: 
```bash
  keys *
```
  Para deletar uma chave: 
```bash
  del "{INSIRA AQUI A SENHA DESEJADA}"
```
  
