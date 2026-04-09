# 🔍 RELATÓRIO DE AUDITORIA - SERVIDOR UBUNTU SERVER 24.04 LTS

**Data da Auditoria:** 6 de Abril de 2026  
**Servidor Auditado:** wslinux01  
**Endereço IPv4:** 192.168.27.107  
**Usuário:** senac  
**Horário da Auditoria:** 00:45 UTC  

---

## 📋 INFORMAÇÕES DO SISTEMA OPERACIONAL

### Hardware
Hardware | Fabricante = innotek GmbH
Hardware | Modelo = VirtualBox
Hardware | Processador = x86-64
Hardware | Virtualização = Oracle VirtualBox
Hardware | Data do Firmware = 2006-12-01
Hardware | Máquina ID = 6953494f7e2842ea8e059dc421b288f0

**Tradução Simplificada:**  
Este servidor é uma máquina virtual hospedada em VirtualBox, rodando em processadores x86 (arquitetura de 64 bits). É uma configuração comum para laboratórios e ambientes de desenvolvimento, não recomendada para produção de alta disponibilidade.

---

### Sistema Operacional
SO | Distribuição = Ubuntu
SO | Versão = 24.04.4 LTS
SO | Codename = noble
SO | Release = 24.04
SO | Kernel = Linux 6.8.0-106-generic
SO | Arquitetura = x86-64
SO | Hostname = wslinux01

**Tradução Simplificada:**  
O servidor está executando a versão mais recente do Ubuntu LTS (Suporte de Longo Prazo), que receberá atualizações de segurança até 2036. LTS significa que o sistema é estável e confiável para uso produtivo.

---

## 🌐 CONFIGURAÇÃO DE REDE

### Interfaces de Rede
Rede | Hostname = wslinux01
Rede | Interface Primária = enp0s3
Rede | Endereço IPv4 = 192.168.27.107/20
Rede | Endereço IPv6 = fe80::a00:27ff:fe11:42e8/64
Rede | MAC Address = 08:00:27:11:42:e8
Rede | MTU = 1500
Rede | Gateway Padrão = 192.168.16.1
Rede | DHCP = Ativo
Rede | Estado = UP (Operacional)

### Roteamento
Rede | Rota Padrão = 192.168.16.1 (DHCP)
Rede | Rede Local = 192.168.16.0/20
Rede | DNS Primário = 8.8.8.8 (via rota)
Rede | DNS Secundário = 8.8.4.4 (via rota)

**Tradução Simplificada:**  
O servidor está conectado à rede usando configuração automática (DHCP). Ele recebe seu endereço IP automaticamente através do roteador (gateway 192.168.16.1). A máscara de rede /20 permite comunicação com até 4.094 outros computadores na mesma rede local. O IPv6 está configurado para suportar a nova versão do protocolo de internet.

---

## 🔌 SERVIÇOS DE REDE E PORTAS ABERTAS

### Serviços TCP (Portas de Escuta)
Serviço | Protocolo = TCP
Serviço | Porta 22 = SSH (Secure Shell - Acesso Remoto)
Serviço | Porta 80 = HTTP (Servidor Web - Apache)
Serviço | Porta 3000 = Aplicação Customizada
Serviço | Porta 3306 = MySQL (Banco de Dados)
Serviço | Porta 8080 = HTTP Alternativo (Aplicação Web)
Serviço | Porta 8888 = Aplicação Customizada
Serviço | Porta 9091 = Aplicação Customizada (Monitor)
Serviço | Porta 9100 = Prometheus Node Exporter
Serviço | Porta 33060 = MySQL X Protocol (Acesso Avançado)
Serviço | Porta 53 = DNS (Resolução de Nomes) - Loopback

### Serviços UDP (Portas de Escuta)
Serviço | Protocolo = UDP
Serviço | Porta 53 = DNS (Resolução de Nomes)
Serviço | Porta 68 = DHCP (Configuração de Rede)

**Tradução Simplificada:**  
O servidor está executando vários serviços de rede:
- **SSH (Porta 22)**: Permite acesso remoto seguro ao servidor via linha de comando
- **HTTP (Portas 80, 8080)**: Servidores web para exibir páginas e aplicações internet
- **MySQL (Porta 3306)**: Banco de dados para armazenar informações estruturadas
- **Aplicações Customizadas (Portas 3000, 8888, 9091)**: Programas específicos desenvolvidos para este ambiente
- **Prometheus (Porta 9100)**: Ferramenta de monitoramento para acompanhar a saúde do servidor

---

## 💾 ESPAÇO EM DISCO

### Discos Conectados
Disco | Total = 47GB (volume principal)
Disco | Usado = 11GB
Disco | Disponível = 35GB
Disco | Percentual Utilização = 24%
Disco | Boot = 2GB (total)
Disco | Boot Usado = 198MB
Disco | Boot Disponível = 1.6GB
Disco | Percentual Boot = 11%
Disco | Swap (Virtual) = 2.0GB (não utilizado)

