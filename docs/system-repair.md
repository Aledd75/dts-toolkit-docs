# Sistema & Reparo

O painel de Sistema e Reparo concentra o arsenal de recuperação do sistema operacional. Cada classe aqui atua diretamente no núcleo do Windows.

## DTMaintenance (Manutenção e Limpeza)
Subdividida em rotinas isoladas ou encadeadas:
* **Limpar Disco:** Invoca a limpeza nativa (`cleanmgr`) e esvazia silenciosamente as pastas `SoftwareDistribution`, `%TEMP%` e `Prefetch`.
* **CHKDSK:** O Scan Online lê a estrutura RAW em tempo real. O Offline programa o volume C: para reparo profundo no próximo boot.
* **DISM & SFC:** Usa os binários de imagem de implantação para restaurar a integridade da pasta `System32` corrompida.
* **Rotina Completa:** Um motor inteligente que para os serviços do Windows Update, executa Limpeza > CHKDSK > DISM > SFC sequencialmente, e reinicia a proteção.
 
## DTOptimizeSystem (Central de Otimização)
O módulo mais complexo do sistema. Apresenta dezenas de *tweaks* seguros com botão de Desfazer (`UNDO`).
* **Energia:** Força o plano "Ultimate Performance" e cria o *Wi-Fi Power Profile* (impedindo a placa de rede de dormir).
* **GPU & Gráficos:** Injeta o HAGS (Hardware Accelerated GPU Scheduling).
* **Privacidade:** Desativa a Telemetria da Microsoft e as Experiências do Consumidor.

## DTServiceRepair (A "Troca de Óleo" do Windows)
Restaura os valores de fábrica de **24 serviços vitais** do Windows (`mpssvc`, `wuauserv`, `WlanSvc`, `Audiosrv`, `Spooler`, etc.). Excelente para reviver PCs que pararam de dar som, conectar à rede ou imprimir devido a "otimizadores ruins" da internet.

## DTBootRepairManager (Reparo de Inicialização)
Interface para reconstruir blocos lógicos quebrados (Telas Azuis).
* Reconstrói o **BCD** (Boot Configuration Data) em discos MBR ou GPT.
* Restaura as partições ativas de recuperação (`WinRE`).

## DTDeepCleaner (Caçador de Resquícios)
Uma arma forense. Você digita uma palavra (Ex: "Avast") e o motor:
1. Verifica se o app consta como instalado e bloqueia se positivo.
2. Mata todos os processos associados.
3. Exclui instâncias em `Get-Service` usando `sc.exe delete`.
4. Varre pastas base (`ProgramData`, `AppData`) e muda o ACL (`takeown` / `icacls`) para destruir pastas teimosas à força.
5. Limpa árvores no Registro (`HKCU` e `WOW6432Node`).
6. Remove os atalhos.

## DTDownloadWindows & DTFixWinget (Ferramentas Essenciais)
* **Download de ISOs:** Módulo que conecta diretamente aos servidores da Microsoft para baixar ferramentas de criação de mídia do Windows 10 e 11, com *fallback* automático caso a rede falhe.
* **Reparar Winget:** Reinstala os provedores e dependências do Gerenciador de Pacotes do Windows caso ele tenha sido corrompido no sistema do cliente.