# Solução de Problemas

### Licenciamento e Ativação
* **Licença Expirada:** O período trial é de 3 dias. Após isso, é necessário inserir a chave anual (`DADALT-PRO-2026`).
* **Erro de Relógio:** Se o sistema detectar que a data do computador é anterior à data de instalação do toolkit, ele bloqueará o acesso por segurança (Anti-Tamper). Ajuste a data do Windows.

### O programa fecha sozinho ou não abre
* **Instância Única:** Verifique se já existe um processo `DTS-Toolkit` no Gerenciador de Tarefas. O sistema usa um Mutex (`Global\DTS_Toolkit_Unique_ID`) para impedir múltiplas janelas.
* **Permissão:** Certifique-se de executar como Administrador.

### Desinstalação de Jogos falhou
* **Proteção Ativa:** O **Deep Uninstaller** ignora intencionalmente pastas e processos relacionados a Steam, Epic Games, Battle.net, Riot, etc., para evitar que você apague acidentalmente centenas de GBs de jogos. Desinstale esses itens manualmente pelos seus respectivos Launchers.

### Erros de Rede em Empresas
* **Domínio Detectado:** Se você estiver em um PC corporativo, a troca de DNS será bloqueada pelo script para evitar perda de conexão com o servidor de domínio. Isso é um comportamento esperado.

### Logs de Erro
Todas as operações geram logs detalhados, salvos automaticamente.
* O visualizador de logs integrado possui um botão "Abrir Logs" no canto superior direito.
* Logs do Robocopy (Backup) são salvos na pasta de destino do backup.