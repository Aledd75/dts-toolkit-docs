# Guia de Início Rápido

## Requisitos do Sistema
* **Sistema Operacional:** Windows 10 ou Windows 11 (x64).
* **Permissões:** É necessário executar como **Administrador**.
* **Internet:** Necessária para baixar atualizações do Winget e Softwares.

## Instalação e Execução

O DTS Toolkit é **portátil** (Portable), ou seja, não instala arquivos no sistema.

1.  Baixe a versão mais recente no [GitHub Releases]().
2.  Clique com o botão direito no arquivo `DTS-Toolkit_v1.0.exe`.
3.  Selecione **Executar como Administrador**.

!!! warning "Aviso de Segurança"
    Como o toolkit manipula configurações profundas do sistema (Registro, Serviços, Boot), o Windows SmartScreen pode exibir um alerta. Clique em "Mais informações" > "Executar mesmo assim".
	
!!! info "Por que preciso executar como Admin?"
    Mesmo que seu usuário seja Administrador, o Windows limita o acesso de programas por segurança (UAC).
    
Como o **DTS Toolkit** realiza manutenções profundas (limpeza de disco, reparo de rede), ele precisa de permissão total para funcionar.
    
**Dica Pro:** Para evitar clicar com o botão direito toda vez:
1. Vá em **Propriedades** do arquivo `.exe`.
2. Na aba **Compatibilidade**, marque **Executar este programa como administrador**.

## Primeiro Acesso

Ao abrir, o sistema verificará automaticamente:
* Se você possui privilégios de Administrador.
* O status da licença (Trial ou Ativado).
* Criará automaticamente a pasta de logs no Desktop (`DTS_Logs`).