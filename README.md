<p align="center">
  <img src="https://github.com/entomologista/juriboss/blob/main/static/banner-juriboss.png" width="100%" alt="JuRiboss — Líder em Tradução do Juridiquês">
</p>


# 🏛️ JuRiboss — Líder em Tradução do Juridiquês

**JuRiboss** é um sistema eletrônico de acesso público criado para **traduzir textos jurídicos complexos ("juridiquês") em linguagem clara e acessível ao cidadão comum**.  
O nome combina três ideias:
- **Juri** → de “jurídico” ou “juris”;  
- **Riboss** → referência ao *ribossomo*, organela responsável pela “tradução” biológica;  
- **Boss** → do inglês “chefe” ou “líder”, simbolizando a posição de vanguarda do sistema em simplificação jurídica.  

---

## ✨ **Objetivo**

Promover **acessibilidade à informação jurídica**, eliminando barreiras linguísticas e permitindo que qualquer pessoa compreenda:
- contratos, editais e legislações;  
- petições, recursos e decisões judiciais;  
- e demais documentos técnicos de difícil leitura.

---

## ⚙️ **Funcionalidades Principais**

- 🔹 **Upload de arquivos** em `.txt`, `.docx` ou `.pdf` (não escaneados);  
- 🔹 **Três níveis de tradução**:
  - 👶 Criança de 10 anos  
  - 🎓 Ensino médio completo  
  - 🎓 Ensino superior completo  
- 🔹 **Tradução via Inteligência Artificial (OpenAI API)**  
- 🔹 **Fallback local**: sistema autônomo que simplifica o texto mesmo offline, com substituição automática de expressões jurídicas por equivalentes simples;  
- 🔹 **Download do resultado** em `.pdf` ou `.docx`.

---

## 🧩 **Tecnologias Utilizadas**

| Camada | Tecnologia |
|---------|-------------|
| Backend | Python + FastAPI |
| Frontend | HTML + CSS + Jinja2 |
| IA | OpenAI API (modelos `gpt-4o-mini`, `gpt-5`, etc.) |
| Conversão de arquivos | `python-docx`, `pypdf`, `reportlab` |
| Implantação | Render.com |
| Pagamentos e validação | Stripe (Render) |

---

## 🧭 **Como Executar Localmente**

### 🔸 1. Clone o repositório
```bash
git clone https://github.com/SEU_USUARIO/juriboss.git
cd juriboss
````

### 🔸 2. Crie o ambiente virtual e instale dependências

```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1     # (Windows PowerShell)
pip install -r requirements.txt
```

### 🔸 3. Configure a variável de ambiente da API

No PowerShell:

```bash
$env:OPENAI_API_KEY = "sua_chave_aqui"
$env:OPENAI_MODEL = "gpt-4o-mini"   # ou "gpt-5"
```

### 🔸 4. Execute o servidor

```bash
uvicorn main:app --reload
```

Acesse: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## ☁️ **Deploy no Render**

1. Crie uma conta em [https://render.com](https://render.com)
2. Conecte seu GitHub e selecione o repositório `juriboss`
3. Configure:

   * **Build Command:** `pip install -r requirements.txt`
   * **Start Command:** `uvicorn main:app --host 0.0.0.0 --port $PORT`
4. Em **Environment Variables**, adicione:

   * `OPENAI_API_KEY` → sua chave pessoal (não inclua no código)
   * `OPENAI_MODEL` → `gpt-5` ou `gpt-4o-mini`
5. Clique em **Deploy Web Service**

Seu sistema ficará disponível em um link público como:
👉 `https://juriboss.onrender.com`

---

## 🧠 **Fallback Local**

O JuRiboss possui um mecanismo de **simplificação local automática**, que entra em ação sempre que a IA estiver indisponível ou sem créditos.
Esse módulo:

* substitui **expressões jurídicas complexas** por linguagem simples;
* traduz **siglas legais** (ex.: CLT → Consolidação das Leis do Trabalho);
* adapta o texto conforme o **nível de leitura escolhido**.

---

## 🧾 **Licença e Uso**

Este projeto tem finalidade **educacional e social**, voltada à promoção da cidadania e ao acesso à justiça.
O código pode ser reutilizado com atribuição ao autor.

---

## 👨‍💻 **Autores**

* **Cherre Sade Bezerra Da Silva**
* **Éllen Rafael Alves Guedes**
* **Emilly Barros de Oliveira da Silva**
* **Julyendreson Marques Ferreira de Sousa**
* **Mariana de Lima Santos**


Acadêmicos do 4° período do curso de Bacharelado em Direito (Noturno) da UNIFACISA.

## 👨‍💻 **Contatos**

* **entomologista@gmail.com**
* **ellen.raguedes@gmail.com**
* **emilly.boss15@gmail.com**
* **julyendreson@gmail.com**
* **mariana.santos@maisunifacisa.com.br**

Projeto desenvolvido em out.-nov./2025 no contexto da competência **“220063 - Projeto Integrador”** do curso de **Bacharelado em Direito – UNIFACISA**.

* **Orientação e codificação:** Prof. Gustavo Costa Vasconcelos (UNIFACISA) e ChatGPT (Inteligência Artificial da OpenAI).

* **Natureza do projeto:** inovação tecnológica e social aplicada ao Direito.

* **Objetivo institucional:** integrar teoria jurídica, tecnologia e cidadania.
