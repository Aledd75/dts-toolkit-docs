# Sistema & Reparo

Este painel foca na saúde e integridade do Windows.

## Rotina de Manutenção
Executa uma sequência automática de correções:
1.  **Limpeza:** Remove cache do Windows Update, Temp e Prefetch.
2.  **SFC / DISM:** Verifica e repara arquivos corrompidos do sistema.
3.  **Checkdisk:** Verifica a integridade do sistema de arquivos.

## Ferramentas de Disco
* **Otimizar SSD/HD:** Executa TRIM (em SSDs) ou Desfragmentação (em HDs).
* **Boost NVMe:** Otimizações específicas para drives NVMe.

## Reparo de Boot (BootRepairManager)
Interface gráfica para corrigir problemas de inicialização:
* **BCDBOOT:** Reinstala arquivos de boot do Windows.
* **MBR Fix:** Atualiza o código mestre de inicialização (NT60).
* **WinRE:** Repara e reativa o Ambiente de Recuperação do Windows.