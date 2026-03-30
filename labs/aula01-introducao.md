🧩 1. Importar a imagem (.OVA)

📁 Arquivo: Downloads\UbuntuServer-OnPremises.ova

Abra o VirtualBox<br>
Clique em 📂 Arquivo → Importar Appliance<br>
Clique em 📁 e selecione:<br>
UbuntuServer-OnPremises.ova<br>
Clique em ➡️ Avançar<br>
Revise as configurações (pode manter padrão)<br>
Clique em ✅ Importar<br>
Aguarde o processo finalizar<br>

⚙️ 2. Ajustar configurações da VM

Após importar:

Selecione a VM UbuntuServer-OnPremises
Clique em ⚙️ Configurações
🧠 Sistema
Verifique RAM e CPU (não alterar se já estiver definido pelo professor)
🌐 3. Configurar rede em modo Bridge (Ponte)
Vá em 🌐 Rede
Em Adaptador 1:
✔️ Marcar: Habilitar placa de rede
🔽 Conectado a: Bridge Adapter (Placa em modo Bridge)
🔽 Nome:
Escolher a placa Ethernet cabeada (ex: Ethernet, Realtek, Intel)
Clique em OK

📌 Objetivo: A VM receberá um IP da mesma rede do laboratório

▶️ 4. Iniciar a máquina virtual
Selecione a VM
Clique em ▶️ Iniciar
Aguarde o boot do Ubuntu Server 22.04.4 LTS
🔐 5. Verificar IP da VM

No terminal da VM:

Digite:

ip a

🔎 Procure algo como:

inet 192.168.x.x

📌 Esse será o IP para acesso remoto

💻 6. Acesso remoto via SSH

No computador host (Windows 11):

Abra o Prompt de Comando ou PowerShell
Execute:
ssh usuario@IP_DA_VM

📌 Exemplo:

ssh aluno@192.168.0.50
Digite a senha quando solicitado
🧪 7. Teste de conectividade (opcional)

No Windows:

ping IP_DA_VM

Se responder → rede OK ✅

⚠️ Observações importantes
🔌 Use rede cabeada (Ethernet) — Wi-Fi pode não funcionar corretamente em Bridge
🔐 Verifique se o SSH está ativo na VM:
sudo systemctl status ssh
Caso não esteja:
sudo systemctl start ssh
✅ Resultado esperado
VM importada com sucesso
Rede em modo Bridge funcionando
IP válido na rede do laboratório
Acesso remoto via SSH operacional

---

Segundo Prompt

---

