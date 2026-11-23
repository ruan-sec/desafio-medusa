# Desafio Medusa

Laboratório que montei no VirtualBox para testar na prática como funciona um ataque de dicionário usando o Medusa e como proteger o servidor contra esse tipo de tentativa.

## Ambiente usado
* Kali Linux (máquina atacante)
* Ubuntu Server 192.168.3.150 e DVWA / Metasploitable 2 (alvos em rede isolada)
* Nmap e Medusa

## O que fiz no lab
1. Rodei o Nmap para mapear o IP do alvo e ver as portas abertas (SSH, FTP e HTTP).
2. Criei duas listas simples de usuários e senhas para o teste.
3. Executei o Medusa no Kali para testar o acesso ao serviço:

    medusa -h 192.168.3.150 -U usuarios.txt -P senhas.txt -M ssh

## O que aprendi (Defesa)
* Senhas fracas caem rápido se o servidor não tiver bloqueio de tentativas.
* Para evitar isso na prática: ativar o Fail2Ban para bloquear IPs após erros seguidos, desativar login por senha no SSH (usar chave Ed25519) e manter o firewall UFW ativo.
