# 🚀 1° Instalação do N8N na DigitalOcean com Dokploy e Cupom de US$ 200

## 🎁 Cupom DigitalOcean

Ao criar sua conta usando o link abaixo, você recebe **US$ 200 de crédito gratuito** para utilizar por até **60 dias**:

🔗 Link de cadastro:  
[https://m.do.co/c/62b4c7d94707](https://m.do.co/c/62b4c7d94707)

💰 Valor aproximado em reais (cotação R$ 5,64):  
**US$ 200 ≈ R$ 1.128,00**

---

#
---

## 🔐 Benefícios do uso com cupom:

| Item                            | Custo com Cupom |
|---------------------------------|------------------|
| VM 1 GB RAM por 60 dias         | **R$ 0,00**      |
| Painel Dokploy (open-source)    | **R$ 0,00**      |
| Testes com HTTPS e plugins      | **Incluso**      |

---

## 🧠 Vantagens

- Controle total da máquina
- SSL incluso
- Pode manter em produção após o trial
- Integrações avançadas com APIs externas

---

📌 **Recomendo iniciar com a região mais próxima (ex: NYC ou SP - se disponível) para menor latência.**




# 🛠️ 2° Criação da Máquina Virtual (Droplet) na DigitalOcean

Após 'Concluir' o cadastro no link da Etapa anterior com o desconto, clique em: **Droplets ou Criar Gotas**  

## 🌍 Etapas:

1. **Escolher a Região**: 🇺🇸 **Nova Iorque (NYC)**  
   - Selecionar o Centro de dados/Datacenter: `Nova York - Datacenter 3 (NYC3)`

2. **Plano de máquina (Droplet):**
   - **SO**: Ubuntu
   - **Opções de CPU**: Regular (Disco SSD)
   - **Recursos escolhidos**:
     - `2 GB RAM`
     - `2 vCPUs`
     - `60 GB SSD`
     - `3 TB de transferência`
   - 💵 **Preço**: **US$ 18/mês** ou **US$ 0,027/hora**
   - 💰 **Equivalente em reais** (cotação: R$ 5,64):  
     **US$ 18 ≈ R$ 101,52/mês**
3.  **Habilite a Opção** = Adicione monitoramento e alertas de métricas aprimorados (grátis).

4. **Observações**:
   - Com o cupom de **US$ 200**, você poderá usar esse droplet por aproximadamente **11 meses gratuitos** ou usar múltiplos droplets menores por até **60 dias**.
   - Recursos dedicados e bom desempenho para rodar N8N com plugins.

---




# ▶️3° Próximos Passos: Acessar Droplet e Instalar Dokploy

## 1️⃣ Acessar a máquina virtual criada

- No painel da DigitalOcean, localize seu droplet:
  - Nome: `ubuntuue-s-2vcpu-2gb-nyc3-01`
  - IPv4 público: `174.XXX.XX.217`

---

## 2️⃣ Clique no botão **"Console"**

- Isso abrirá um terminal web para você acessar o Ubuntu diretamente pelo navegador.
- Você já estará logado como `root` e poderá rodar comandos imediatamente.

---

## 3️⃣ O que é o Dokploy?

🔧 **Dokploy** é um painel de deploy simples e open-source que permite:
- Subir aplicações com Docker sem configurar tudo manualmente.
- Configurar SSL automaticamente com Let's Encrypt.
- Gerenciar containers via interface web.

🌐 Site oficial: [https://dokploy.com](https://dokploy.com)

---

## 4️⃣ Comando de instalação do Dokploy

No console do seu droplet, execute o seguinte comando:

```bash
curl -sSL https://dokploy.com/install.sh | sh




# 🌐 4. Acesso ao Dokploy e Criação da Conta

Após a instalação do Dokploy, a seguinte mensagem vai ser exibida no terminal:
1. **Congratulations, Dokploy is installed!
Please go to http://174.XXX.XX.217:3000**


---

## ✅ Etapas seguintes:

1️⃣ **Acesse o painel web**  
Abra seu navegador e digite o endereço:  
🔗 [http://174.XXX.XX.217:3000](http://174.XXX.XX.217:3000)

2️⃣ **Crie sua conta no Dokploy**  
Você verá a tela de registro com os campos:

- **Nome**
- **E-mail**
- **Senha**
- **Confirmar senha**

Depois, clique no botão **Registrar**.

🛡️ *Essa conta será usada para acessar e gerenciar seus containers e serviços dentro do Dokploy.*

---

📌 **Importante**:
- Esse endereço está em HTTP (não seguro) neste momento.
- Após configurar o domínio e SSL via Dokploy, a conexão será convertida para HTTPS.

---




# ⚙️ 5° Criando o Serviço N8N no Dokploy

## ✅ Etapas para subir o N8N com modelo pronto

1️⃣ **Clique no botão `+ Criar Projeto`**  
Dê um nome para o projeto, por exemplo:  
**`agente_aline`**  
Depois clique em **Criar**.

---

2️⃣ **Abra o projeto criado**  
Clique sobre o nome do projeto (ex: `agente_aline`)

---

3️⃣ **Clique no botão `+ Criar Serviço`** (canto superior direito)

- Uma lista de opções será exibida:
  - Aplicativo
  - Banco de dados
  - **Modelo** ✅
  - Assistente de IA
  - etc.

Selecione **Modelo**.

---

4️⃣ **Pesquise pelo modelo `n8n`**  
Digite `n8n` na barra de busca e pressione Enter.

- O modelo do N8N aparecerá com a versão (ex: `1.83.2`)
- Clique no botão **Criar** para iniciar a criação do serviço.

---

📌 Observações:
- Essa abordagem usa um **template oficial** da comunidade com as configurações básicas do N8N.
- O painel do Dokploy irá provisionar automaticamente o container Docker com o N8N.

---




# 🔧6° Criando o Serviço da Evolution API no Dokploy

A **Evolution API** é uma plataforma de mensageria robusta voltada principalmente para **integrações com WhatsApp** e outras soluções de comunicação.  
Ela permite que você envie, receba e automatize mensagens via **API REST**, integrando facilmente com ferramentas como o **N8N** e **ChatGPT**.

---

## ✅ Etapas para criar o serviço da Evolution API

1️⃣ **Acesse o mesmo projeto criado anteriormente**  
Exemplo: `agente_aline`

2️⃣ Clique no botão **`+ Criar Serviço`** no canto superior direito.

3️⃣ Selecione a opção **`Modelo`**.

4️⃣ Na barra de pesquisa, digite:  

evolution 

## 📬 O que é a Evolution API?
* Plataforma de comunicação para automação de mensagens.

* Especializada em WhatsApp Business API.

* Suporta:

1. Envio e recebimento de mensagens

2. Webhooks

3. Integração com bots (ex: N8N + ChatGPT)

🔐 Ideal para criar assistentes inteligentes, respostas automáticas, e integrações com fluxos de atendimento.
