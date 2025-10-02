# 🤖 Robô de Consulta Simples Nacional e MEI

## 📌 Descrição
Este projeto é um **robô em Python** que automatiza a consulta de **CNPJs** no site do Simples Nacional.  
Ele extrai a situação da empresa em relação ao **Simples Nacional** e ao **MEI**, atualiza diretamente uma **planilha Excel** e envia notificações para o **Telegram** sobre o andamento da execução.

O processo é totalmente automatizado, eliminando a necessidade de consultas manuais e acelerando a coleta de informações fiscais.

---

## 🛠 Tecnologias Utilizadas
- **Python** 🐍  
- [PyAutoGUI](https://pypi.org/project/PyAutoGUI/) → automação da interação no navegador  
- [OpenPyXL](https://pypi.org/project/openpyxl/) → leitura e escrita em planilhas Excel  
- [Pyperclip](https://pypi.org/project/pyperclip/) → copiar/colar resultados do site  
- [Requests](https://pypi.org/project/requests/) → integração com API do Telegram  
- [python-dotenv](https://pypi.org/project/python-dotenv/) → gerenciamento seguro de variáveis de ambiente  

---

## 🚀 Funcionalidades

- Lê CNPJs de uma planilha Excel.  
- Consulta automaticamente a situação de cada CNPJ no site da Receita Federal.  
- Identifica e registra status no **Simples Nacional** e no **MEI**.  
- Atualiza a planilha com os resultados.  
- Salva automaticamente a cada 50 linhas processadas.  
- Envia mensagens para o Telegram informando o progresso.  
- Ao final, envia mensagem de conclusão e total de CNPJs processados.  

---

## 📂 Estrutura do Projeto
📁 SimplesNacionalBot  
│  
├── 📜 main.py — código principal  
├── 🔑 .env — variáveis de ambiente (não subir no GitHub)  
├── 📦 requirements.txt — dependências do projeto  
└── 📘 README.md — documentação  

---

## ⚙️ Pré-requisitos
- Python 3.9+  
- Navegador instalado (padrão: abre no navegador padrão do sistema)  
- Planilha Excel de entrada (`.xlsx`) contendo os **CNPJs** na **primeira coluna**  

---

## 📥 Instalação e Uso
1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/SimplesNacionalBot.git
   cd SimplesNacionalBot

🐍 Ambiente Virtual

Para rodar o projeto em um ambiente isolado, siga os passos:

# Windows
python -m venv venv

# Linux / Mac
python3 -m venv venv

# Windows (PowerShell)
venv\Scripts\Activate.ps1

# Windows (CMD)
venv\Scripts\activate

# Linux / Mac
source venv/bin/activate

## 📦 Instalação de Dependências
Com o ambiente virtual ativado, instale as dependências:

```bash        
pip install -r requirements.txt
```            

---

## 🔑 Configuração do arquivo `.env`
Crie o arquivo `.env` na raiz do projeto e adicione:

```env        
PLANILHA_PATH=C:\caminho\para\sua\planilha.xlsx
TELEGRAM_TOKEN=SEU_TOKEN_AQUI
TELEGRAM_CHAT_ID=SEU_CHAT_ID_AQUI
```            

---

## ▶️ Execução
Para rodar o robô:

```bash       
python main.py
```           
