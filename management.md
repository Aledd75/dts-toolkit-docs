# Gestão & Diagnóstico

Ferramentas focadas no gerenciamento de aplicativos, arquivos do usuário e integridade do software.

## Deep Uninstaller (Desinstalação Profunda)
Este módulo substitui o "Adicionar ou Remover Programas" com recursos forenses:

1.  **Smart Uninstall:** Tenta desinstalar via Winget, MSIExec ou string nativa. Se falhar ou abrir janelas, detecta e aguarda intervenção do usuário.
2.  **Proteção de Jogos:** O script detecta e **impede** a remoção acidental de Launchers (Steam, Epic, Battle.net, Riot, etc) para evitar perda de bibliotecas de jogos.
3.  **Varredura Forense:** Após a desinstalação, varre e deleta resíduos em:
    * `Program Files`, `ProgramData`, `AppData` (Local/Roaming).
    * Chaves de Registro em `HKLM` e `HKCU`.

## Gerenciador de Softwares e Bloatware
* **Instalador em Massa:** Lista JSON online (GitHub) com softwares essenciais (Navegadores, Runtimes, Ferramentas Dev).
* **Bloatware Remover:** Remove apps nativos (Xbox, Clima, Notícias, etc). Possui função de **Restaurar** apps removidos caso necessário.

## Backup & Restauração Inteligente
Sistema robusto utilizando `Robocopy` em background (Jobs):

* **Backup:** Permite selecionar pastas do perfil (Desktop, Documentos, Imagens, etc).
* **Restore:** Verifica o backup mais recente na pasta `Toolkit_Backup` em qualquer disco conectado.
* **Diferencial:** Copia apenas arquivos novos ou modificados, economizando tempo.

## Relatório de Hardware (HTML)
Gera um arquivo HTML rico visualmente contendo:
* Detalhes da RAM (Slots usados/livres).
* Saúde dos Discos e Partições.
* Status de Segurança (TPM, Secure Boot).
* Periféricos USB conectados.