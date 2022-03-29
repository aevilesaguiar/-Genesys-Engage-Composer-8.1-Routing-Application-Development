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



## 1.4 Routing Application

Routing Application is a set of instructions and decisions that indicate how and where to direct customer interactions.

Aplicativo de roteamento é um conjunto de instruções e decisões que indicam como e para onde direcionar as interações com o cliente.

![image](https://user-images.githubusercontent.com/52088444/160660780-cc543638-03f0-4487-979f-4f711f984cff.png)

A routing application is a set of decisions and instructions that tell Genesys Routing how to handle and where to direct interactions under different circumstances.

Think of a routing application as a structured set of choice-points, each of which analyzes some aspect of the current interaction. The data that a routing application uses to analyze an interaction includes facts related to the interaction itself, the customer initiating the interaction, the state of the contact center, and the particular point in time.

At any given choice-point, only one of several possible outcomes can be optimal. Routing determines which outcome is optimal and sends the interaction along a specified route accordingly.

Um aplicativo de roteamento é um conjunto de decisões e instruções que informam ao Genesys Routing como lidar e para onde direcionar as interações em diferentes circunstâncias.

Pense em um aplicativo de roteamento como um conjunto estruturado de pontos de escolha, cada um dos quais analisa algum aspecto da interação atual. Os dados que um aplicativo de roteamento usa para analisar uma interação incluem fatos relacionados à própria interação, o cliente que iniciou a interação, o estado do contact center e o momento específico.

Em qualquer ponto de escolha, apenas um dos vários resultados possíveis pode ser ótimo. O roteamento determina qual resultado é ideal e envia a interação ao longo de uma rota especificada de acordo.

## 1.5 Routing Targets

Resources to which you can route.

Examples of target types:

- ACD Queue
- Agent
- Agent Group 
- Place
- Place Group
- Routing Point  
![image](https://user-images.githubusercontent.com/52088444/160661196-3076d9ad-3d10-40ea-ad4d-91452782473a.png)

Provisioned in Configuration Layer

![image](https://user-images.githubusercontent.com/52088444/160661242-b9848de6-9f90-4c4e-a21b-7adf60781c2a.png)


A routing target is the resource to which a routing application routes an interaction. Some examples are the CustomerService agent group, Technical_Support agent group, and queue 6602. Most routing applications have more than one target. 

Categories of target types include ACD Queues, Agents, Agent Groups, Places, Place Groups, and Route Points. You may see these target types identified by abbreviations within Genesys.

Question: What kind of targets are used in your company’s environment?

Um destino de roteamento é o recurso para o qual um aplicativo de roteamento roteia uma interação. Alguns exemplos são o grupo de agentes CustomerService, o grupo de agentes Technical_Support e a fila 6602. A maioria dos aplicativos de roteamento tem mais de um destino.

As categorias de tipos de destino incluem Filas ACD, Agentes, Grupos de Agentes, Locais, Grupos de Locais e Pontos de Rota. Você pode ver esses tipos de destino identificados por abreviações no Genesys.

Pergunta: Que tipo de metas são usadas no ambiente da sua empresa?


## Configuration Objects and Routing

You can create configuration objects in Genesys Administrator and then use them in routing. For example, you might enter routing points, queues, places, agents, skills, agent groups, and place groups depending on what targets that contact center needs.

Once you enter this information, Configuration Server works with other Genesys servers to provide the contact center objects and stores them in the configuration database.

Você pode criar objetos de configuração no Genesys Administrator e usá-los no roteamento. Por exemplo, você pode inserir pontos de roteamento, filas, locais, agentes, habilidades, grupos de agentes e grupos de locais, dependendo de quais alvos o contact center precisa.

Depois de inserir essas informações, o Configuration Server trabalha com outros servidores Genesys para fornecer os objetos do contact center e armazená-los no banco de dados de configuração.


## 1.6 Exercise: Identify Routing Resources

The objective of this exercise is to become familiar with routing resources.

Actions

- Log in to Genesys Administrator
- Determine possible routing targets

O objetivo deste exercício é familiarizar-se com os recursos de roteamento.

Ações

- Faça login no Administrador Genesys
- Determinar possíveis destinos de roteamento

![image](https://user-images.githubusercontent.com/52088444/160663179-3240ce08-9e51-4e79-97ed-4363740fa2bc.png)



Log in to Genesys Administrator

1 - Open the Chrome Web browser and click Genesys Administrator (GA) on the bookmarks bar. 

2 - Enter Username: JAdmin and Password: sa

3 - Enter the following in the text field (More):

      - Application: default
      - Host Name: roswell
      - Port: 2020
4 - Click Log in.


Faça login no Administrador Genesys

1 - Abra o navegador da Web Chrome e clique em Genesys Administrator (GA) na barra de favoritos.

2 - Digite Usuário: JAdmin e Senha: sa

3 - Digite o seguinte no campo de texto (Mais):

      - Aplicação: padrão
      - Nome do anfitrião: roswell
      - Porto: 2020
4 - Clique em Entrar.

![image](https://user-images.githubusercontent.com/52088444/160663295-8cc9e1ea-00ae-42fe-9e21-c6ce1a08194d.png)

Determine Possible Routing Targets

1 - Go to PROVISIONING > Switching > Switches. 

2 - Double click on ChicagoSwitch.

3 - Click on the DNs tab. What are some routing points and queues in the ChicagoSwitch?


Note: Drill into the Routing Points folder to locate the routing points in Chicago Switch. 

4 - Go to PROVISIONING > Accounts > Agent Groups. What are some possible agent group targets?

5 - What agents are in Chicago_Sales?

Please refer to the Appendix A: Sample Environment for answers.

Determinar possíveis destinos de roteamento

1 - Vá em PROVISIONING > Switching > Switches.

2 - Clique duas vezes em ChicagoSwitch.

3 - Clique na aba DNs. Quais são alguns pontos de roteamento e filas no ChicagoSwitch?


Observação: acesse a pasta Pontos de roteamento para localizar os pontos de roteamento no Chicago Switch.

4 - Vá em PROVISIONING > Accounts > Agent Groups. Quais são alguns possíveis alvos do grupo de agentes?

5 - Quais são os agentes em Chicago_Sales?

Consulte o Apêndice A: Ambiente de Amostra para obter respostas.

## 1.7 Genesys Routing: Orchestration Platform

- Session-based platform
- Takes Genesys’ core capability of routing and extends it, generalizes it, and integrates it more tightly with other Genesys products

    - Examples include: Mobile Engagement, Proactive Engagement, Conversation Manager, Business Rules, and others.

- Uses open-standard development language: SCXML
- Application Development Tool: Composer
- Runtime: Universal Routing Server + Orchestration Server = Orchestration Platform

- Plataforma baseada em sessão
- Pega a capacidade central de roteamento da Genesys e a estende, generaliza e integra mais firmemente com outros produtos da Genesys

    - Os exemplos incluem: Mobile Engagement, Proactive Engagement, Conversation Manager, Business Rules e outros.

- Usa linguagem de desenvolvimento de padrão aberto: SCXML
- Ferramenta de Desenvolvimento de Aplicativos: Composer
- Tempo de execução: Universal Routing Server + Orchestration Server = Orchestration Platform

![image](https://user-images.githubusercontent.com/52088444/160663880-128755c7-4d3c-4287-a115-3c988bad6847.png)

Genesys Orchestration Platform (Universal Routing Server + Orchestration Server) takes Genesys’ core capability of routing and extends it, generalizes it, and integrates it more tightly with other Genesys products (e.g., Mobile Engagement, Proactive Engagement, and others). 

A Genesys Orchestration Platform (Universal Routing Server + Orchestration Server) pega a capacidade central de roteamento da Genesys e a estende, generaliza e a integra mais firmemente a outros produtos da Genesys (por exemplo, Mobile Engagement, Proactive Engagement e outros).

For example, a bank customer calls an 800 number inquiring about mortgage preapproval. An IVR prompts the customer for an account number and then transfers the call to an agent, who fills in an application form and asks the customer to email some supporting documents. After the customer emails the documents, the customer receives an automated push notification message via a mobile banking application on a smartphone. The message indicates the customer will receive a response within 48 hours. The next day the customer receives a congratulatory email on the approval of the mortgage application.

This example involves voice, IVR, email, and mobile channels. The Orchestration Platform is able to treat the entire transaction as a single service.

Orchestration is a session-based driven platform that deals with interactions as long as they are involved with the session. The session can be the life of the interaction not just delivery to the agent. This allows ORS to continue to work with the interaction, even after the agent has answered.

Por exemplo, um cliente de banco liga para um número 800 perguntando sobre a pré-aprovação de hipoteca. Um IVR solicita ao cliente um número de conta e, em seguida, transfere a chamada para um agente, que preenche um formulário de inscrição e solicita que o cliente envie alguns documentos de suporte por e-mail. Depois que o cliente envia os documentos por e-mail, o cliente recebe uma mensagem automática de notificação por push por meio de um aplicativo de banco móvel em um smartphone. A mensagem indica que o cliente receberá uma resposta dentro de 48 horas. No dia seguinte, o cliente recebe um e-mail de felicitações pela aprovação do pedido de hipoteca.

Este exemplo envolve voz, IVR, e-mail e canais móveis. A Plataforma de Orquestração é capaz de tratar toda a transação como um único serviço.

A orquestração é uma plataforma baseada em sessão que lida com interações desde que estejam envolvidas com a sessão. A sessão pode ser a vida da interação e não apenas a entrega ao agente. Isso permite que o ORS continue trabalhando com a interação, mesmo após o agente ter respondido.

Other examples of how this could be used:

- Adding key-value pairs to the call via the ORS application, not through the agent desktop, as the call is in progress
- Conducting post-call activities on the interaction, such as triggering a survey
- Having the same session control the interaction if the agent does not answer or reject the call

Outros exemplos de como isso pode ser usado:

- Adicionar pares de valores-chave à chamada por meio do aplicativo ORS, não por meio da área de trabalho do agente, pois a chamada está em andamento
- Realização de atividades pós-chamada sobre a interação, como acionar uma pesquisa
- Ter a mesma sessão controlando a interação caso o agente não atenda ou rejeite a chamada

Orchestration Server offers an open standard-based platform with a SCXML engine. SCXML is a language that defines steps (states) and the conditions for transitions between states. SCXML fits perfectly with the idea of routing as a series of steps with feedback to determine transitions between steps.

You can use Genesys Composer to build SCXML-based applications that Orchestration Server will execute. The focus of the course is on developing applications using Composer. 

O Orchestration Server oferece uma plataforma aberta baseada em padrão com um mecanismo SCXML. SCXML é uma linguagem que define etapas (estados) e as condições para transições entre estados. O SCXML se encaixa perfeitamente na ideia de roteamento como uma série de etapas com feedback para determinar as transições entre as etapas.

Você pode usar o Genesys Composer para criar aplicativos baseados em SCXML que o Orchestration Server executará. O foco do curso é o desenvolvimento de aplicativos usando o Composer.

## 1.8 Orchestration Platform Architecture

![image](https://user-images.githubusercontent.com/52088444/160664615-e9d88aa5-9b9d-4f44-b97c-e71787c3dd1b.png)

The Orchestration Platform (Universal Routing Server (URS) and Orchestration Server (ORS)) communicates with Configuration Server to read into memory information about contact center objects such as routing points, agents, agent groups, and skills. Configuration Server also provides application setup information such as the starting SCXML page, to the Orchestration Platform. 

A Plataforma de Orquestração (Universal Routing Server (URS) e o Orchestration Server (ORS)) se comunicam com o Configuration Server para ler na memória informações sobre objetos do contact center, como pontos de roteamento, agentes, grupos de agentes e habilidades. O Configuration Server também fornece informações de configuração do aplicativo, como a página inicial do SCXML, para a Orchestration Platform.

![image](https://user-images.githubusercontent.com/52088444/160664761-3afe3161-4734-4de2-bdb9-ffc85dea0a5f.png)


T-Server has many roles in the Orchestration Platform:

- Interfacing with communications equipment (such as switches and ACDs)

- Creating and maintaining the call object—a detailed record of each interaction from its beginning to its end

- Distributing relevant messages from the switch to other Framework components
- Attaching and maintaining attached data for the interaction
- Letting Universal Routing Server (URS) and Orchestration Server (ORS) know a call has arrived and a routing application needs to be executed

O T-Server tem muitas funções na Orchestration Platform:

- Interface com equipamentos de comunicação (como switches e ACDs)

- Criação e manutenção do objeto de chamada - um registro detalhado de cada interação do início ao fim

- Distribuir mensagens relevantes do switch para outros componentes do Framework
- Anexar e manter dados anexados para a interação
- Informar o Universal Routing Server (URS) e o Orchestration Server (ORS) que uma chamada chegou e um aplicativo de roteamento precisa ser executado

T-Server monitors certain DNs in the switch and receives messages regarding these DNs through the CTI link. T-Server then communicates these messages to its clients. For example, when a telephone call arrives at a routing point, DN is configured to request a routing destination, T-Server is alerted and then it notifies URS and ORS with an EventRouteRequest message. 

SIP Server has the same position in the Genesys Media Layer as all Genesys T-Servers. SIP Server is an application server that integrates Genesys telephony-based applications to various SIP-based products. SIP Server operates both as a T-Server (telephony server) and as a call-switching component in which the call-switching element functions as SIP (Session Initiation Protocol). 

O T-Server monitora certos DNs no switch e recebe mensagens sobre esses DNs através do link CTI. O T-Server então comunica essas mensagens aos seus clientes. Por exemplo, quando uma chamada telefônica chega a um ponto de roteamento, o DN é configurado para solicitar um destino de roteamento, o T-Server é alertado e notifica o URS e o ORS com uma mensagem EventRouteRequest.

O SIP Server tem a mesma posição na Genesys Media Layer que todos os Genesys T-Servers. O SIP Server é um servidor de aplicativos que integra aplicativos baseados em telefonia da Genesys a vários produtos baseados em SIP. O Servidor SIP opera tanto como um T-Server (servidor de telefonia) quanto como um componente de comutação de chamadas no qual o elemento de comutação de chamadas funciona como SIP (Protocolo de Iniciação de Sessão).

![image](https://user-images.githubusercontent.com/52088444/160665173-8c8160e9-c925-456a-8c79-5a1adf0e2784.png)

Stat Server tracks the real-time status of the contact center objects. For example, Stat Server knows the Place at which each Agent is logged in, along with the status of each agent (Ready or Not Ready). Stat Server also collects performance statistics. For example, Stat Server knows the length of time each agent has been in the Ready state.

The Orchestration Platform, specifically URS, can use statuses and statistics to find targets and make more intelligent real-time routing decisions.

O Stat Server rastreia o status em tempo real dos objetos do contact center. Por exemplo, o Stat Server sabe o Local em que cada Agente está conectado, juntamente com o status de cada agente (Pronto ou Não Pronto). O Stat Server também coleta estatísticas de desempenho. Por exemplo, o Stat Server sabe por quanto tempo cada agente esteve no estado Pronto.

A Orchestration Platform, especificamente o URS, pode usar status e estatísticas para encontrar destinos e tomar decisões de roteamento mais inteligentes em tempo real.

![image](https://user-images.githubusercontent.com/52088444/160665330-df2bbd88-229c-489f-8fe0-695962eeb824.png)

Orchestration Server executes SCXML applications. A developer can use Composer to develop the SCXML applications. Composer provides drag-and-drop graphical development of voice applications (or callflows) and routing applications (or workflows) as well as syntax-directed editing of these applications. 

Composer is an Eclipse-based application. Eclipse (www.eclipse.org) is an integrated development environment (IDE) comprising of a base workspace and an extensible plug-in system for customizing the environment. Composer can run on the following operating systems: Windows 2003 and 2008, Windows XP, Windows Vista, Windows 7, and MacOS (partial support). 

O Orchestration Server executa aplicativos SCXML. Um desenvolvedor pode usar o Composer para desenvolver os aplicativos SCXML. O Composer fornece desenvolvimento gráfico de arrastar e soltar de aplicativos de voz (ou fluxos de chamadas) e aplicativos de roteamento (ou fluxos de trabalho), bem como edição direcionada por sintaxe desses aplicativos.

O Composer é um aplicativo baseado em Eclipse. Eclipse (www.eclipse.org) é um ambiente de desenvolvimento integrado (IDE) composto por uma área de trabalho base e um sistema de plug-in extensível para personalizar o ambiente. O Composer pode ser executado nos seguintes sistemas operacionais: Windows 2003 e 2008, Windows XP, Windows Vista, Windows 7 e MacOS (suporte parcial).

We will discuss routing applications during this course. Voice applications are for Genesys Voice Platform (GVP)—a software suite that unifies voice and Web technologies to provide a complete solution for customer self-service or assisted service. If you would like to learn more about GVP, please visit Genesys documentation at http://docs.genesys.com/Documentation/GVP.

Discutiremos os aplicativos de roteamento durante este curso. Os aplicativos de voz destinam-se à Genesys Voice Platform (GVP)—um conjunto de software que unifica as tecnologias de voz e da Web para fornecer uma solução completa de autoatendimento ou serviço assistido ao cliente. Se você quiser saber mais sobre o GVP, visite a documentação da Genesys em http://docs.genesys.com/Documentation/GVP.

State Chart XML

General-purpose event-based state machine language.

A state machine can have:


- A series of States

- Transitions that go between states

    - Transitions are triggered by Events

- Actions that “do” something

XML do gráfico de estado

Linguagem de máquina de estado baseada em eventos de uso geral.

Uma máquina de estado pode ter:


- Uma série de Estados

- Transições que vão entre os estados

    - As transições são acionadas por eventos

- Ações que “fazem” algo

