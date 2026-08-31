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


## 🧪 Testes Realizados
- [x] PING  8.8.8.8 simulando internet em algum qualquer dispositivo.
- ![image url](https://github.com/Dudasantluiz/Redes-Redund-ncia/blob/main/captura01.png?raw=true) 
- [x] após ping com sucesso desligo switch CORE1 simulando uma falha.
- ![image url](https://github.com/Dudasantluiz/Redes-Redund-ncia/blob/main/captura02.png?raw=true) 
- [x] em seguida imagem mostra o Core 2 assumindo automaticamente o tráfego da rede.
- ![image url](https://github.com/Dudasantluiz/Redes-Redund-ncia/blob/main/captura03.png?raw=true)
-  Comando tracert mostrando a nova Rota pelo switch Core 2 com o ip 172.16.10.3.
-  ![image url]()

-  Comando Tracert mostrando a volta da rota priority no Core 1 de ip 172.16.10.2.
-  ![image url](https://github.com/Dudasantluiz/Redes-Redund-ncia/blob/main/captura04.png?raw=true)

-  ## 🚀 Como Executar o Projeto
1. Baixe o arquivo `.pkt` localizado na pasta `src/` [neste link](src/rede_corporativa.pkt).
2. Abra o arquivo no **Cisco Packet Tracer**.
3. Para testar a conectividade:
   - Abra o terminal do `PC-TI-01` e execute: `ping 192.168.20.10`
   - Realize um `tracert` para validar a redundância do protocolo HSRP.
