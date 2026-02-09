## Etapa 2 – Configuração da Dashboard do pfSense
**Data:** 08/02/2026

### 2.1 Ajustes Gerais do Sistema
Após a instalação, foram realizadas configurações iniciais diretamente na dashboard do pfSense com o objetivo de padronizar o ambiente, melhorar a usabilidade e facilitar o monitoramento.

As seguintes configurações foram aplicadas:
- Definição de **Hostname** do firewall
- Definição de **Domain** interno
- Ajuste de **Timezone** conforme a localidade do ambiente
- Alteração do **tema da interface para Dark Mode**, visando melhor ergonomia e redução de fadiga visual
- Definição do layout da dashboard para **3 colunas**
- Configuração de **Interfaces Sort**
- Ativação de **Associated Panels Show**
- Ativação da exibição de **Hostname no topo da interface de login**

Essas configurações facilitam a identificação do firewall, organização das informações e administração do ambiente.

### 2.2 Instalação e Configuração de Widgets da Dashboard
Foram instalados e configurados os seguintes widgets nativos do pfSense para monitoramento e visibilidade operacional:

- **Disks** – Monitoramento de uso de armazenamento
- **Interfaces** – Status das interfaces de rede
- **Gateways** – Monitoramento de gateways e links
- **Interface Statistics** – Estatísticas detalhadas de tráfego por interface
- **Traffic Graphs** – Visualização gráfica de tráfego em tempo real
- **Service Status** – Status dos serviços ativos no firewall
- **NTP Status** – Verificação de sincronização de horário
- **IPsec** – Monitoramento de túneis IPsec
- **OpenVPN** – Monitoramento de conexões VPN
- **Firewall Logs** – Visualização imediata de logs de bloqueio e permissões

A escolha desses widgets permite uma visão centralizada do estado do firewall e acelera a detecção de falhas, anomalias e eventos de segurança.

### 2.3 Considerações Operacionais e de Segurança
- A dashboard foi configurada com foco em **monitoramento contínuo** e resposta rápida a incidentes.
- A centralização de logs e status reduz o tempo de diagnóstico em cenários de falha.
- A configuração visual não impacta a segurança diretamente, mas melhora a eficiência operacional do analista.