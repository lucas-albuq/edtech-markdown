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
- **Working Tree** → arquivos locais  
- **Staging Area / Index** → arquivos preparados  
- **Repository / Commits** → histórico salvo

---

## 10. 📌 Principais comandos

### Inicialização  
```bash
git init
git clone <repositório>
```

---

## 11. 🧱 Ciclo básico de uso

### Adicionar arquivos  
```bash
git add <arquivo>
git add .        # adiciona tudo
```

### Salvar alterações  
```bash
git commit -m "mensagem descrevendo a alteração"
```

### Ver status  
```bash
git status
```

### Ver histórico  
```bash
git log
```

---

## 12. 🌿 Branches (Ramificações)

### Criar e trocar de branch  
```bash
git branch minha-branch
git checkout minha-branch
git checkout -b minha-branch   # cria e já troca
```

### Ver branches  
```bash
git branch
```

### Deletar branch  
```bash
git branch -d minha-branch
```

---

## 13. 🔄 Merge — unindo branches  
Mescla o conteúdo de outra branch na atual.

```bash
git checkout main
git merge minha-branch
```

---

## 14. 🧭 Navegando pelo histórico

### Voltar para um commit  
```bash
git checkout <hash>
```

### Reset — mover o ponteiro da branch

- Mantendo arquivos:  
  ```bash
  git reset --soft <hash>
  ```

- Limpando staging:  
  ```bash
  git reset --mixed <hash>
  ```

- Reset bruto (perde alterações locais):  
  ```bash
  git reset --hard <hash>
  ```

---

## 15. 🚀 Git Remote — enviar para servidor

### Definir remoto  
```bash
git remote add origin <url>
```

### Enviar alterações  
```bash
git push origin main
```

Primeiro push de uma branch:

```bash
git push -u origin minha-branch
```

### Baixar atualizações  
```bash
git pull
git fetch
```

---

## 16. 📝 Tags — marcar versões

### Criar tag  
```bash
git tag v1.0
git tag -a v1.0 -m "Primeira versão"
```

### Enviar tags  
```bash
git push origin --tags
```

---

## 17. 🧼 Lidando com conflitos

O Git marca conflitos assim:

```
<<<<<<< HEAD
seção da branch atual
=======
seção da outra branch
>>>>>>> minha-branch
```

Depois de resolver:

```bash
git add .
git commit
```

---

## 18. 🧪 Modelos de Branching

### Git Flow  
- `main`  
- `develop`  
- `feature/*`  
- `release/*`  
- `hotfix/*`

### Trunk Based  
- foco em uma branch principal  
- merges rápidos e contínuos  

---

## 19. 🧲 Stash — guardando alterações temporárias

```bash
git stash
git stash list
git stash pop
```

---

## 20. 🔐 Arquivo `.gitignore`

Arquivos comuns:

```
node_modules/
.env
.vscode/
*.log
```

