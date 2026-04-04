# Solução de Problemas

Se você encontrou algum comportamento inesperado ao usar o **Dadalt Tech Toolkit**, verifique as soluções catalogadas abaixo:

### A Janela ou Botões estão travados ("Aguarde...")
* O sistema conta com uma proteção chamada `$IsBusy`. Isso significa que um processo pesado (como o SFC Scan) está rodando no **Runspace** assíncrono. Você pode abrir a aba de Logs no canto inferior direito para assistir ao trabalho sendo feito. Quando terminar, os botões serão destravados automaticamente.

### A Internet caiu no meio de um download
* **Auto-Recuperação:** Nossa arquitetura possui tratamento de exceções rigoroso (`try/catch`). Se a conexão cair enquanto o Toolkit baixa um aplicativo ou o Windows Media Creation Tool, o sistema **não irá travar**. O processo atual será abortado com segurança e um alerta em vermelho será gerado no painel de Logs informando a falha de conexão, permitindo que você retome o trabalho assim que a rede voltar.

### Desinstalação de Jogos falhou (Erro no Deep Uninstaller)
* **Proteção Ativa:** O módulo `DTDeepUninstaller` ignora intencionalmente comandos para desinstalar os aplicativos Steam, Epic Games, Battle.net e Riot Games. Isso previne que a desinstalação forense apague acidentalmente centenas de Gigabytes de bibliotecas de jogos. Desinstale-os manualmente, se necessário.

### Geração da Ordem de Serviço em Branco
* O botão **Ordem de Serviço** conta com inteligência para não desperdiçar recursos. Se você abriu o programa e não rodou nenhuma ferramenta de reparo, o sistema apresentará um aviso dizendo que não há logs de manutenção, bloqueando a geração do PDF. Faça um reparo (ex: Limpar Arquivos Temporários) e tente novamente.

### Falso Positivo com Anti-Vírus
* Módulos como o `DTDeepCleaner` e o `DTOptimizeSystem` alteram chaves de registro em *CurrentControlSet* ou usam comandos avançados como *takeown* (Apropriação de Pastas Root). Recomendamos executar a varredura do Windows Defender pelo próprio Toolkit ou pausar antivírus de terceiros, pois as heurísticas podem barrar operações legítimas de manutenção.