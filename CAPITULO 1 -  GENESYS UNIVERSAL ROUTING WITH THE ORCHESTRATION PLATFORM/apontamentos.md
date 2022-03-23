# 1.1 Learning Objectives

After completing this chapter, you should be able to do the following: 

- List the components of Genesys Universal Routing with Orchestration Server

- Describe the function of each component in an Inbound Voice Routing Solution with Orchestration Server

- Define State Chart XML (SCXML) and its use in the Inbound Voice Routing Solution

Depois de concluir este capítulo, você deve ser capaz de fazer o seguinte:

- Listar os componentes do Genesys Universal Routing with Orchestration Server

- Descrever a função de cada componente em uma solução de roteamento de voz de entrada com o Orchestration Server

- Definir o State Chart XML (SCXML) e seu uso na solução de roteamento de voz de entrada

## 1.2 Genesys Universal Routing

![image](https://user-images.githubusercontent.com/52088444/159705854-ec1df12b-f180-4e25-905b-0062b756c18b.png)

In the simplest terms, routing is the process of sending an interaction to a target. For example, sending an incoming telephone call or an incoming email to an agent.

Em termos mais simples, roteamento é o processo de enviar uma interação para um destino. Por exemplo, enviar uma chamada telefônica ou um e-mail para um agente.

In practice, many steps must be taken between the arrival of an interaction and the selection of a target. Not all interactions should go to the same target.
Choices must be made in order to determine the best target for each interaction. 

Each choice-point is an opportunity to make a decision based on the current situation—with the goal of getting the interaction delivered to the right target.

Na prática, muitos passos devem ser dados entre a chegada de uma interação e a seleção de um alvo. Nem todas as interações devem ir para o mesmo destino. Escolhas
devem ser feitas para determinar o melhor alvo para cada interação.

Cada ponto de escolha é uma oportunidade de tomar uma decisão com base na situação atual – com o objetivo de entregar a interação ao alvo certo.

At a high level, Genesys Universal Routing incorporates three key areas for routing decisions such as customer, interaction, and resources. With customer 
information, interaction types, and various kinds of resource availability, businesses can develop a variety of routing strategies to meet their needs and goals.

Em alto nível, o Genesys Universal Routing incorpora três áreas principais para decisões de roteamento, como cliente, interação e recursos. Com informações do cliente,
tipos de interação e vários tipos de disponibilidade de recursos, as empresas podem desenvolver uma variedade de estratégias de roteamento para atender às suas 
necessidades e objetivos.

## 1.3 CIM Platform and Universal Routing(Plataforma CIM e Roteamento Universal)

Universal Routing is part of the Customer Interaction Management (CIM) Platform

- All types of customer interactions are universally routed
- Integrates with existing call center - enterprise, network, VoIP, TDM, or hybrid
- Single point of configuration and management using Web-based Genesys Administrator
- Comprehensive and customizable reporting: Real-time and Historical
Universal Routing is part of the Customer Interaction Management (CIM) Platform

- All types of customer interactions are universally routed
- Integrates with existing call center - enterprise, network, VoIP, TDM, or hybrid
- Single point of configuration and management using Web-based Genesys Administrator
- Comprehensive and customizable reporting: Real-time and Historical

O Roteamento Universal faz parte da Plataforma de Gerenciamento de Interação com o Cliente (CIM)

- Todos os tipos de interações com clientes são roteados universalmente
- Integra-se ao call center existente - corporativo, de rede, VoIP, TDM ou híbrido
- Ponto único de configuração e gerenciamento usando o Genesys Administrator baseado na Web
- Relatórios abrangentes e personalizáveis: em tempo real e históricos

![image](https://user-images.githubusercontent.com/52088444/159707425-f912671d-81ea-468a-bbe4-6dc8ed6fb4e4.png)

The CIM Platform is the core of the Genesys solution suite―a powerful and proven environment for designing, deploying,
and managing all customer interactions and work item processes within the contact center as well as across the entire enterprise.

A plataforma CIM é o núcleo do conjunto de soluções Genesys – um ambiente poderoso e comprovado para projetar, implantar e
gerenciar todas as interações com clientes e processos de itens de trabalho dentro do contact center, bem como em toda a empresa.


Genesys CIM supports all traditional interaction channels such as voice, email, and Web―and emerging channels such as video, SMS, 
chat, and mobile―and activities such as work items in a consistent manner according to company-defined interaction processes and strategies. 
It supports all-channel interactions with automatic capture, process, routing, and reporting based on a company’s specific business criteria,
providing a universal view of the management of every customer interaction.

O Genesys CIM oferece suporte a todos os canais de interação tradicionais, como voz, e-mail e Web – e canais emergentes, como vídeo, SMS, bate-papo
e dispositivos móveis – e atividades como itens de trabalho de maneira consistente, de acordo com os processos e estratégias de interação 
definidos pela empresa. Ele suporta interações em todos os canais com captura, processo, roteamento e relatórios automáticos com base nos critérios
de negócios específicos de uma empresa, fornecendo uma visão universal do gerenciamento de cada interação com o cliente.

The CIM platform centralizes the creation, provisioning, administration, and management of the interaction process reports all interactions and activities 
at both the network and premise levels, and integrates with the broadest range of contact center infrastructure. It also routes interactions across single 
or multiple sites to the most qualified resource available.

A plataforma CIM centraliza a criação, provisionamento, administração e gerenciamento do processo de interação, relata todas as interações e atividades nos 
níveis de rede e local, e se integra com a mais ampla gama de infraestrutura de contact center. Ele também roteia interações em um ou vários sites para o
recurso mais qualificado disponível.




