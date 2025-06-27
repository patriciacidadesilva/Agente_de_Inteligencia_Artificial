%md

# AGENTE DE INTELIGÊNCIA ARTIFICIAL 

# 💡 1° O que é um Agente de Inteligência Artificial? 

Um agente de inteligência artificial (IA) é um sistema que percebe seu ambiente, toma decisões e executa ações com base nessas percepções para atingir um objetivo específico. Em outras palavras, é uma entidade (software, robô, chatbot etc.) que atua de forma autônoma ou semiautônoma com base em dados, algoritmos e regras predefinidas.


### 🔍 Estrutura básica de um agente de IA:
#### 1. Sensores (Percepção)
Capturam dados do ambiente (ex: câmera, microfone, logs de sistema, texto digitado pelo usuário).

#### 2. Processamento/Modelo de decisão
Utiliza algoritmos para interpretar os dados e decidir o que fazer. Pode envolver:

* Regras lógicas

* Aprendizado de máquina

* Modelos estatísticos

#### 3. Atores (Ação)
Executa ações no ambiente (ex: responder uma pergunta, mover um robô, enviar um e-mail, sugerir um produto).



### 🧠 Tipos de Agentes de IA:
* Reativos Simples: Reagem diretamente a estímulos (ex: termostato inteligente).

* Baseados em Objetivos: Avaliam as consequências antes de agir para atingir um objetivo.

* Baseados em Utilidade: Escolhem a ação que maximiza uma "utilidade" (benefício).

* Aprendizes: Aprendem com o tempo para melhorar suas decisões (ex: ChatGPT, assistentes virtuais, carros autônomos).



### 💡 Exemplos práticos:
* Assistentes virtuais como Siri, Alexa e ChatGPT.

* Sistemas de recomendação da Netflix ou Amazon.

* Bots de atendimento em sites e aplicativos.

* Robôs autônomos em fábricas ou veículos autônomos.

* Agentes no Microsoft Copilot Studio, que automatizam processos com base em dados e interações.


# 🚀 2° Formas de Instalação do N8N + Custos 

## ✅ Formas de instalação do N8N

### ☁️ 1. Cloud via [n8n.io](https://n8n.io)
- Hospedagem oficial na nuvem, gerenciada pela equipe do N8N.
- Ideal para quem quer simplicidade, atualização automática e suporte.
- **Custo variável por execução**: além do valor base mensal, a plataforma cobra conforme o número de execuções mensais dos fluxos.

📌 **Exemplo**:
- Plano Starter: **US$ 26,54/mês = R$ 150,00/mês** inclui até **2.500 execuções/mês**.
- Execuções adicionais são cobradas à parte.

### 💻 2. Railways (via container Docker)
- Subida de VM (container) com N8N.
- Plataforma Railway com deploy em containers.


### 🌐 3. Provedores Cloud: DigitalOcean, Amazon, Azure, Oracle
- Instalação manual em máquina virtual.
- Etapas incluem uso de **Dokploy** e **SSL**.


---

## 💰 Conversão de Valores – USD para BRL

*Cotação base: US$ 1,00 ≈ R$ 5,64*

| **Serviço**                       | **Valor em USD** | **Valor em BRL**    |
|----------------------------------|------------------|----------------------|
| n8n.io (plano base)              | US$ 26,54/mês       | R$ 150,00/mês        |
| Railway (plano básico)           | US$ 5/mês        | R$ 28,20/mês         |
| DigitalOcean (droplet 1GB)       | US$ 5/mês        | R$ 28,20/mês         |
| Amazon EC2 (t2.micro - Free Tier)| US$ 0            | R$ 0,00              |
| Azure (créditos gratuitos)       | US$ 0            | R$ 0,00              |
| Oracle Cloud (Always Free)       | US$ 0            | R$ 0,00              |

---

## 📊 Comparativo das Opções

