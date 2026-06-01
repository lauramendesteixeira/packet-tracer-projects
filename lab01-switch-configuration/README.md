### Lab 01 - Configuração Básica de Switch

Neste laboratório foram realizadas as seguintes configurações:

- Alteração do hostname
- Configuração da senha privilegiada (enable secret)
- Criptografia de senhas
- Configuração do console
- Configuração de acesso Telnet
- Configuração de endereço IP na VLAN
- Configuração de banner MOTD
- Salvamento da configuração

**Arquivo:** `lab01-switch-configuration.pkt`

## Comandos Utilizados

### Alteração do hostname

```bash
enable
configure terminal
hostname IPCiscoSwitch
```

### Configuração da senha privilegiada

```bash
enable secret ipcisco
```

### Criptografia das senhas

```bash
service password-encryption
```

### Configuração do console

```bash
line console 0
password cisco123
login
exec-timeout 10 15
logging synchronous
history size 10
```

### Configuração do acesso Telnet

```bash
line vty 0 15
password cisco123
login
exec-timeout 10 15
logging synchronous
history size 10
```

### Configuração do endereço IP da VLAN

```bash
interface vlan1
ip address 10.0.0.1 255.255.255.0
exit
```

### Configuração do banner MOTD

```bash
banner motd #
Unauthorized access is forbidden#
```

### Salvamento da configuração

```bash
exit
write
```

## O que aprendi

- Como acessar os modos de configuração do Cisco IOS
- Como alterar o hostname de um switch
- Como configurar senhas locais
- Como habilitar acesso via console e Telnet
- Como configurar um endereço IP de gerenciamento em uma VLAN
- Como criar uma mensagem MOTD
- Como salvar configurações permanentemente

## Arquivo

`lab01-switch-configuration.pkt`

## Referência

Exercício baseado em:

https://ipcisco.com/lesson/switch-configuration-on-cisco-packet-tracer/
