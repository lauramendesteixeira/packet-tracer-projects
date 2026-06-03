# Lab 03 - Interligação de Duas Redes com Dois Roteadores e DHCP (Packet Tracer)

Neste laboratório foi criada uma topologia composta por duas redes locais (LANs) interligadas por dois roteadores. Cada rede possui um servidor DHCP responsável pela distribuição automática de endereços IP aos hosts.

Foram utilizados:

- 2 switches Cisco 2960
- 2 roteadores Cisco 2621XM
- 2 servidores DHCP
- 6 PCs (3 em cada rede)

<img width="782" height="404" alt="2" src="https://github.com/user-attachments/assets/b09cd482-f904-4910-bdeb-f02ff311d584" />

## Configuração realizada

- Criação de duas redes independentes
- Configuração de servidores DHCP
- Distribuição automática de endereços IP
- Configuração das interfaces FastEthernet dos roteadores
- Configuração das interfaces Serial para comunicação entre roteadores
- Configuração do protocolo RIP
- Teste de conectividade entre redes distintas

## Endereçamento IP

### Rede 1

- Rede: 192.168.0.0/24
- Gateway: 192.168.0.1
- Servidor DHCP: 192.168.0.5
- Hosts distribuídos via DHCP:
  - 192.168.0.10
  - 192.168.0.11
  - 192.168.0.12

### Rede 2

- Rede: 10.0.0.0/24
- Gateway: 10.0.0.1
- Servidor DHCP: 10.0.0.5
- Hosts distribuídos via DHCP:
  - 10.0.0.10
  - 10.0.0.11
  - 10.0.0.12

### Rede Serial entre Roteadores

- Router0 Serial: 200.100.10.1
- Router1 Serial: 200.100.10.2

## Configuração dos Servidores DHCP

Cada servidor foi configurado com endereço IP estático e serviço DHCP habilitado.

### Servidor da Rede 1

- IP: 192.168.0.5
- Gateway: 192.168.0.1
- DNS: 192.168.0.6
- Início da distribuição DHCP: 192.168.0.10

### Servidor da Rede 2

- IP: 10.0.0.5
- Gateway: 10.0.0.1
- DNS: 10.0.0.6
- Início da distribuição DHCP: 10.0.0.10

## Configuração dos Roteadores

### Router0

FastEthernet:

- 192.168.0.1 /24

Serial:

- 200.100.10.1 /24

### Router1

FastEthernet:

- 10.0.0.1 /24

Serial:

- 200.100.10.2 /24

## Configuração de Roteamento

Foi utilizado o protocolo RIP para permitir a comunicação entre as redes.

### Router0

Redes anunciadas:

- 192.168.0.0
- 200.100.10.0

### Router1

Redes anunciadas:

- 10.0.0.0
- 200.100.10.0

## Tipos de Cabos Utilizados

- PC para Switch: Copper Straight-Through
- Servidor para Switch: Copper Straight-Through
- Switch para Router: Copper Straight-Through
- Router para Router: Serial DCE/DTE

## Teste de Conectividade

Após a configuração dos roteadores e do protocolo RIP, foi possível realizar comunicação entre dispositivos de redes diferentes.

Exemplo:

```bash
ping 10.0.0.12
```

## Referência

Exercício baseado em:

https://youtu.be/fEx_qPy5XZY?si=393gDuQQDVHyB1y-
