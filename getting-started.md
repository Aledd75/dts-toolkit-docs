# Guia de Início Rápido

## Requisitos do Sistema
* **Sistema Operacional:** Windows 10 ou Windows 11 (x64).
* **Permissões:** É obrigatório executar como **Administrador** (o script verifica e solicita elevação).
* **Internet:** Necessária para validação inicial, Winget e downloads de softwares.

## Instalação e Execução

O DTS Toolkit é **portátil** (Portable), não deixando rastros de instalação convencional.

1.  Baixe o arquivo `DTS-Toolkit_v1.0.exe` (ou `.ps1`).
2.  Clique com o botão direito no arquivo.
3.  Selecione **Executar como Administrador**.

!!! warning "SmartScreen e Antivírus"
    Como o toolkit manipula configurações profundas (Registro, Serviços, Boot), o Windows SmartScreen pode exibir um alerta. Clique em "Mais informações" > "Executar mesmo assim".

## Primeiro Acesso e Licença

Ao abrir pela primeira vez, o sistema realizará as seguintes verificações:

1.  **Criação de Registro:** Configura as chaves em `HKCU:\Software\DadaltToolkitConfig`.
2.  **Ativação Trial:** Uma mensagem informará o início do período de testes de **3 dias**.
3.  **Validação de Ambiente:** Detecta se o usuário é Administrador e se o ambiente é corporativo (Domínio).

**Nota:** Se a licença expirar, o software bloqueará o acesso às ferramentas e solicitará a chave de ativação anual.