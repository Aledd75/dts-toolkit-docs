# Sistema & Reparo

Painel dedicado à saúde, integridade e performance do Windows.

## Rotina de Manutenção Automática
Executa uma sequência lógica de correções com logs em tempo real:
1.  **Stop Services:** Para Windows Update e BITS.
2.  **Limpeza:** Esvazia pastas `SoftwareDistribution`, `Temp`, `Prefetch` e Lixeira.
3.  **Diagnóstico:** Executa `CHKDSK /Scan` (Online), `DISM /RestoreHealth` e `SFC /Scannow`.
4.  **Conclusão:** Se houver reparos críticos em arquivos de sistema, sugere reinicialização.

## Central de Otimização
Interface dedicada para ativar/desativar tweaks de sistema (com botão de desfazer para cada item):

* **Energia:** Ativa plano "Desempenho Máximo" (Ultimate Performance) e ajusta Wi-Fi para performance.
* **GPU & Gráficos:** Ativa HAGS (Hardware Accelerated GPU Scheduling), Otimização de Janela e remove transparências.
* **Gaming:** Desativa DVR/GameBar e ativa "Game Mode".
* **Rede:** Aplica `TCPNoDelay` e remove `NetworkThrottlingIndex`.
* **Privacidade:** Desativa serviço de Geolocalização (`lfsvc`) e Telemetria.
* **Interface:** Restaura Menu de Contexto Clássico (Win11), remove Widgets e pesquisa da barra de tarefas.

## Ferramentas de Disco e Boot
* **Otimizar SSD/HD:** Identifica o tipo de mídia. Executa `TRIM` em SSDs/NVMe e Desfragmentação em HDDs.
* **Reparo de Boot:**
    * **BCDBOOT:** Recria os arquivos de inicialização na partição EFI/Sistema.
    * **WinRE:** Tenta reativar o ambiente de recuperação.