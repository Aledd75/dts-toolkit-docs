# Gestão & Diagnóstico

Ferramentas para gerenciar o ambiente do usuário e softwares.

## Deep Uninstaller
Diferente da desinstalação comum, este módulo realiza uma **varredura forense**:
1.  Executa o desinstalador padrão do software.
2.  Varre pastas (`Program Files`, `AppData`, `ProgramData`) em busca de sobras.
3.  Limpa chaves de registro órfãs (`HKLM` e `HKCU`).

## Gerenciador de Softwares
Interface conectada ao repositório **Winget** e lista JSON personalizada:
* **Instalação em Massa:** Selecione navegadores, ferramentas dev e jogos para instalar de uma vez.
* **Bloatware Remover:** Remove aplicativos pré-instalados do Windows (Xbox, Clima, Notícias, etc.) com segurança.

## Backup & Restauração
Sistema de backup inteligente utilizando `Robocopy`:
* **Backup:** Salva Desktop, Documentos, Imagens, etc.
* **Restore:** Restaura apenas arquivos novos ou alterados, preservando dados existentes.