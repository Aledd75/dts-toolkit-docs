# Gestão & Diagnósticos

Ferramentas focadas na governança do sistema, instalação em massa de aplicativos e testes de hardware em laboratório.

## DTSoftwares & DTBloatwares (Gestão de Pacotes)
* **Instalador em Massa:** Interface limpa que consome a API do `Winget` para instalar navegadores, ferramentas e runtimes essenciais com um clique, de forma totalmente silenciosa.
* **Remoção de Bloatwares:** Varre e remove nativos indesejados do Windows (Cortana, Xbox, Hub de Feedback, etc.) localmente do disco rígido para liberar espaço e processamento.

## DTDeepUninstaller (Desinstalação Profunda)
Módulo cirúrgico que substitui o painel nativo do Windows.
* **Proteção Gamers:** Possui uma "Whitelist" embutida que **trava** a desinstalação caso o usuário tente remover Steam, Epic Games, Riot ou Battle.net, evitando a remoção de terabytes de jogos.
* **Caça a Registros:** Após desinstalar de forma limpa, atua limpando as pontas soltas na árvore do Windows, somente após confirmada a remoção do aplicativos.

## DTBackupFiles & DTRestoreFiles
A interface gráfica de espelhamento baseada no poderoso `RoboCopy`.
* Copia diretórios vitais do usuário para a pasta `/Toolkit_Backup/` sempre na mesma pasta onde o DT Toolkit estiver sendo executado (Geralmente, Pen Drive ou SSD Portátil).
* **Efeito Diferencial:** Só copia arquivos que foram modificados ou adicionados desde o último backup, economizando horas de trabalho.

## DTPasswordManager (SAM Control)
Ferramenta para redefinir o acesso à máquina sem formatação:
* Redefine contas locais, respeitando a permanência do PIN (Windows Hello).
* **Gatilho Root:** Permite Habilitar/Desabilitar o usuário Oculto "Administrador" (SID-500) em caso de quebra total do sistema.

## DTConsistencyChecker (Auditoria de Sistema)
O verdadeiro "Blue Team". Um script de inspeção profunda que gera relatórios HTML:
* **Hijacking:** Verifica valores ilícitos em `AppInit_DLLs` e `Userinit`.
* **IFEO Blocks:** Descobre se o Gerenciador de Tarefas ou o Regedit foram "sequestrados".
* **Segurança:** Analisa falhas no UAC e **Exclusões Maliciosas** injetadas no Windows Defender.

## DTHardwareDiagnostics & HwMonitor (Raio-X Físico)
Submete o equipamento a testes de estresse:
* **CPU Stress:** Força o `Win32_Processor` e varre o Log de Eventos do Windows (WHEA) caçando falhas de energia/cache.
* **RAM Test:** Testa blocos virtuais procurando vazamentos e "Bad Sectors" na memória.
* **Discos (SMART):** Alerta sobre setores realocados ou temperatura crítica no SSD/HDD.
* **Monitor Térmico:** Baixa e executa a versão portátil mais recente do *HWMonitor* para leitura precisa de temperaturas em tempo real.

## DTServiceOrder (Ordem de Serviço Inteligente)
Gera um relatório profissional em PDF contendo dados da máquina e da licença. O sistema possui inteligência para bloquear a geração do PDF caso nenhuma ferramenta de manutenção tenha sido rodada na sessão atual, evitando relatórios vazios.