| **Versão**               | **Custo** | **Cobrança por Execução** | **Facilidade** | **Controle** |
|--------------------------|-----------|----------------------------|----------------|--------------|
| n8n Cloud (n8n.io)       | Alto      | ✅ Sim                     | ✅ Alta         | ❌ Baixo     |
| Railway (Docker)         | Baixo     | ❌ Não (exceto por uso de recursos) | Médio      | Médio       |
| DigitalOcean com Dokploy| Médio     | ❌ Não                     | Baixa          | ✅ Alto      |
| Amazon/Azure/Oracle Free| Nenhum    | ❌ Não                     | Médio          | Médio        |

---


# 🌐 3° O que é um DNS?

## ✅ Definição
**DNS (Domain Name System)** é o sistema responsável por traduzir **nomes de domínio legíveis por humanos** (como `google.com`) em **endereços IP** (como `8.8.8.8`), que são compreendidos pelos servidores e dispositivos na internet.

---

## 🔁 Como funciona o processo (fluxo da imagem):

1. **CLIENTE** (usuário) digita um endereço como `google.com`.
2. O pedido vai para a **Internet**, onde é direcionado ao servidor DNS.
3. O **DNS SERVER** localiza o IP associado (`8.8.8.8`) ao nome `google.com`.
4. Com o IP em mãos, a requisição é enviada ao **WEB SERVER** correspondente.
5. O conteúdo do site é então retornado ao **cliente**.

---

## 🧠 Analogia simples:
Imagine o DNS como a **agenda de contatos da internet**:
- Você busca “João” e a agenda te mostra o número dele.
- Com esse número, você faz a ligação.
- No caso da internet: você digita `google.com`, o DNS te fornece `8.8.8.8`, e com isso o site é carregado.

---

## 📌 Exemplo prático:
- Nome de domínio: `google.com`
- Endereço IP real: `8.8.8.8` (exemplo usado pelo Google)

---

## 🔐 Curiosidade:
O DNS pode ser manipulado ou atacado (ex: DNS spoofing). Por isso, existem versões seguras como **DNS over HTTPS (DoH)** e **DNSSEC**.



# 🚀 4° Instalação do N8N via n8n.cloud em 5 minutos

## ✅ Passo a passo simples:

