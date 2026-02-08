## Etapa 1 – Instalação e Configuração Inicial das Máquinas Virtuais
**Data:** 08/02/2026

### 1.1 Máquina Virtual pfSense
Configuração da máquina virtual destinada ao firewall pfSense:

- **Memória RAM:** 4096 MB
- **Processadores:** 2 CPUs
- **Memória de Vídeo:** 128 MB
- **Controladora Gráfica:** VMSVGA
- **Armazenamento:** 16 GB
- **Adaptadores de Rede:**
  - Adaptador 1: NAT (Interface WAN)
  - Adaptador 2: Rede Interna (Interface LAN)
- **Modo Promíscuo:** Allow All

Essa configuração permite que o pfSense atue como gateway entre a internet simulada (NAT) e a rede interna protegida.

### 1.2 Máquina Virtual Debian 13
Configuração da máquina virtual utilizada como host interno da rede:

- **Memória RAM:** 2048 MB
- **Processadores:** 2 CPUs
- **Memória de Vídeo:** 16 MB
- **Controladora Gráfica:** VMSVGA
- **Armazenamento:** 20 GB
- **Adaptadores de Rede:**
  - Adaptador 1: Rede Interna
- **Modo Promíscuo:** Allow All

O Debian 13 atua como máquina cliente da rede interna, permitindo testes de conectividade, políticas de firewall e futuras implementações de serviços.

### 1.3 Considerações de Segurança
- O uso de **modo promíscuo** é intencional para fins de análise e monitoramento de tráfego.
- O ambiente é estritamente de laboratório, não recomendado para produção.
- A separação WAN/LAN segue boas práticas de segmentação de rede.


