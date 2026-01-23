# Segurança e Rede

Ferramentas para proteção do endpoint, controle de acesso e conectividade.

## Reparo de Rede
Resolve problemas de conexão resetando a pilha TCP/IP.
* **Ações:** Reset de Winsock, Firewall, Flush DNS, ARP e Route.
* **Segurança de Domínio:** O script detecta se o PC está em um Domínio Active Directory. Se estiver, **ignora** alterações de DNS para não quebrar a confiança com o controlador de domínio.
* **Seletor de DNS:** Para usuários domésticos, permite troca rápida para Google (8.8.8.8) ou Cloudflare (1.1.1.1).

## Browser Optimizer (Segurança de Navegadores)
Módulo de varredura que fecha os navegadores e analisa extensões instaladas (Chrome, Edge, Brave, etc).
* Identifica extensões de terceiros.
* Permite remoção em massa de extensões suspeitas ou indesejadas.

## Gestão de Políticas (GPO Local)
Interface para aplicar restrições administrativas rapidamente (Kiosk Mode):
* **Bloqueio de USB:** Impede gravação em dispositivos de armazenamento externo.
* **Bloqueio de UI:** Desabilita Painel de Controle, CMD, Executar e força Tela de Bloqueio.

## Security Manager
* **Scan Rápido:** Varredura de processos ativos e áreas críticas usando o motor do Windows Defender ou Antivírus padrão.