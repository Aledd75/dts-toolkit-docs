# Solução de Problemas

### O programa fecha sozinho ao abrir
O sistema possui uma proteção de instância única (Mutex). Verifique se ele já não está rodando minimizado ou se há um processo `DTS-Toolkit` no Gerenciador de Tarefas.

### Erro "Requer Administrador"
O script contém uma classe `EnsureAdmin` que tenta elevar privilégios automaticamente. Se falhar, clique com o botão direito no executável e escolha "Executar como Administrador".

### O "Deep Uninstaller" não removeu tudo
Alguns programas protegem seus arquivos enquanto estão rodando.
* **Solução:** O script tenta matar os processos automaticamente, mas reinicie o PC e tente novamente se persistir.

### Logs de Erro
Todas as operações geram logs detalhados.
* Localização: `Desktop\DTS_Logs\`
* Formato: `Relatorio_DTS_YYYY-MM-DD.txt`