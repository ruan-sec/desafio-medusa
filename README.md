# Auditoria de Credenciais e Análise de Autenticação em Ambiente Controlado (DIO)

Este repositório documenta o laboratório prático desenvolvido como parte do desafio de Cibersegurança da **Digital Innovation One (DIO)**. O projeto demonstra a arquitetura de um ambiente virtualizado isolado para avaliação de políticas de senha fracas, análise de tráfego HTTP e aplicação de medidas defensivas contra ataques automatizados de autenticação.

> **Aviso Ético:** Todas as atividades descritas neste documento foram executadas exclusivamente em ambiente virtualizado local e isolado (*Host-Only*), sem conexão com redes externas ou sistemas de terceiros.

---

## 1. Arquitetura do Ambiente

O laboratório foi estruturado no **Oracle VirtualBox** utilizando uma rede privada **Host-Only** (`192.168.56.0/24`) para garantir total isolamento:

* **Máquina de Análise (Atacante):** Kali Linux (`192.168.56.102`)
* **Máquina Alvo:** Metasploitable 2 (`192.168.56.101`)

### Estrutura do Repositório

```text
desafio-medusa/
├── images/
│   ├── 01-nmap-scan.jpg
│   ├── 02-medusa-ftp.jpg
│   ├── 03-ftp-validacao.jpg
│   ├── 04-dvwa-security-low.jpg
│   ├── 05-dvwa-cookies.jpg
│   └── 06-dvwa-http-headers.jpg
├── wordlists/
│   ├── users.txt
│   └── passwords.txt
└── README.md
