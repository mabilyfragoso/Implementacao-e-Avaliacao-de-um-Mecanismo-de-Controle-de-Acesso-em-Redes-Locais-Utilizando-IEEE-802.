# Implementação e Avaliação de um Mecanismo de Controle de Acesso em Redes Locais Utilizando IEEE 802.1X e FreeRADIUS

## Descrição

Este projeto apresenta a implementação e avaliação de um mecanismo de controle de acesso baseado no padrão IEEE 802.1X utilizando o servidor FreeRADIUS em um ambiente de rede local simulado.

O objetivo é demonstrar como a autenticação baseada em portas pode aumentar a segurança da infraestrutura de rede, permitindo que apenas usuários devidamente autenticados obtenham acesso aos recursos disponíveis.

## Objetivos

* Implementar um ambiente de autenticação utilizando IEEE 802.1X.
* Configurar o FreeRADIUS para validação de credenciais.
* Simular clientes autenticados e não autenticados.
* Avaliar o comportamento do sistema diante de acessos autorizados e não autorizados.
* Demonstrar a atribuição dinâmica de VLANs conforme o perfil do usuário.

## Tecnologias Utilizadas

* CORE Emulator
* FreeRADIUS
* hostapd
* wpa_supplicant
* Linux
* IEEE 802.1X
* RADIUS
* VLANs IEEE 802.1Q

## Topologia da Rede

A topologia foi construída no CORE Emulator e composta pelos seguintes elementos:

* Servidor FreeRADIUS
* Autenticador (hostapd)
* Clientes autenticados
* Switch lógico com segmentação por VLAN
* VLAN 10 – Usuários do setor RH
* VLAN 99 – Usuários visitantes

<img width="491" height="507" alt="Captura de tela 2026-06-22 215906" src="https://github.com/user-attachments/assets/1f2a6052-8c3e-48ba-a255-b678a2a63a51" />


## Metodologia

1. Criação da topologia de rede.
2. Configuração dos endereços IP.
3. Validação da comunicação entre os dispositivos.
4. Implementação de um cenário sem autenticação.
5. Configuração do servidor FreeRADIUS.
6. Cadastro de usuários e definição de políticas de acesso.
7. Configuração do hostapd como autenticador IEEE 802.1X.
8. Configuração do wpa_supplicant para os clientes.
9. Realização dos testes de autenticação utilizando o comando radtest.
10. Avaliação dos resultados obtidos.

## Resultados

Os testes realizados demonstraram que:

* Usuários com credenciais válidas receberam a resposta Access-Accept.
* Usuários com credenciais inválidas receberam a resposta Access-Reject.
* O mecanismo de autenticação impediu acessos não autorizados.
* Foi possível segmentar usuários em VLANs distintas de acordo com as políticas definidas.

## Trabalhos Futuros

Como continuação deste estudo, recomenda-se:

* Avaliação de desempenho utilizando iPerf.
* Captura e análise de pacotes com tcpdump ou Wireshark.
* Integração com diretórios LDAP ou Active Directory.
* Expansão do ambiente para cenários corporativos maiores.
* Implementação de autenticação multifator.

## Autores

Amabile M. Fragoso (Curso de Sistemas de Informação)

Wesley P. Pereira (Curso de Sistemas de Informação)

