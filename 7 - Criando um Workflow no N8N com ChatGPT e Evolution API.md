# 🤖 1° Criando um Workflow no N8N com ChatGPT e Evolution API

Neste fluxo, vamos configurar um chatbot automatizado no N8N que responde mensagens recebidas via WhatsApp, utilizando a integração entre a **Evolution API** e a **OpenAI (ChatGPT)**.

---

## ⚙️ Etapa 1 - Criar o Workflow

1. Acesse o painel do N8N: **https://n8n.agenteinteligente.ddns-ip.net**
2. Clique no botão **+ Create Workflow**.
3. Dê um nome para o seu fluxo (ex: `Chatbot WhatsApp GPT`).

---

## 💬 Etapa 2 - Adicionar o Gatilho de Webhook

1. Clique em **Add first step**.
2. Pesquise por `Webhook` e selecione o nó **Webhook**.
3. Configure o nó com os seguintes parâmetros:
   - **HTTP Method**: `POST`
   - **Authentication**: `None`
   - **Respond**: `Immediately`
4. Copie a **Test URL** exibida no topo.

---

## 🧠 Etapa 3 - Adicionar o AI Agent

1. Adicione o nó **AI Agent (Tools Agent)**.
2. Source for Prompt (User Message) = Define below
3. Prompt (User Message) = conversation
4. Options/System Message = Você é um assistente financeiro inteligente da empresa. Sua principal missão é dar dicas de como fazer a cobrança dos clientes. 
5. Max Iterations = 10
2. Conecte o Webhook à entrada do AI Agent.
3. No campo `Chat Model`, conecte o próximo nó do ChatGPT.

---

## 🤖 Etapa 4 - Adicionar o Nó do ChatGPT

1. Adicione o nó **OpenAI Chat Model**.
2. Configure com os seguintes parâmetros:
   - **Model**: `gpt-4-mini` ou outro modelo desejado.
   - **Credentials**: selecione a credencial `OpenAI account`.

---

## 📤 Etapa 5 - Enviar Resposta pelo WhatsApp

1. Adicione o nó **Evolution API**.
2. Configure com os seguintes campos:
   - **Credencial**: `Evolution account`
   - **Recurso**: `Mensagem`
   - **Operação**: `Enviar Texto`
   - **Nome da Instância**: ex: `patricia`
   - **Número do Destinatário**: `remoteJid`     
   - **Mensagem**: `output`

---

## 🧪 Etapa 6 - Testando o Webhook no Evolution Manager

1. No N8N, clique no nó Webhook e copie a **Test URL** gerada.
2. Acesse o painel da instância em **https://apievolution.agenteinteligente.ddns-ip.net/manager/**
3. Vá no menu lateral em **Events > Webhook**.
4. Cole a **Test URL** no campo **URL**.
5. Ative o botão **Enabled**.
6. Em **Eventos**, ative a opção **MESSAGES_UPSERT**.
7. Clique em **Save** para salvar a configuração.

---

## ⚙️ Etapa 7 - Ajustes Finais

1. Acesse o menu **Configurations > Settings** no painel do Evolution Manager.
2. Ative a opção **Read Messages** para que as mensagens recebidas sejam marcadas como lidas.
3. Clique em **Save**.




# 🧪 2° Testando o Workflow 

Após configurar todo o fluxo entre Webhook, AI Agent, OpenAI Chat Model e Evolution API, é hora de **realizar os testes finais** para garantir que o bot está funcionando corretamente, para iniciar o fluxo de teste clique em = **Test workflow**

---

## 📩 Etapa 1 - Enviar uma Mensagem de Teste

1. Com o fluxo ativo, envie uma mensagem real via WhatsApp para o número conectado à instância da **Evolution API**.
2. Certifique-se de que o Webhook esteja conectado e com o evento `MESSAGES_UPSERT` habilitado.

---

## 🧾 Etapa 2 - Verificar se o Webhook capturou a mensagem

1. Clique sobre o nó `Webhook`.
2. Na aba de output, verifique os detalhes da requisição recebida:
   - Campo: `body.data.message.conversation`
   - Contém a mensagem enviada no WhatsApp.

---

## 🧠 Etapa 3 - Checar o Prompt no AI Agent

1. Abra o nó **AI Agent (Tools Agent)**.
2. Confirme que o campo de prompt está puxando corretamente o conteúdo:
**{{ $json.body.data.message.conversation }}**
3. O System Message também deve estar preenchido com o papel da IA:
> Você é um assistente financeiro inteligente da empresa...

---

## 🧠 Etapa 4 - Analisar a Resposta do ChatGPT

1. Clique no nó **OpenAI Chat Model**.
2. Confirme o modelo utilizado (ex: `gpt-4o-mini`).
3. A resposta gerada será exibida na aba `response.text`.

---

## ✅ Etapa Final - Conferir se a resposta chegou no WhatsApp

1. Após o fluxo completo ser executado, a resposta gerada será enviada automaticamente via **Evolution API**.
2. Verifique se a mensagem foi recebida corretamente no número de origem do WhatsApp.

---

🎉 **Pronto! Seu assistente está testado e funcionando com sucesso!**
Agora você pode expandir o fluxo com validações, filtros de palavras, lógica de negócios, e muito mais!




# ✅ 3° Ativando e Finalizando o Workflow no N8N

Agora que o fluxo está pronto, com as integrações entre Webhook, AI Agent, ChatGPT e Evolution API funcionando corretamente em ambiente de desenvolvimento, vamos finalizar e ativar tudo para o uso em **PRODUÇÃO**.

---

## 🌐 Atualizando o Webhook na Evolution API

1. Acesse o painel do Evolution Manager:  
   **https://apievolution.agenteinteligente.ddns-ip.net/manager/**
2. No menu lateral, vá em: **Events > Webhook**.
3. No campo **URL**, cole o webhook definitivo:**https://n8n.agentedeco.ddns-ip.net/webhook/f4010f78-709c-4cfc-ae1e-57cc3e2a1d15**
4. Ative o botão **Enabled**.
5. Em **Eventos**, ative: `MESSAGES_UPSERT`.
6. Clique em **Save**.

---

## 🧠 Ajuste final no N8N

1. Abra seu workflow no painel do N8N:  
   **https://n8n.agentedeco.ddns-ip.net**
2. Clique no botão **Save** no topo da tela.
3. Altere o status no topo de `Inactive` para `Active` (botão de ativação).
4. Seu fluxo agora está oficialmente **publicado e funcionando em produção**!

---

## 🚀 Testando em Produção

1. Envie uma mensagem real para o número conectado à Evolution API.
2. O webhook será acionado.
3. A mensagem será processada pelo AI Agent + OpenAI Chat Model.
4. A resposta será enviada automaticamente via WhatsApp pelo nó da Evolution API.

---

🎉 **Pronto! Seu chatbot financeiro está ativo, testado e respondendo via WhatsApp com ChatGPT integrado!**
