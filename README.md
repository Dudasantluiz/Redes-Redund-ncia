# Redes-Redund-ncia
O foco principal foi a criação de uma arquitetura resiliente a falhas, onde a queda de um equipamento de borda não interrompe a comunicação dos usuários finais nem os serviços vitais da empresa.

Para disponibilidade, foi implementado o protocolo HSRP atuando no gateway da rede, em conjunto com o Spanning Tree Protocol (STP) para prevenir loops e garantir caminhos redundantes de Camada 2. A segmentação do tráfego interno é tratada via VLANs, e a atribuição de IPs é automatizada por um servidor DHCP e também estática. Para acesso externo, foram configurados o NAT e Rotas Default, enquanto a segurança corporativa é controlada por (ACLs).

🛠️ Tecnologias Aplicadas
HSRP: Redundância de gateway com failover automático em caso de falhas.

Spanning Tree (STP): Prevenção de loops de camada 2 em links redundantes.

VLANs: Segmentação de tráfego entre departamentos.

DHCP: Atribuição dinâmica e centralizada de IPs.

NAT & Rota Default: Tradução de endereços e roteamento de saída para a Internet.

ACLs: Filtragem de pacotes e controle de acesso entre sub-redes.

![image url](https://github.com/Dudasantluiz/Redes-Redund-ncia/blob/main/Captura%20de%20tela%202026-08-30%20194550.png)
