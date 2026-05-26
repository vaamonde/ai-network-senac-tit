# Guia Prático — Importação da Máquina Virtual Ubuntu Server 22.04.4 LTS no Oracle VirtualBox 7.2

## Curso Livre de Inteligência Artificial Voltada a Redes de Computadores
### SENAC São Paulo — Unidade Lapa Tito

---

# 🎯 Objetivo

Importar a imagem virtual `UbuntuServer-OnPremises.ova` no Oracle VirtualBox 7.2, configurar a rede em modo **Bridge (Ponte)** utilizando a rede cabeada do laboratório (`10.24.82.0/24`) e iniciar a máquina virtual para acesso remoto via SSH.

---

# 🖥️ Ambiente do Laboratório

| Item | Configuração |
|---|---|
| Sistema Operacional | Microsoft Windows 11 |
| Virtualizador | Oracle VirtualBox 7.2 |
| CPU | Intel Core i7 14700K |
| Memória RAM | 32 GB |
| Disco | NVMe 1TB |
| Rede Local | 10.24.82.0/24 |

---

# 📁 Pré-Requisitos

Antes de iniciar, confirme:

- ✅ Oracle VirtualBox 7.2 instalado;
- ✅ Arquivo `UbuntuServer-OnPremises.ova` disponível na pasta `Downloads`;
- ✅ Cabo de rede conectado no computador;
- ✅ Permissão de uso do laboratório.

---

# 🚀 PASSO 1 — Abrir o Oracle VirtualBox

1. Clique no menu **Iniciar** do Windows;
2. Procure por:

   ```text
   Oracle VirtualBox
   ```

3. Abra o programa.

---

# 📦 PASSO 2 — Importar a Máquina Virtual OVA

## 🔹 Método de Importação

1. No VirtualBox clique em:

   ```text
   Arquivo → Importar Appliance
   ```

2. Clique no ícone da pasta 📂;

3. Navegue até:

   ```text
   Downloads
   ```

4. Selecione o arquivo:

   ```text
   UbuntuServer-OnPremises.ova
   ```

5. Clique em:

   ```text
   Próximo
   ```

---

# ⚙️ PASSO 3 — Revisar as Configurações da VM

Na tela de importação:

- ✅ Verifique o nome da VM;
- ✅ Confira CPU e memória;
- ✅ Mantenha as configurações padrão do professor.

Depois clique em:

```text
Finalizar
```

⏳ Aguarde a importação terminar.

---

# 🌐 PASSO 4 — Configurar Rede em Modo Bridge (Ponte)

## 🔹 Abrir Configurações da VM

1. Selecione a máquina virtual importada;
2. Clique em:

   ```text
   Configurações
   ```

3. Vá até:

   ```text
   Rede
   ```

---

## 🔹 Configurar Adaptador

### Adaptador 1

Configure exatamente assim:

| Opção | Configuração |
|---|---|
| Habilitar Placa de Rede | ✅ Marcado |
| Conectado a | Adaptador em Ponte |
| Nome | Placa de Rede Cabeada do Laboratório |
| Modo Promíscuo | Permitir Tudo |
| Cabo Conectado | ✅ Marcado |

---

# 🧠 Explicação do Modo Bridge

O modo **Bridge (Ponte)** faz a máquina virtual participar diretamente da rede do laboratório.

Isso significa que:

- ✅ A VM recebe IP da rede `10.24.82.0/24`;
- ✅ A VM poderá acessar internet e outros dispositivos;
- ✅ Outros computadores poderão acessar a VM via SSH.

---

# 💾 PASSO 5 — Salvar Configurações

Após concluir:

1. Clique em:

   ```text
   OK
   ```

---

# ▶️ PASSO 6 — Iniciar a Máquina Virtual

1. Selecione a VM;
2. Clique em:

   ```text
   Iniciar
   ```

3. Aguarde o Ubuntu Server carregar.

---

# 🔐 PASSO 7 — Fazer Login no Ubuntu Server

Na tela do terminal:

Digite o usuário e senha fornecidos pelo professor.

Exemplo:

```bash
login: aluno
password: ********
```

---

# 🌍 PASSO 8 — Verificar Endereço IP da VM

Após o login execute:

```bash
ip addr
```

ou

```bash
hostname -I
```

---

# ✅ Resultado Esperado

A interface de rede deverá receber um IP da faixa:

```text
10.24.82.X
```

Exemplo:

```text
10.24.82.120
```

---

# 🔎 PASSO 9 — Testar Conectividade

Execute:

```bash
ping 10.24.82.1
```

ou

```bash
ping google.com
```

Se houver resposta:

✅ Rede funcionando corretamente.

---

# 🔐 PASSO 10 — Verificar Serviço SSH

Verifique se o SSH está ativo:

```bash
sudo systemctl status ssh
```

---

# ✅ Resultado Esperado

Deve aparecer algo semelhante:

```text
active (running)
```

---

# 🖧 PASSO 11 — Acessar Remotamente via SSH

No Windows 11:

1. Abra o:

```text
PowerShell
```

2. Execute:

```powershell
ssh usuario@IP_DA_VM
```

Exemplo:

```powershell
ssh aluno@10.24.82.120
```

---

# 🔑 Primeiro Acesso SSH

Na primeira conexão aparecerá:

```text
Are you sure you want to continue connecting?
```

Digite:

```text
yes
```

Depois informe a senha.

---

# ✅ Resultado Final Esperado

Ao concluir a atividade você terá:

- ✅ Máquina virtual importada;
- ✅ Rede Bridge configurada;
- ✅ VM conectada na rede do laboratório;
- ✅ IP válido na rede `10.24.82.0/24`;
- ✅ Acesso remoto SSH funcionando.

---

# 📌 Dicas Importantes

## ⚠️ Caso a VM não receba IP

Execute:

```bash
sudo dhclient
```

---

## ⚠️ Caso o SSH não esteja ativo

Execute:

```bash
sudo systemctl enable ssh
sudo systemctl start ssh
```

---

# 🧾 Resumo Rápido

| Etapa | Ação |
|---|---|
| 1 | Abrir VirtualBox |
| 2 | Importar arquivo `.ova` |
| 3 | Configurar rede Bridge |
| 4 | Iniciar VM |
| 5 | Verificar IP |
| 6 | Testar SSH |

---

# 👨‍🏫 Observação Final

Essa máquina virtual será utilizada durante as aulas práticas de Inteligência Artificial aplicada a Redes de Computadores, portanto recomenda-se:

- Não alterar configurações críticas da VM;
- Não remover pacotes instalados pelo professor;
- Sempre desligar corretamente o sistema.

---

# ✅ Fim do Guia
