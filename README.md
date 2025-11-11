# Transcritor de Imagens (OCR) para DOCX

Este é um script Python que automatiza o processo de extração de texto de um conjunto de imagens (como páginas de um livro escaneadas) e compila todo o texto em um único arquivo `.docx`. O script utiliza a API **Google Cloud Vision** para realizar o Reconhecimento Óptico de Caracteres (OCR).

## Funcionalidades

* Descompacta um arquivo `.zip` contendo as imagens.
* Ordena as imagens para manter a sequência correta.
* Envia cada imagem para a API do Google Cloud Vision (`document_text_detection`).
* Salva o texto extraído de todas as páginas em um único arquivo `.docx`, com separadores de página.

---

## 🛠️ Requisitos

* Python 3.8+
* Uma conta no Google Cloud Platform com a API Cloud Vision ativada.
* Um arquivo de credencial JSON de uma Conta de Serviço.
* As seguintes bibliotecas Python:
    * `google-cloud-vision`
    * `python-docx`

---

## ⚙️ Configuração

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/lagame/TranscritorPDF2TXT.git](https://github.com/lagame/TranscritorPDF2TXT.git)
    cd TranscritorPDF2TXT
    ```

2.  **Crie e ative um ambiente virtual:**
    ```bash
    # Criar o venv
    python -m venv venv
    
    # Ativar no PowerShell (Windows)
    .\venv\Scripts\Activate.ps1
    ```

3.  **Instale as dependências:**
    ```bash
    pip install google-cloud-vision python-docx
    ```

4.  **Adicione os Arquivos:**
    * **Credencial:** Coloque seu arquivo `.json` de credencial do Google Cloud na raiz do projeto (ex: `chave-servico.json`).
    * **Imagens:** Coloque o arquivo `.zip` com suas imagens na raiz do projeto e renomeie-o para `meu_livro.zip` (ou atualize a variável `zip_file_path` no script).

---

## 🚀 Como Executar

1.  **Configure a Autenticação:**
    No seu terminal (com o `venv` ativo), aponte para a sua chave de serviço:

    ```powershell
    # Exemplo no PowerShell
    $env:GOOGLE_APPLICATION_CREDENTIALS="C:\caminho\completo\para\sua-chave.json"
    ```

2.  **Rode o Script:**
    ```bash
    python sistema_transcritor.py
    ```

O script irá criar a pasta `imagens_extraidas` e, ao final, gerar o arquivo `Transcricao_Cultura_Surda.docx` (ou o nome definido em `output_file_path`).

---

## ✍️ Autor

* **Cristiano Lagame**
* **E-mail:** crislagame@gmail.com