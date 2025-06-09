# 🌐 Entendendo HTTP, GET e POST

Este documento explica de forma simples o que é **HTTP**, e como funcionam os métodos **GET** e **POST**, que são muito usados na comunicação entre o navegador (cliente) e os servidores web.

---

## 🧠 O que é HTTP?

**HTTP (HyperText Transfer Protocol)** é o protocolo que define as regras da comunicação entre o **cliente** (normalmente o navegador) e o **servidor** (onde o site ou sistema está hospedado).

### 🔁 Como funciona?

1. O cliente envia uma **requisição HTTP** ao servidor.
2. O servidor analisa a requisição.
3. O servidor envia de volta uma **resposta HTTP**, com um código de status e os dados solicitados.

---

## ⚙️ Métodos HTTP

Os métodos HTTP definem **o que o cliente quer fazer** com os dados no servidor.

Os mais usados são:

### ✅ GET

- Serve para **buscar informações**.
- Os dados são enviados **na URL**.
- Exemplo:
https://site.com/produtos?categoria=livros

- Não é seguro para informações sensíveis (porque tudo fica visível na URL).
- Ideal para consultas e pesquisas.

### 📨 POST

- Serve para **enviar dados** ao servidor.
- Os dados vão **no corpo da requisição**, não na URL.
- Usado em formulários como login, cadastro, envio de mensagens etc.
- Mais seguro que GET para informações confidenciais.

---

## 📊 Comparação entre GET e POST

| Característica       | GET                          | POST                          |
|----------------------|------------------------------|-------------------------------|
| Visibilidade         | Dados visíveis na URL        | Dados ocultos no corpo        |
| Segurança            | Menos seguro                 | Mais seguro                   |
| Tamanho de dados     | Limitado pela URL            | Pode enviar mais dados        |
| Usado para           | Consultas, buscas            | Enviar ou alterar dados       |
| Pode ser armazenado? | Sim (cacheável)              | Não (geralmente não cacheável) |

---

# 📡 HTTP Status Codes

Este documento lista e explica os principais **códigos de status HTTP** que indicam o resultado de uma requisição entre cliente e servidor.

---

## 🔵 1xx – Informativo

| Código | Significado             | Descrição |
|--------|--------------------------|-----------|
| 100    | Continue                 | O cliente pode continuar com a requisição. |
| 101    | Switching Protocols      | O servidor está mudando de protocolo conforme solicitado. |
| 102    | Processing               | O servidor recebeu e está processando a requisição (WebDAV). |

---

## 🟢 2xx – Sucesso

| Código | Significado             | Descrição |
|--------|--------------------------|-----------|
| 200    | OK                       | Requisição bem-sucedida. |
| 201    | Created                  | Recurso criado com sucesso. |
| 202    | Accepted                 | Requisição aceita, mas ainda não processada. |
| 204    | No Content               | Sucesso, porém sem retorno no corpo da resposta. |
| 206    | Partial Content          | Parte do conteúdo foi entregue (ex.: downloads por partes). |

---

## 🟡 3xx – Redirecionamento

| Código | Significado             | Descrição |
|--------|--------------------------|-----------|
| 301    | Moved Permanently        | Redirecionamento permanente. |
| 302    | Found                    | Redirecionamento temporário. |
| 304    | Not Modified             | Conteúdo não modificado (usado em cache). |
| 307    | Temporary Redirect       | Redirecionamento temporário mantendo o método. |
| 308    | Permanent Redirect       | Redirecionamento permanente mantendo o método. |

---

## 🔴 4xx – Erro do Cliente

| Código | Significado             | Descrição |
|--------|--------------------------|-----------|
| 400    | Bad Request              | Erro na sintaxe da requisição. |
| 401    | Unauthorized             | Requer autenticação. |
| 403    | Forbidden                | Acesso negado mesmo com autenticação. |
| 404    | Not Found                | Recurso não encontrado. |
| 405    | Method Not Allowed       | Método HTTP não permitido para o recurso. |

---

## ⚫ 5xx – Erro do Servidor

| Código | Significado             | Descrição |
|--------|--------------------------|-----------|
| 500    | Internal Server Error    | Erro interno no servidor. |
| 501    | Not Implemented          | Funcionalidade não implementada. |
| 502    | Bad Gateway              | O servidor recebeu uma resposta inválida. |
| 503    | Service Unavailable      | O servidor está temporariamente fora do ar. |
| 504    | Gateway Timeout          | Tempo limite de resposta excedido no gateway. |

---

> ℹ️ Baseado no conteúdo de [httpstatus.com.br](https://www.httpstatus.com.br/) e documentação oficial do HTTP.



