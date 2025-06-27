# 🌐 1 ° Criando Nova Instância na API Evolution

Para configurar a comunicação do seu agente com o WhatsApp utilizando a API Evolution, siga os passos abaixo:

---

## ✅ Passo 1 - Acesse o Gerenciador da API Evolution

Abra o navegador e vá para o seguinte link:

👉 [https://apievolution.agenteinteligente.ddns-ip.net/manager/](https://apievolution.agenteinteligente.ddns-ip.net/manager/)

---

## ➕ Passo 2 - Criar Nova Instância

1. Após acessar o painel de gerenciamento, clique no botão `+ Instance` no canto superior direito.

2. Preencha os campos conforme o exemplo abaixo:

| Campo     | Valor Exemplo                           | Descrição                                                                 |
|-----------|------------------------------------------|--------------------------------------------------------------------------|
| **Name**  | `patricia`                               | Nome identificador da instância                                          |
| **Channel** | `Baileys`                             | Selecione o canal Baileys para integração com o WhatsApp                 |
| **Token** | `4B8E9440470F-4907-8423-B81132BC6C9B34`     | Token de autenticação (gerado automaticamente ou fornecido pela API)     |
| **Number**| `5511945748834`                          | Número de telefone com DDI (ex: 55 para Brasil, 11 para São Paulo)       |

> ⚠️ Certifique-se de que o número está no formato internacional, **sem espaços, hífens ou símbolos**.

---

## 💾 Passo 3 - Salvar

Após preencher todos os campos corretamente, clique no botão verde `Save` para criar a instância.

---

🎉 Pronto! Sua instância está criada e pronta para ser usada nas integrações com o N8N ou outras plataformas.




## 🔗 2° Conectando o WhatsApp à Instância no Evolution Manager

Após criar a instância no painel da API Evolution, siga os passos abaixo para ativar a conexão com o WhatsApp:

---

### 🛠️ Passo 1 - Acesse a Instância Criada

No painel inicial (https://apievolution.agenteinteligente.ddns-ip.net/manager/):

1. Localize a instância criada (exemplo: `patricia`).
2. Clique no ícone de **ferramenta redonda** ⚙️ (localizado no canto superior direito do cartão da instância).

---

### 📲 Passo 2 - Gerar o QR Code

1. Dentro do painel da instância, clique no botão **Get QR Code**.
2. Um QR Code será exibido na tela.

---

### 📱 Passo 3 - Escanear com WhatsApp Business

Abra o **WhatsApp Business** no seu celular:

1. Toque nos **três pontinhos** no canto superior direito.
2. Selecione **Dispositivos Conectados**.
3. Clique em **Conectar um dispositivo**.
4. Aponte a câmera para o QR Code exibido na tela do Evolution Manager.

---

### ✅ Passo 4 - Verificar Conexão

Após o escaneamento:

- A instância será atualizada para o status `Connected ✅`.
- Você verá os dados do número conectado, como contatos, chats e mensagens.

---

### 🧩 Passo 5 - Copiar Token para Integração

- No painel da instância, clique no botão de cópia 📋 ao lado do token.
- Esse token será utilizado para configurar a integração no **N8N** ou qualquer outro sistema externo.

---

📘 **Pronto!** Sua instância está conectada e pronta para enviar/receber mensagens via API Evolution com o WhatsApp Business.




## 🔐 3° Configurando Credenciais da Evolution API no N8N

Após conectar sua instância do WhatsApp no Evolution Manager, agora vamos configurar o N8N para utilizá-la com a Evolution API.

---

### 🌐 Passo 1 - Acessar o N8N

1. Vá para o painel do N8N no navegador:
**https://n8n.agenteinteligente.ddns-ip.net**

2. Clique na aba **Credentials** no menu superior.
3. Clique em **Add first credential**.

---

### 🧩 Passo 2 - Criar Credencial para Evolution API

1. Selecione o tipo: **Evolution API**
2. Na tela de configuração preencha:

| Campo        | Valor                                                   |
|--------------|----------------------------------------------------------|
| **Server Url** | `https://apievolution.agenteinteligente.ddns-ip.net` |
| **ApiKey**     | Cole aqui o **Token da Instância** copiado no painel da API Evolution |

---

### ✅ Passo 3 - Testar Conexão

1. Após preencher os campos, clique em **Save** no canto superior direito.
2. A mensagem `Connection tested successfully` deverá aparecer em verde.

> Se não aparecer, verifique se o token está correto e se a instância no Evolution Manager está com status **Connected**.

---

🔗 **Pronto!** Agora o N8N está conectado com sua instância da Evolution API e você pode usar os nós da comunidade para enviar e receber mensagens do WhatsApp.