1. Acesse o link:  
   👉 [app.n8n.cloud/register](https://app.n8n.cloud/register)

2. Preencha os seguintes campos:
   - **Full name** (nome completo)
   - **Company email** (e-mail corporativo)
   - **Confirm email address** (confirmar e-mail)
   - **Password** (senha)
   - **Account name** (nome da sua conta — será usado na URL)

3. Após o cadastro, você recebe:
   - **14 dias de trial grátis**
   - Instância **100% configurada** e pronta para uso

---

## 🎯 Vantagens dessa opção:

✅ Instalação automatizada (nenhuma configuração técnica necessária)  
✅ Acesso imediato via navegador  
✅ Ideal para testes, provas de conceito ou primeiras automações

---

## ⚠️ Observação:

Após o período gratuito de 14 dias, o plano passa a ser **pago** com base no número de execuções mensais. Consulte os planos atualizados em:  
👉 [n8n.io/pricing](https://n8n.io/pricing)


# 💸 Planos Atualizados do N8N.cloud (2024/2025)

## ✅ Preços com cobrança **mensal e anual** 

| **Plano**   | **Valor Plano Mensal** | **Valor Plano Anual** | **Execuções**            | **Workflows Ativos** |
|-------------|--------------------|------------------|---------------------------|-----------------------|
| **Starter** | R$150         | R$125/mês        | 2.500 execuções/mês       | 5 ativos              |
| **Pro**     | R$375         | R$313/mês        | 10.000 execuções/mês      | 15 ativos             |
| **Enterprise** | Sob consulta     | Sob consulta     | Execuções ilimitadas      | Workflows ilimitados  |

> 💡 Todos os planos permitem **etapas ilimitadas por workflow** e **workflows de teste ilimitados**.

---

## 🔍 Observações importantes:


- A cobrança é feita em **Reais (BRL)**, facilitando para usuários no Brasil.
- O plano **Starter** é ideal para uso individual ou pequenos projetos.
- O plano **Pro** atende equipes com maior volume de automações.
- O plano **Enterprise** é voltado para empresas com alto nível de segurança e personalização — o preço é sob consulta.

---

## 🧪 Trial Gratuito
Você ainda pode começar com um período de **14 dias gratuitos** em:  
👉 [https://app.n8n.cloud/register](https://app.n8n.cloud/register)



# 🚄 5° Instalação do N8N com Railway – Ambiente Gratuito para Testes

A Railway é uma plataforma moderna de deploy que permite criar e escalar containers de forma simples. Ideal para quem quer rodar o N8N com custo reduzido e controle técnico.

## 🧪 Trial Gratuito com Créditos

Ao criar sua conta no [Railway](https://railway.app), você recebe um **crédito inicial de US$ 5,00**, que permite testar e rodar aplicações como o N8N **sem custos imediatos**.

💰 **Valor aproximado em reais (cotação R$ 5,64)**:  
**US$ 5,00 ≈ R$ 28,20**

---

## 📦 Ambiente Provisionado no Plano Gratuito (Trial)

- **512 MB de RAM**
- **1 GB de Disco**
- **2 vCPU**
- Duração do trial depende do uso de recursos (CPU/RAM).

> 💡 O valor do uso vai sendo descontado do crédito de US$ 5,00, mostrado no topo do painel da Railway.

---

## ✅ Etapas Visuais da Instalação

1. Após login via GitHub, você será redirecionado ao painel.
2. O projeto criado recebe um nome aleatório (ex: `passionate-wisdom`).
3. Dentro do projeto, você pode subir containers (ex: N8N com Docker).
4. O uso de recursos será abatido do valor em **trial** (ex: `US$ 4.92` de uso).

---

## 📌 Observações

- Railway cobra por tempo de uso (horas de CPU, RAM, disco).
- Quando o trial termina, você pode **migrar para o plano pago**:
  - A partir de **US$ 5/mês** ≈ **R$ 28,20/mês**
- Ideal para **MVPs**, **testes de automação** ou **uso pessoal leve**.

---

👉 Acesse e teste gratuitamente: [https://railway.app](https://railway.app)


# 🌐 6° Instalação do N8N na DigitalOcean com Dokploy (Instalação de InfraEstrura mais Complexa)

## ✅ Instruções passo a passo:

1. **Criando uma máquina virtual (VM) na DigitalOcean**
   - Sugestão: Droplet de 1 GB RAM, 1 vCPU, 25 GB SSD

2. **Instalando o painel Dokploy**
   - Gerenciador de deploys via interface web
   - Instalação via SSH com script automático

3. **Subindo container do N8N e EvolutionAPI com SSL (HTTPS)**
   - Uso de Docker para rodar o N8N
   - Configuração de certificado SSL (Let’s Encrypt)

4. **Configurando o plugin EvolutionAPI no N8N**
   - Comunicação segura com APIs (ex: WhatsApp via Evolution)

5. **Desafio**: Criar um **Agente AI** que integra:
   - 🔁 N8N  
   - 🤖 ChatGPT  
   - 📲 WhatsApp (via Evolution API)

---

## 💰 Custo estimado (DigitalOcean)

| Recurso                  | Valor em USD | Valor Aproximado em BRL |
|--------------------------|--------------|--------------------------|
| Droplet básico (1 GB RAM)| US$ 5/mês    | **R$ 28,20/mês**         |

> 💡 **Cotação base**: US$ 1,00 ≈ R$ 5,64

---

## 🧠 Ideal para quem:
- Precisa de controle total da infraestrutura
- Quer instalar plugins e serviços customizados
- Deseja usar HTTPS e deploy automatizado com SSL

---

## 🛠️ Recursos necessários:
- Conta na DigitalOcean: [https://www.digitalocean.com](https://www.digitalocean.com)
- Acesso a terminal SSH
- Conhecimentos básicos em Linux e Docker (ou seguir tutoriais passo a passo)


