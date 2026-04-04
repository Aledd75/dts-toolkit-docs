# Segurança e Rede

Ferramentas projetadas para endurecimento (Hardening), remoção rápida de ameaças e estabilidade de conexão.

## DTSecurityManager (Caça a Malwares)
Lança o motor do Microsoft Defender através de Runspace cego (sem janelas nativas):
* **Hardening Instantâneo:** Antes de scannear, ele eleva a proteção para `High` (Bloqueio em Nuvem) e liga a Proteção de PUA (Software Potencialmente Indesejado).
* **Offline Trigger:** Se o processo `Get-MpThreat` retornar um vírus ativo e teimoso, o Toolkit lança um alerta pedindo a reinicialização da máquina para executar o "Windows Defender Offline Scan" a nível de boot (limpando rootkits).

## DTWebFilterManager (DNS e Blindagem)
Constrói o Grid através da Fábrica Visual (`DTUIFactory`) permitindo forçar servidores DNS nas placas ativas de Ethernet/Wi-Fi:
* **Perfís Atuais:** Google (Estabilidade), Cloudflare 1.1.1.1 (Ping Baixo para Jogos), Quad9 (Segurança Corporativa Extrema), AdGuard (Remoção de Anúncios nativa) e Family Shields (Bloqueio de Conteúdo Adulto).
* Ao clicar em *Aplicar*, limpa instantaneamente o Cache (`Clear-DnsClientCache`) validando a alteração.

## DTPoliciesManager (GPO Local & Kiosk Mode)
Interface robusta para alterar políticas restritivas do computador na hora:
* **Bloqueio de USB Mass Storage:** Trava pendrives (Ideal para lojas).
* **Bloqueio Administrativo:** Desativa o Painel de Controle, CMD e o "Executar", transformando o PC em um terminal restrito.

## DTNetworkRepair (Ataque às Redes)
Quando o sistema perde a capacidade de identificar o IP (famoso cabo amarelo):
* **Auditoria de Domínio:** O script detecta automaticamente se a máquina pertence a um `Active Directory`. Se sim, a troca forçada de DNS é abortada para não destruir a conectividade com os servidores locais (File Servers/Printers).
* Libera os caches ARP, reconstrói o catálogo Winsock (`netsh winsock reset`) e reinicia o DHCP.