**Tradução Simplificada:**  
O servidor possui espaço de disco suficiente. Apenas 24% do disco principal está sendo usado, deixando 35GB livres para crescimento futuro. O disco de boot está em bom estado. A memória virtual (swap) está disponível como fallback.

---

## 💻 MEMÓRIA E PROCESSAMENTO

### Memória RAM
Memória | Total = 1.9GB
Memória | Utilizada = 1.2GB
Memória | Livre = 74MB
Memória | Em Cache = 820MB
Memória | Disponível = 740MB
Memória | Percentual Utilização = 63%

**Tradução Simplificada:**  
O servidor tem 1.9GB de memória RAM. Atualmente está utilizando 1.2GB, deixando cerca de 740MB livres para novas operações. O cache de sistema (820MB) pode ser liberado se necessário. A utilização está moderada (63%).

---

## 📦 SOFTWARES INSTALADOS

### Aplicações Críticas
Aplicação | Apache Web Server = 2.4.58 (instalado e ativo)
Aplicação | MySQL Server = 8.0.45 (instalado e ativo)
Aplicação | PHP/mod_php = 8.3.6 (instalado)
Aplicação | Tomcat Application Server = em /opt/tomcat (instalado e ativo)
Aplicação | Java OpenJDK = 1.21.0 (instalado)

**Tradução Simplificada:**  
O servidor executa uma pilha completa de aplicação web:
- **Apache**: Servidor web para servir páginas internet
- **MySQL**: Banco de dados para aplicações
- **PHP**: Linguagem de programação para web
- **Tomcat**: Servidor de aplicações Java
- **Java**: Máquina virtual para executar aplicações modernas

---

## 🟢 STATUS DOS SERVIÇOS

### Serviços em Execução
Serviço | Apache2 = Ativo [running]
Serviço | Apache2 PID = 975 (processo principal)
Serviço | Apache2 Memória = 24.9MB
Serviço | Apache2 Workers = 5 (www-data)

Serviço | MySQL = Ativo [running]
Serviço | MySQL PID = 878
Serviço | MySQL Memória = 573.6MB
Serviço | MySQL Status = Server is operational

Serviço | Tomcat = Ativo [running]
Serviço | Tomcat PID = 781
Serviço | Tomcat Memória = 234.6MB
Serviço | Tomcat JVM = Java 21 OpenJDK

**Tradução Simplificada:**  
Todos os serviços principais estão funcionando normalmente:
- Apache: Consumindo 24.9MB de memória (normal)
- MySQL: Consumindo 573.6MB de memória (esperado para banco de dados)
- Tomcat: Consumindo 234.6MB de memória com JVM Java 21

---

## 🔐 SEGURANÇA SSH

### Configuração de SSH
Segurança | Porta SSH = 22
Segurança | Protocolo SSH = 2 (versão segura)
Segurança | Listen Address = 0.0.0.0 (todas as interfaces)
Segurança | Autenticação = Password + Public Key (Dual)
Segurança | PermitRootLogin = No (root não pode conectar)
Segurança | AllowUsers = senac (apenas este usuário)
Segurança | AllowGroups = senac (apenas este grupo)
Segurança | DenyUsers = root
Segurança | DenyGroups = root
Segurança | Ciphers = aes128-ctr, aes192-ctr, aes256-ctr
Segurança | Log Level = VERBOSE
Segurança | Modo Estrito = Ativo

**Tradução Simplificada:**  
A configuração SSH está adequadamente protegida:
- Root não pode se conectar diretamente (melhor prática)
- Apenas o usuário 'senac' é permitido (acesso restrito)
- Suporta chaves públicas (mais seguro que senha)
- Criptografia forte (AES) é utilizada
- Logs detalhados são mantidos para auditoria

---

## 📊 ATUALIZAÇÕES DISPONÍVEIS

### Status de Atualizações
Atualizações | Total Disponíveis = 72
Atualizações | Atualizações Normais = 52
Atualizações | Atualizações de Segurança = 20
Atualizações | ESM Apps Disponíveis = 3
Atualizações | Última Verificação = 6 de Abril de 2026

**Atualizações Críticas de Segurança Encontradas:**
- bind9 (DNS) - Vulnerabilidades de segurança corrigidas
- libfwupd2 (Firmware) - Atualizações de segurança
- libnss-systemd (Sistema) - Atualizações de segurança

**Tradução Simplificada:**  
O servidor tem 72 atualizações disponíveis, dos quais 20 são atualizações de segurança importantes. É recomendado aplicar essas atualizações regularmente para manter o servidor protegido contra vulnerabilidades conhecidas.

