# Criptografador Seguro de Arquivos (Python)

Este é um script simples em Python para criptografar e descriptografar arquivos em uma pasta específica usando a biblioteca `cryptography` (Fernet) e derivação de chave segura (PBKDF2HMAC).

## Para Testar

Siga os passos abaixo para testar o script.

### 1. Pré-requisitos

Você precisa ter o Python instalado e as bibliotecas necessárias.

```bash
# Instale a biblioteca cryptography
pip install cryptography
```

### 2. Configuração do Script

1.  Salve o código otimizado (por exemplo, `gryphony.py`) em uma pasta.
2.  **Crie uma pasta** chamada `files` no mesmo diretório do script.
3.  Coloque alguns arquivos de teste (ex: `.txt`, `.jpg`, `.pdf`) dentro da pasta `files`.

### 3. Execução

Execute o script pelo terminal:

```bash
python gryphony.py
```

### 4. Menu de Opções

O script apresentará um menu:

1.  **Configurar senha (primeira vez):**
    *   **IMPORTANTE:** Você deve usar esta opção na primeira execução.
    *   O script pedirá para você criar e confirmar uma senha.
    *   Ele criará dois arquivos ocultos (`.encryption_key.bin` e `.salt.bin`) que são essenciais para a criptografia.

2.  **Criptografar arquivos:**
    *   O script pedirá a senha.
    *   Ele listará os arquivos elegíveis na pasta `files`.
    *   Após a confirmação, ele criptografará os arquivos e adicionará o sufixo `.encrypted` ao nome. Os arquivos originais serão deletados.

3.  **Descriptografar arquivos:**
    *   O script pedirá a senha.
    *   Ele listará os arquivos com o sufixo `.encrypted`.
    *   Após a descriptografia, ele removerá o sufixo e deletará os arquivos criptografados.

4.  **Sair**

---

**Dica:** Para testar, use a Opção 1, depois a Opção 2 para criptografar, e por fim a Opção 3 para descriptografar. Se a senha estiver errada, o script informará o erro.
