### Lab 02 - Configuração de Rede com Roteamento Básico (Packet Tracer)

Neste laboratório foi criada uma topologia com duas redes locais (LANs) conectadas por um roteador, permitindo comunicação entre diferentes sub-redes.

Foram utilizados:

- 2 switches Cisco 2960
- 1 roteador Cisco 1941
- 10 PCs (5 em cada rede)

<img width="785" height="290" alt="1" src="https://github.com/user-attachments/assets/7177763e-d171-4e59-8c0a-be9b14a936d0" />

## Configuração realizada:

- Criação de duas redes independentes
- Configuração de endereçamento IPv4
- Definição de gateway padrão nos hosts
- Interconexão entre redes através de roteador
- Teste de conectividade entre redes

## Endereçamento IP

### Rede 1
- Rede: 192.168.10.0/24
- Hosts: 192.168.10.1 até 192.168.10.5
- Gateway: 192.168.10.254

### Rede 2
- Rede: 192.168.20.0/24
- Hosts: 192.168.20.1 até 192.168.20.5
- Gateway: 192.168.20.254

## Conceito do Roteador

O roteador foi configurado com duas interfaces:

- Interface para Rede 1: 192.168.10.254
- Interface para Rede 2: 192.168.20.254

Ele atua como dispositivo de camada 3 (comunicação entre redes diferentes).

## Tipos de cabos utilizados

- PC para Switch: Copper Straight-Through
- Switch para Router: Copper Straight-Through

## Teste de conectividade

Foi utilizado o comando `ping` para verificar comunicação entre hosts de redes diferentes.

Exemplo:

```bash id="lab02ping"
ping 192.168.20.1
```

## Arquivo

`lab02-basic-internetwork-routing`

## Referência

Exercício baseado em:

https://youtu.be/-e5oM07Oed0?si=7FV6WuX1M1zs5gJu