---

# 🚨 ANÁLISE DE SEGURANÇA E VULNERABILIDADES

## Problemas Identificados

### 1. ⚠️ SEVERIDADE: ALTO
**Problema:** Múltiplas Portas Abertas e Expostas  
**Descrição:** O servidor tem 13 portas TCP abertas, incluindo serviços customizados (portas 3000, 8888, 9091) que não têm firewall intermediário.  
**Impacto:** Exposição a ataques diretos na rede, possível acesso não autorizado aos serviços.  
**Recomendação:** Implementar firewall (ufw) para restringir acesso apenas a portas necessárias. Bloquear portas 3000, 8888, 9091 do acesso externo.  
**Comando Sugerido:**  
```bash
sudo ufw enable
sudo ufw default deny incoming
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw deny 3000/tcp
sudo ufw deny 8888/tcp
sudo ufw deny 9091/tcp
```

---

### 2. ⚠️ SEVERIDADE: ALTO
**Problema:** MySQL Exposto Globalmente  
**Descrição:** MySQL está escutando em 0.0.0.0:3306 (todas as interfaces), permitindo acesso de qualquer máquina da rede.  
**Impacto:** Risco crítico de segurança - possível acesso não autorizado ao banco de dados e execução de SQL injection.  
**Recomendação:** Modificar configuração MySQL para escutar apenas em localhost (127.0.0.1).  
**Comando Sugerido:**  
```bash
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
# Alterar: bind-address = 127.0.0.1
sudo systemctl restart mysql
```

---

### 3. ⚠️ SEVERIDADE: ALTO
**Problema:** Autenticação SSH com Senha Habilitada  
**Descrição:** Tanto a autenticação por senha quanto por chave pública estão ativadas. Senhas são vulneráveis a ataques de força bruta.  
**Impacto:** Possibilidade de acesso não autorizado através de força bruta ou phishing.  
**Recomendação:** Desabilitar autenticação por senha e usar apenas chaves públicas (SSH key-based).  
**Comando Sugerido:**  
```bash
sudo nano /etc/ssh/sshd_config
# Alterar: PasswordAuthentication no
# Manter: PubkeyAuthentication yes
sudo systemctl restart ssh
```

---

### 4. ⚠️ SEVERIDADE: MÉDIO
**Problema:** Atualizações de Segurança Críticas Pendentes (20 disponíveis)  
**Descrição:** 20 atualizações de segurança aguardando instalação, incluindo bind9, libfwupd2, libnss-systemd.  
**Impacto:** Vulnerabilidades conhecidas não corrigidas expõem o servidor a ataques.  
**Recomendação:** Aplicar atualizações de segurança imediatamente.  
**Comando Sugerido:**  
```bash
sudo apt update
sudo apt upgrade -y
sudo apt install unattended-upgrades
sudo dpkg-reconfigure unattended-upgrades
```

---

### 5. ⚠️ SEVERIDADE: MÉDIO
**Problema:** Utilização Elevada de Memória (63% usada, 74MB livres)  
**Descrição:** Memória RAM utilizada em 63%, deixando apenas 740MB disponíveis. MySQL consome 573.6MB. Risco de degradação de desempenho.  
**Impacto:** Possível lentidão em horários de pico, swap ativo pode prejudicar performance.  
**Recomendação:** Aumentar memória RAM de 1.9GB para 4GB ou 8GB, ou otimizar configurações de MySQL.  
**Comando Sugerido (Otimização MySQL):**  
```bash
# Ajustar max_connections e memory usage
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
# Reduzir max_connections de 151 para 50
# Aumentar innodb_buffer_pool_size
```

---

### 6. ⚠️ SEVERIDADE: MÉDIO
**Problema:** Serviço DNS Resolvendo 8.8.8.8 e 8.8.4.4 (Google)  
**Descrição:** O servidor está utilizando DNS público (Google) ao invés de DNS privado corporativo ou internal.  
**Impacto:** Possível vazamento de informação sobre domínios consultados, falta de controle DNS corporativo.  
**Recomendação:** Configurar DNS privado corporativo ou usar systemd-resolved com DNS seguro (Cloudflare 1.1.1.1 ou Quad9 9.9.9.9).  
**Comando Sugerido:**  
```bash
sudo nano /etc/systemd/resolved.conf
# Alterar: DNS=1.1.1.1 9.9.9.9
# Alterar: FallbackDNS=1.0.0.1 149.112.112.112
sudo systemctl restart systemd-resolved
```

---

