# Procedimento de Importação da Máquina Virtual (OVA) Ubuntu Server 22.04.4 LTS no Oracle VirtualBox 7.2

## Objetivo

Documentar o processo de importação da imagem da Máquina Virtual (OVA) do GNU/Linux Ubuntu Server 22.04.4 LTS no Oracle VirtualBox versão 7.2, executando no Microsoft Windows 11, utilizando o modo de rede Bridge (Ponte) para permitir acesso remoto via SSH na rede do cliente.

---

# Requisitos

| Item | Descrição |
|---|---|
| 💻 Sistema Operacional | Microsoft Windows 11 |
| 🖥️ Virtualizador | Oracle VirtualBox 7.2 |
| 📦 Imagem Virtual | Ubuntu Server 22.04.4 LTS (.OVA) |
| 🌐 Rede | Rede física com acesso DHCP |
| 🔌 Adaptador de Rede | Placa de rede física ativa no computador local |

---

# Etapa 01 — Abrir o Oracle VirtualBox

1. Clique no botão **Iniciar** do Windows.
2. Pesquise por **Oracle VM VirtualBox**.
3. Abra o aplicativo.

### Exemplo Visual

| Ação | Descrição |
|---|---|
| 📂 Menu | Iniciar |
| 🔎 Pesquisar | Oracle VM VirtualBox |
| ▶️ Executar | Abrir o VirtualBox |

---

# Etapa 02 — Importar a Máquina Virtual OVA

1. No menu superior do VirtualBox, clique em:

```text
Arquivo → Importar Appliance
```

2. Na janela de importação:
   - Clique em **Selecionar Arquivo**.
   - Localize o arquivo `.OVA` do Ubuntu Server 22.04.4 LTS.
   - Clique em **Abrir**.

3. Após selecionar o arquivo:
   - Clique em **Próximo**.

---

# Etapa 03 — Revisar as Configurações da Appliance

Na tela de configurações da appliance:

| Configuração | Ação Recomendada |
|---|---|
| 📛 Nome da VM | Validar nome da máquina virtual |
| 💾 Pasta Base | Confirmar local de armazenamento |
| 🧠 Memória RAM | Validar quantidade disponível |
| ⚙️ CPUs | Validar quantidade configurada |

1. Após revisar as informações:
   - Clique em **Finalizar**.

2. Aguarde o processo de importação.

### Observação

⏳ O tempo de importação depende do desempenho do computador e do tamanho da imagem OVA.

---

# Etapa 04 — Validar a Máquina Virtual Importada

Após finalizar a importação:

1. Verifique se a máquina virtual aparece na lista lateral esquerda do VirtualBox.
2. Confirme se o status da VM está como:

```text
Desligada
```

---

# Etapa 05 — Configurar Rede em Modo Bridge (Ponte)

1. Selecione a máquina virtual importada.
2. Clique em:

```text
Configurações → Rede
```

3. Na aba **Adaptador 1**:

| Configuração | Valor |
|---|---|
| ✅ Habilitar Placa de Rede | Ativado |
| 🌐 Conectado a | Placa em modo Bridge |
| 🔌 Nome | Selecionar adaptador físico ativo da rede local |

4. Após configurar:
   - Clique em **OK**.

---

# Etapa 06 — Iniciar a Máquina Virtual

1. Selecione a máquina virtual.
2. Clique em:

```text
Iniciar
```

3. Aguarde o carregamento do GNU/Linux Ubuntu Server.

---

# Etapa 07 — Validar Comunicação na Rede

Após iniciar a VM:

1. Verifique se a máquina virtual recebeu endereço IP da rede do cliente.
2. Confirmar que o endereço IP pertence à mesma faixa da rede local.

### Exemplo

| Equipamento | Exemplo de IP |
|---|---|
| 💻 Desktop Local | 192.168.0.10 |
| 🖥️ Ubuntu Server VM | 192.168.0.20 |

---

# Etapa 08 — Validar Acesso Remoto SSH

A partir de outro computador da rede:

1. Abrir terminal ou PowerShell.
2. Executar:

```bash
ssh usuario@IP_DA_VM
```

### Exemplo

```bash
ssh administrador@192.168.0.20
```

---

# Observações Gerais

| ⚠️ Observação | Descrição |
|---|---|
| 🌐 Rede Bridge | A VM dependerá da rede física disponível no ambiente |
| 🔌 Adaptador Correto | Selecionar sempre a placa física conectada à rede |
| 📡 DHCP | Necessário existir servidor DHCP ativo na rede |
| 🏢 Ambiente Corporativo | Algumas redes possuem restrições de segurança para novos dispositivos |
| 🔄 Mudança de Ambiente | Ao utilizar em outra rede, validar novamente o adaptador Bridge |
| 🛡️ Políticas da Rede | Redes corporativas podem bloquear comunicação SSH automaticamente |
| 💾 Espaço em Disco | Garantir espaço suficiente antes da importação da OVA |
| ⚙️ Compatibilidade | Validar compatibilidade da versão do VirtualBox com a imagem OVA |

---

# Finalização

| Informação | Valor |
|---|---|
| 📅 Data da Execução | 27/05/2026 |
| ⏰ Hora da Execução | 16:20:19 |
| 🖥️ Plataforma | Microsoft Windows 11 |
| 📦 Virtualizador | Oracle VirtualBox 7.2 |
| 🐧 Sistema Operacional | Ubuntu Server 22.04.4 LTS |

