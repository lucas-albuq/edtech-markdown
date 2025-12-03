# 📘 Compilado de Redes e Git  
*Lucas Francisco de Albuquerque Barbosa - Turma 7 Alpha Edtech*

## 1. 🛰️ Fundamentos de Redes  
As redes de computadores permitem que dispositivos troquem informações entre si. Para isso, utilizam protocolos, endereços, equipamentos físicos e camadas de abstração.

---

## 2. 🔢 Endereçamento IP

### IPv4  
- Usa 32 bits (4 blocos de 0–255).  
- Exemplo: `192.168.0.15`  
- Possui faixas privadas e públicas.  
- Usa máscara de rede para definir o tamanho da rede.

### Sub-redes  
Criar sub-redes permite dividir uma rede maior, melhorando organização e segurança.

**Exemplo:**  
Rede `192.168.1.0/24` pode ser dividida em sub-redes `/28`.

---

## 3. 🌍 DNS — Domain Name System  
O DNS funciona como uma “agenda de contatos” da internet, traduzindo domínios legíveis em IPs.

- **A** → aponta domínio para IPv4  
- **AAAA** → aponta domínio para IPv6  
- **CNAME** → alias para outro domínio  
- **MX** → define servidores de e-mail  
- **TXT** → informações adicionais ou verificações

---

## 4. ⚙️ DHCP — Configuração automática  
O DHCP distribui IP, máscara, gateway e DNS automaticamente.

Processo simplificado:  
1. *Discover* → cliente anuncia que precisa de IP  
2. *Offer* → servidor oferece um endereço  
3. *Request* → cliente escolhe a oferta  
4. *ACK* → servidor confirma e libera o IP

---

## 5. 📡 Modos de comunicação  
- **Unicast** → um para um  
- **Broadcast** → um para todos  
- **Multicast** → um para vários selecionados  

---

## 6. 📦 Protocolos Importantes  

### TCP  
- Confiável  
- Ordenado  
- Garantia de entrega  
- Usado em navegação, e-mail, downloads

### UDP  
- Não confiável  
- Leve e rápido  
- Usado em streaming, jogos e chamadas de voz

---

## 7. 📁 Termos essenciais em redes  
- **Gateway** → porta de saída da rede  
- **Switch** → conecta dispositivos internos  
- **Roteador** → conecta redes diferentes  
- **NAT** → traduz IPs privados em públicos  
- **Proxy** → intermediário para segurança e cache  
- **Firewall** → controla acessos e bloqueios

---

# 🛠️ Git — Controle de Versão

## 8. 🎯 O que é Git?  
Sistema de versionamento que registra alterações, permite colaboração e facilita o controle do histórico.

---

## 9. 📂 Três estados do Git  
- **Working Directory** → arquivos locais  
- **Staging Area** → arquivos preparados  
- **Repository** → histórico salvo

---

## 10. 📌 Principais comandos

### Inicialização  
```bash
git init
git clone <repositório>