### 7. 🟡 SEVERIDADE: BAIXO
**Problema:** ListenAddress Configurada para 0.0.0.0 (SSH)  
**Descrição:** SSH está escutando em 0.0.0.0 (todas as interfaces), permitindo acesso de qualquer rede.  
**Impacto:** Aumenta superfície de ataque para força bruta em SSH, porém com 'AllowUsers' restrito.  
**Recomendação:** Limitar ListenAddress a IP específico ou Interface específica.  
**Comando Sugerido:**  
```bash
sudo nano /etc/ssh/sshd_config
# Alterar: ListenAddress 192.168.27.107
# Ou: ListenAddress 127.0.0.1
sudo systemctl restart ssh
```

---

### 8. 🟡 SEVERIDADE: BAIXO
**Problema:** Prometheus Node Exporter Exposto na Porta 9100  
**Descrição:** Prometheus (ferramenta de monitoramento) está acessível sem autenticação na porta 9100.  
**Impacto:** Exposição de métricas detalhadas do servidor (CPU, memória, processos em execução) para qualquer pessoa na rede.  
**Recomendação:** Proteger acesso a Prometheus com firewall ou autenticação reversa (nginx com BasicAuth).  
**Comando Sugerido:**  
```bash
sudo ufw deny 9100/tcp
# Ou configurar acesso apenas de rede local
sudo ufw allow from 192.168.27.0/24 to any port 9100
```

---

## 📈 Resumo de Problemas por Severidade

| Severidade | Quantidade | Problemas |
|-----------|-----------|----------|
| 🔴 ALTO | 3 | Portas abertas, MySQL exposto, SSH com senha |
| 🟠 MÉDIO | 3 | Atualizações pendentes, RAM insuficiente, DNS público |
| 🟡 BAIXO | 2 | ListenAddress SSH, Prometheus exposto |

---

# ✅ RECOMENDAÇÕES DE MELHORIAS

## Prioridade 1 - Implementar Imediatamente (Próximas 24 horas)

1. **Ativar e Configurar Firewall (ufw)**
   ```bash
   sudo ufw enable
   sudo ufw default deny incoming
   sudo ufw allow 22/tcp
   sudo ufw allow 80/tcp
   sudo ufw allow 443/tcp
   ```

2. **Desabilitar SSH com Senha**
   ```bash
   sudo sed -i 's/^PasswordAuthentication yes/PasswordAuthentication no/' /etc/ssh/sshd_config
   sudo systemctl restart ssh
   ```

3. **Aplicar Atualizações de Segurança**
   ```bash
   sudo apt update
   sudo apt upgrade -y
   ```

---

## Prioridade 2 - Implementar em 1 Semana

4. **Configurar MySQL para Localhost**
   ```bash
   sudo sed -i 's/^bind-address.*/bind-address = 127.0.0.1/' /etc/mysql/mysql.conf.d/mysqld.cnf
   sudo systemctl restart mysql
   ```

5. **Aumentar Memória RAM**
   - Solicitar upgrade de 1.9GB → 4GB ou 8GB
   - Ou otimizar MySQL e aplicações

6. **Configurar Atualizações Automáticas**
   ```bash
   sudo apt install unattended-upgrades
   sudo dpkg-reconfigure unattended-upgrades
   ```

---

## Prioridade 3 - Implementar em 2 Semanas

7. **Implementar Backup Automático**
   - Backup diário de /var/www e /var/lib/mysql
   - Armazenamento em servidor remoto

8. **Configurar Monitoramento e Alertas**
   - Integrando Prometheus com Grafana
   - Alertas para CPU, memória e disco

9. **Implementar Logs Centralizados**
   - Enviar logs para servidor ELK (Elasticsearch, Logstash, Kibana)
   - Arquivo permanente para auditoria

10. **Configurar HTTPS/SSL**
    - Instalar Certbot e Let's Encrypt
    - Redirecionar HTTP → HTTPS

---

# 🎯 CONCLUSÃO

O servidor **wslinux01** está em **estado de funcionamento aceitável**, porém com **vulnerabilidades críticas de segurança** que devem ser corrigidas imediatamente:

✅ **Pontos Positivos:**
- Sistema operacional atualizado e estável (Ubuntu 24.04 LTS)
- Serviços principais funcionando corretamente
- Configuração SSH com restrições adequadas (AllowUsers)
- Espaço em disco disponível
- Hardware virtualizado facilita backup e migração

❌ **Pontos Críticos:**
- Múltiplas portas expostas sem proteção de firewall
- MySQL acessível globalmente (risco crítico)
- SSH com autenticação por senha ativada
- 20 atualizações de segurança aguardando instalação
- Memória RAM insuficiente para carga esperada

**Prioridade Máxima:** Implementar firewall e desabilitar acesso desprotegido ao MySQL nos próximos dias.

---

**Relatório Gerado:** 6 de Abril de 2026 - 00:45 UTC  
**Analista:** Sistema de Auditoria Automática  
**Próxima Auditoria Recomendada:** 13 de Abril de 2026
