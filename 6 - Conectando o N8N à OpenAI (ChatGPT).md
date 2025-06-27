## 🤖 Conectando o N8N à OpenAI (ChatGPT)

Para utilizar o ChatGPT dentro do N8N, é necessário gerar uma chave de API da OpenAI e configurar a credencial no painel do N8N. Siga os passos abaixo:

---

### 🔑 Passo 1 - Gerar a API Key na OpenAI

1. Acesse a plataforma da OpenAI:
   👉 https://platform.openai.com/api-keys
2. Clique no botão **+ Create new secret key**.
3. Dê um nome para sua chave, exemplo: `My Test Key`.
4. Clique em **Create secret key**.
5. Copie a chave gerada. **Importante: você só verá a chave uma vez!**

---

### 🧩 Passo 2 - Adicionar Credencial no N8N

1. Vá para o painel do N8N: **https://n8n.agenteinteligente.ddns-ip.net**
2. Clique na aba **Credentials**.
3. Clique em **Add Credential** e escolha a opção **OpenAI**.
4. No campo **API Key**, cole a chave gerada na OpenAI.
5. Clique em **Save**.

---

### ✅ Passo 3 - Testar e Utilizar

- A conexão será salva e estará pronta para uso nos nós do OpenAI dentro dos seus Workflows no N8N.
- Agora você poderá utilizar o modelo GPT para gerar textos, respostas, e muito mais diretamente do seu fluxo.

---

🔗 **Pronto!** O N8N agora está conectado ao ChatGPT via OpenAI API.
