# Guia de Início Rápido

## Requisitos do Sistema
* **Sistema Operacional:** Windows 10 ou Windows 11 (x64). Modo WinPE é suportado em módulos limitados.
* **Privilégios:** É obrigatório executar como **Administrador**. O motor do `DTCore` audita a sessão; se não for admin, o programa solicitará elevação via UAC automaticamente.
* **Internet:** Necessária para **validação da licença/assinatura** na abertura do programa, além do uso de módulos online como `DTDownloadWindows`, relatórios JSON do Winget e sincronização do status do módulo `DTNetworkRepair`.

## Instalação e Execução

O DT Toolkit é **100% portátil** (Portable) e opera inteiramente na memória RAM (`Runspace`), não deixando rastros de instalação convencional no disco.

1.  Baixe o arquivo empacotado `DTToolkit.exe` (direto do nosso repositório oficial).
2.  Clique com o botão direito no arquivo e selecione **Executar como Administrador**.

"SmartScreen e Antivírus"
    Como o toolkit manipula configurações em Kernel e System32 (Registro de Serviços, Boot e Políticas GPO), o Windows SmartScreen ou antivírus de terceiros podem exibir um falso-positivo. Clique em "Mais informações" > "Executar mesmo assim".

## O Ciclo de Vida da Primeira Execução
Ao abrir, o sistema executa o **Efeito Cascata** no background para garantir um ambiente seguro:
1. **Autenticação SaaS:** O `DTLicenseManager` valida a sua chave de acesso na nuvem (ou inicia o período Trial de 3 dias).
2. **Auditoria:** Mapeia a máquina (`ComputerInfo`, WMI e SID do usuário ativo).
3. **Preparação:** Injeta o plano de energia máximo (`powercfg -duplicatescheme`) para acelerar as manutenções.
4. **Renderização:** A classe `DTGui` entra em ação, construindo a interface e acionando a leitura de hardware.

## 🩺 O Dashboard: Monitor Multiparamétrico do PC

O carro-chefe do DT Toolkit é o seu Dashboard em tempo real. Assim como um médico conecta um paciente a um monitor para o primeiro diagnóstico, o nosso sistema lê o núcleo do Windows e fornece um raio-X instantâneo através de duas tecnologias visuais:

### 1. Gráficos de Desempenho em Tempo Real (O Eletrocardiograma)
Através do motor de renderização gráfica nativo do Windows, o painel desenha o histórico de estresse da máquina segundo a segundo. Você consegue visualizar fisicamente os picos de uso da **CPU** e o consumo da **RAM** em linhas dinâmicas, identificando gargalos e processos pesados no exato momento em que eles acontecem, sem precisar abrir o Gerenciador de Tarefas.

### 2. Lógica Semafórica de Saúde
Aliado aos gráficos, o sistema traduz os números brutos em um indicativo de cores inteligente, avaliando a saúde geral da máquina:

* 🟢 **Verde (Saudável):** Os recursos operam dentro da margem de segurança e o sistema está estável.
* 🟡 **Amarelo (Atenção):** O uso de hardware ou armazenamento está elevado, indicando acúmulo de lixo eletrônico ou gargalos de performance.
* 🔴 **Vermelho (Crítico):** O sistema está no limite extremo (ex: Disco C: lotado, CPU a 100% ou falha de rede). Exige intervenção técnica imediata.

Toda essa leitura visual é feita através de "Túneis Expressos" (Via Rápida) em milissegundos, rodando de forma totalmente assíncrona. O técnico sabe exatamente por onde começar o reparo antes mesmo de dar o primeiro clique, com fluidez total na interface.