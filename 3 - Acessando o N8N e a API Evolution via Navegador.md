# 🧭 Acesso ao API Evolution e N8N após configuração no Dokploy

Após adicionar os domínios, ativar HTTPS e fazer o deploy no Dokploy, siga os passos abaixo para acessar os serviços diretamente via navegador:

---

## 1️⃣ Acessando o **API Evolution**

- No painel do **Dokploy**, vá até a aba **Domains** do serviço `apievolution`.
- Clique sobre o novo domínio configurado, por exemplo:  
  `apievolution.agenteinteligente.ddns-ip.net`

- Após abrir o link, **adicione** `/manager` ao final da URL:
`https://apievolution.agenteinteligente.ddns-ip.net/manager`

- Isso abrirá a tela de login do **Evolution Manager**, onde você deve inserir:
`https://apievolution.agenteinteligente.ddns-ip.net/manager/login`
1. **Server URL:** preenchido automaticamente
2. **API Key Global:** fornecida pela EvolutionAPI na aba Environment do Dokploy como = AUTHENTICATION_API_KEY

---

## 2️⃣ Acessando o **N8N**

- No painel do **Dokploy**, vá até o serviço `n8n` e clique na aba **Domains**.
- Clique no novo domínio configurado.
- Isso abrirá a interface principal do **N8N**, ai é só preencher as informações solicitadas e pronto!.

---

✅ Ambos os serviços agora estão acessíveis de forma pública, segura (HTTPS) e com seus domínios DNS configurados via **ClouDNS**.



