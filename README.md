# 🌐 Fundamentos de Redes de Computadores com NotebookLM

> Projeto desenvolvido como parte de um Desafio de Projeto da DIO, utilizando o NotebookLM como ferramenta de aprendizagem ativa para pesquisa, organização e consolidação de conhecimentos sobre fundamentos de redes de computadores.

---

## 📌 1. Contexto e Objetivos

### Contexto

Este projeto tem como objetivo explorar os fundamentos de redes de computadores utilizando o NotebookLM como ferramenta de apoio ao processo de aprendizagem.

Foram selecionadas fontes abertas e confiáveis sobre redes de computadores, que foram utilizadas como base para consultas, comparação de conceitos, elaboração de perguntas e construção de um miniguia de estudos.

### Objetivos

* Compreender os principais fundamentos de redes de computadores;
* Entender o funcionamento dos modelos OSI e TCP/IP;
* Conhecer os principais protocolos de comunicação;
* Compreender conceitos como endereço IP, máscara de rede, gateway e DNS;
* Diferenciar protocolos e suas respectivas funções;
* Utilizar o NotebookLM para realizar pesquisas baseadas nas fontes selecionadas;
* Experimentar diferentes estratégias de prompting;
* Identificar limitações e dificuldades encontradas durante as consultas;
* Consolidar o conhecimento adquirido em um material de consulta futura.

---

# 📚 2. Curadoria de Fontes

Foram selecionadas fontes abertas relacionadas aos fundamentos de redes de computadores.

A seleção considerou principalmente:

* Autoridade da instituição ou autor;
* Qualidade e profundidade do conteúdo;
* Relevância para os objetivos do projeto;
* Disponibilidade pública;
* Possibilidade de utilizar o material como fonte de consulta no NotebookLM.

### Fonte 01

**Título:**
Computer Networking: Principles, Protocols and Practice

**Autor/Instituição:**
Olivier Bonaventure, UCLouvain

**Tipo:**
PDF 

**Justificativa da seleção:**
É um livro-texto completo de redes e cobre justamente uma grande conteúdo: introdução, modelos de referência, camada de aplicação, transporte, rede, enlace, LANs, TCP, UDP, IP, roteamento, Ethernet e Wi-Fi. A Open Textbook Library o considera adequado para cursos introdutórios de Ciência da Computação/Engenharia.

---

### Fonte 02

**Título:**
RFC 1122 - Requirements for Internet Hosts

**Tipo:**
Documentação HTML

**Link:**
https://www.rfc-editor.org/rfc/rfc1122.html

**Justificativa da seleção:**
Ele especifica requisitos para hosts da Internet e aborda as camadas de comunicação da arquitetura Internet, incluindo link layer, IP layer e transport layer.

---

### Fonte 03

**Título:**
Internet Protocol RFC 791 part of STD 5

**Tipo:**
Documentação HTML

**Link:**
https://www.rfc-editor.org/rfc/rfc791.html

**Justificativa da seleção:**
Detalha e especifica o protocolo de internet (IP)

---

### Fonte 04

**Título:**
Transmission Control Protocol (TCP) RFC 9293 also known as STD 7

**Autor/Instituição:**
[Autor ou instituição]

**Tipo:**
Documentação HTML

**Link:**
https://www.rfc-editor.org/rfc/rfc9293.html

**Justificativa da seleção:**
Detalha e especifica o protocolo transmissão e controle (TCP)

---

## 🤖 3. Utilização do NotebookLM

As fontes selecionadas foram adicionadas a um notebook no NotebookLM.

A ferramenta foi utilizada principalmente para:

* Consultar informações presentes nas fontes;
* Comparar conceitos;
* Solicitar explicações em diferentes níveis de profundidade;
* Identificar relações entre diferentes conceitos;
* Criar perguntas para revisão;
* Consolidar informações encontradas nas fontes;
* Verificar as referências utilizadas nas respostas.
  
---

# 🧪 4. Engenharia de Prompts

Nesta etapa foram realizados diferentes experimentos com prompts, buscando melhorar a qualidade, profundidade e utilidade das respostas.

## Experimento 01: Pergunta inicial

### Prompt

> Explique o modelo TCP/IP.

### Resultado observado

O modelo TCP/IP foi consolidado na RFC 1122 e surgiu a partir de uma arquitetura que já havia sido amplamente implementada e testada, diferentemente do modelo OSI, que possui uma origem mais teórica.

Ele é organizado em quatro camadas:

Aplicação
Fornece serviços diretamente às aplicações. Reúne funções equivalentes às camadas de aplicação, apresentação e sessão do OSI.
Exemplos: HTTP, FTP, SMTP e DNS.
Transporte
Responsável pela comunicação ponta a ponta entre aplicações.
TCP: confiável, orientado à conexão, garante ordem e retransmissão dos dados.
UDP: simples, sem conexão e mais rápido, mas não garante a entrega dos dados.
Internet
Responsável pelo endereçamento e encaminhamento de pacotes entre redes.
IP: entrega de datagramas em modo best-effort, sem garantia de entrega.
ICMP: mensagens de erro e diagnóstico, como no ping.
IGMP: gerenciamento de grupos multicast.
Link/Enlace
Responsável pela comunicação entre o dispositivo e a rede local, envolvendo tecnologias físicas e de enlace.
Exemplo: ARP, que relaciona endereços IP a endereços físicos (MAC).
Princípios importantes
Roteadores stateless: os roteadores não precisam manter informações sobre cada conexão. Cada pacote é tratado independentemente, enquanto a confiabilidade fica principalmente com os dispositivos nas extremidades.
Princípio da Robustez (Postel): "Seja liberal no que você aceita e conservador no que você envia." Sistemas devem enviar dados corretamente formatados e ser tolerantes a pequenas irregularidades nos dados recebidos.

Em uma frase: o TCP/IP divide a comunicação em camadas, deixando a rede responsável pelo transporte dos pacotes e as extremidades responsáveis pela confiabilidade e controle da comunicação.

### Problema identificado

A resposta foi correta, porém sem o apontamento específico que esperávamos e sem exemplo prático

---

## Experimento 02: Prompt aprimorado

### Prompt

> Com base exclusivamente nas fontes disponíveis neste notebook, explique o modelo TCP/IP. Para cada camada, apresente sua função principal, os principais protocolos associados e exemplos práticos de utilização. Sempre que possível, indique a fonte utilizada.

### Resultado observado

O modelo de referência TCP/IP foi estruturado formalmente na RFC 1122 como a arquitetura de comunicação que rege os computadores e sistemas interconectados da Internet
. Diferente do modelo OSI de sete camadas, o modelo TCP/IP foi consolidado a partir de implementações práticas e baseia-se em quatro camadas hierárquicas
.
Abaixo estão descritas as funções principais, os protocolos e as aplicações de cada camada:
1. Camada de Aplicação (Application Layer)
Função Principal: É a camada mais alta do modelo, responsável por prover serviços de comunicação diretamente aos programas de usuário (como clientes e servidores) e executar funções de suporte ao sistema
. Ela simplifica as camadas superiores do modelo OSI ao incluir de maneira implícita as funções de Apresentação (como codificação de caracteres) e de Sessão
.
Principais Protocolos: HTTP (HyperText Transfer Protocol)
, SMTP (Simple Mail Transfer Protocol)
, POP/IMAP
, FTP (File Transfer Protocol)
 e DNS (Domain Name System)
.
Exemplo Prático:
Quando um usuário digita um nome amigável como www.ietf.org no navegador, o cliente DNS realiza uma consulta na rede para mapear esse nome em um endereço IP binário (como 64.170.98.32) para viabilizar a conexão
.
O navegador web (cliente), por sua vez, abre uma conexão para recuperar o documento HTML usando requisições e respostas textuais sob o protocolo HTTP
.
Em sistemas de correio eletrônico, uma mensagem de e-mail é enviada a partir de um Mail User Agent (MUA) usando comandos SMTP para o servidor de e-mail do domínio
.
2. Camada de Transporte (Transport Layer)
Função Principal: Responsável por fornecer serviços de comunicação de ponta a ponta (end-to-end) para as aplicações de nível superior, isolando-as dos detalhes da transmissão de dados pela rede
.
Principais Protocolos:
TCP (Transmission Control Protocol): Um protocolo virtual orientado a conexão e confiável que fornece entrega ordenada, correção de erros (checksum), gerenciamento de fluxo por janelas deslizantes e retransmissões automáticas de pacotes perdidos
.
UDP (User Datagram Protocol): Um protocolo de transporte minimalista, não orientado à conexão e não confiável (melhor esforço), que adiciona apenas controle básico de erros (checksum) e multiplexação de aplicações via portas numéricas
.
Exemplo Prático:
O TCP é amplamente utilizado em transferências de dados massivos e transações que não aceitam perdas, como FTP, login remoto SSH ou transferências de e-mail por SMTP
. O estabelecimento da conexão TCP é feito através de um handshake de três vias (Three-Way Handshake) utilizando segmentos com bits de controle SYN e ACK
.
O UDP é frequentemente aplicado em jogos interativos online, onde a latência ultra baixa é preferível à confiabilidade absoluta e os dados podem sofrer pequenas perdas pontuais de pacotes sem comprometer a aplicação
. Ele também sustenta serviços de arquivos locais rápidos como o NFS (Network File System) rodando sobre RPC
.
3. Camada de Internet (Internet Layer)
Função Principal: É o núcleo da comunicação sem conexão da arquitetura, equivalente à camada de Rede
. Sua função é transportar datagramas de dados de forma independente do host de origem até o host de destino final através de sistemas intermediários chamados roteadores
. Ele gerencia o endereçamento lógico dos dispositivos, o roteamento dos datagramas e a fragmentação quando necessário
.
Principais Protocolos: IP (Internet Protocol - versões IPv4 e IPv6)
, ICMP (Internet Control Message Protocol)
 e IGMP (Internet Group Management Protocol)
.
Exemplo Prático:
Os roteadores na Internet utilizam o endereço IP do pacote recebido para inspecionar suas tabelas de encaminhamento e aplicar o algoritmo de correspondência de prefixo mais longo (Longest Prefix Match) para direcionar o pacote à interface correta de saída
.
Se um datagrama IP de 2000 bytes é transmitido por uma rede Token Ring e precisa trafegar por uma rede Ethernet intermediária com MTU máximo de 1500 bytes, a camada IP do roteador cuida da fragmentação desse datagrama em partes menores para que possam ser reestruturados no destino
.
O utilitário ping envia mensagens de ICMP Echo Request para testar se uma máquina ou roteador está operacional, medindo o tempo de ida e volta (RTT) das respostas ICMP Echo Reply
.
4. Camada de Link ou Enlace (Link Layer)
Função Principal: Situa-se na base da pilha de protocolos e realiza a interface de software diretamente com o hardware de rede conectado física ou logicamente (connected network)
. Ela combina os aspectos lógicos de enlace de dados e os aspectos físicos da infraestrutura de transmissão
.
Principais Protocolos: ARP (Address Resolution Protocol)
, PPP (Point-to-Point Protocol)
, bem como os padrões físicos de controle de acesso ao meio como Ethernet (IEEE 802.3)
 e Wi-Fi (IEEE 802.11)
.
Exemplo Prático:
Antes de transmitir fisicamente um pacote IP em uma rede local, um host precisa converter o IP lógico de destino no endereço físico (endereço MAC de 48 bits) da placa de rede associada
. Para isso, ele envia um quadro ARP em broadcast perguntando qual dispositivo possui aquele IP
. A resposta em unicast retorna o endereço de hardware, permitindo que a camada de link monte o quadro Ethernet e o envie pelo meio físico
.

### Melhoria identificada

A resposta foi mais concreta, especificando o que desejávamos obter e com exemplo prático.

---

## Experimento 03: Comparação de conceitos

### Prompt

> Com base nas fontes disponíveis, compare TCP e UDP. Apresente as principais diferenças em uma tabela considerando conexão, confiabilidade, controle de fluxo, velocidade, overhead e exemplos de utilização. Indique as fontes utilizadas.

### Resultado observado

Abaixo está a comparação detalhada entre os protocolos de transporte TCP (Transmission Control Protocol) e UDP (User Datagram Protocol) baseada exclusivamente nas fontes disponíveis neste notebook.
Tabela Comparativa: TCP vs. UDP
Critério
TCP
UDP
Conexão
Orientado a conexão
. Requer um processo de estabelecimento de conexão de três vias (three-way handshake) antes de enviar dados
.
Sem conexão (connectionless)
. Trata cada datagrama como uma entidade independente e sem circuitos lógicos
.
Confiabilidade
Confiável
. Garante a entrega ordenada e sem erros do fluxo de bytes (byte-stream) através de números de sequência, somas de verificação (checksum) e retransmissões de pacotes perdidos
.
Não confiável
. Não oferece garantias de entrega de ponta a ponta (podendo ocorrer perdas e desordenação de pacotes)
. O checksum apenas garante que segmentos corrompidos não sejam entregues à aplicação (sendo silenciosamente descartados)
.
Controle de Fluxo e Congestionamento
Possui controle de fluxo (baseado em janela deslizante para evitar sobrecarregar o receptor)
 e controle de congestionamento (algoritmos como slow start, congestion avoidance e AIMD) para ajustar a taxa de transmissão ao estado da rede
.
Não possui mecanismos nativos de controle de fluxo ou de congestionamento
. Qualquer controle de entrega ou ordenação necessário deve ser implementado diretamente pela própria aplicação
.
Velocidade / Latência
Mais lento devido ao atraso no estabelecimento de conexão (handshake)
 e à necessidade de esperar por confirmações de recebimento (ACKs) e possíveis retransmissões sob controle de congestionamento
.
Mais rápido (latência minimizada)
. Ideal para transmissões que toleram pequenas perdas, mas exigem tempo de entrega mínimo
.
Overhead
Alto overhead. O cabeçalho padrão possui pelo menos 20 bytes (podendo aumentar caso utilize opções adicionais)
. Além disso, consome recursos do sistema mantendo o estado de cada conexão ativa por meio de um Bloco de Controle de Transmissão (TCB)
.
Baixo overhead. O cabeçalho possui um tamanho fixo de apenas 8 bytes (64 bits contendo portas de origem/destino, comprimento e checksum)
. Não há consumo de recursos para manter conexões ativas na memória
.
Exemplos de Utilização
Aplicações que exigem entrega garantida de dados sem erros: Correio eletrônico (SMTP, POP, IMAP)
; navegação Web (HTTP)
; transferência de arquivos (FTP, compartilhamento P2P)
; e acesso remoto (SSH, Telnet, X11, VNC)
.
Aplicações tolerantes a perdas e altamente sensíveis a atrasos: Consultas de nomes de domínio (DNS)
; chamadas de procedimento remoto (RPC) e sistemas de arquivos rápidos em redes locais (NFS sobre UDP)
; jogos de computador interativos de tempo real
; e transmissões de voz (VoIP) ou vídeo interativo.

---

# 🩹 5. Cicatrizes e Troubleshooting

Durante os experimentos foram identificadas algumas dificuldades na obtenção das respostas desejadas.

### Cicatriz 01: Respostas muito genéricas

**Problema:**
Perguntas muito abertas produziram respostas introdutórias, sem aprofundamento suficiente.

**Solução:**
A pergunta foi reformulada especificando o nível de detalhamento, os conceitos desejados e a necessidade de utilizar exclusivamente as fontes do notebook.

---

### Cicatriz 02: Falta de contexto

**Problema:**
Algumas perguntas não deixavam claro se o objetivo era obter uma explicação introdutória ou técnica.

**Solução:**
Foram adicionadas instruções sobre público-alvo, profundidade e formato esperado da resposta.

---

### Cicatriz 03: Necessidade de verificar as fontes

**Problema:**
Uma resposta gerada pela ferramenta pode parecer correta, mas a origem da informação precisa ser verificada.

**Solução:**
Os prompts passaram a solicitar explicitamente referências às fontes utilizadas, permitindo comparar a resposta com o material original.

---

# 🧠 6. Miniguia de Estudos

## 6.1 O que é uma rede de computadores?

Uma rede de computadores é um sistema de comunicação utilizado para permitir que múltiplos dispositivos autônomos, referidos tecnicamente como hosts, compartilhem recursos e troquem informações diretamente entre si.
Sob o ponto de vista das aplicações de software e dos usuários, uma rede pode ser abstratamente compreendida como um provedor que oferece um conjunto de capacidades de comunicação (serviços), no qual cada dispositivo final é identificado de forma inequívoca por meio de um endereço exclusivo.
As redes de computadores podem ser classificadas e descritas sob diversas perspectivas de acordo com as fontes disponíveis:

1. Classificação por Área Geográfica
   
As redes costumam ser agrupadas com base na distância física e na abrangência territorial que cobrem:
LAN (Local Area Network - Rede Local): Interconecta dispositivos localizados em uma área restrita, que varia tipicamente de alguns metros até poucas dezenas de quilômetros de distância (como em um ambiente doméstico ou de escritório).
MAN (Metropolitan Area Network - Rede Metropolitana): Interliga equipamentos distribuídos em limites urbanos ou metropolitanos, abrangendo distâncias de até algumas centenas de quilômetros.
WAN (Wide Area Network - Rede de Longa Distância): Permite a interconexão de hosts que podem estar localizados em qualquer parte do globo terrestre, dependendo de tecnologias complexas como links satelitais e cabos oceânicos.

2. Topologias Físicas
   
A organização e o desenho geométrico das conexões físicas (que podem ser cabos de par trançado, cabos coaxiais, fibras ópticas ou ondas de rádio) definem a topologia de uma rede:
Malha Completa (Full-Mesh): Apresenta um link físico dedicado e exclusivo entre cada par de hosts na rede. Garante extrema redundância e desempenho, mas exige muitas portas de hardware e tem alto custo de implantação.
Barramento (Bus): Todos os hosts são conectados de forma paralela a um único meio de transmissão compartilhado (cabo principal). Um sinal elétrico emitido por qualquer host propaga-se por toda a extensão do barramento e é recebido por todos os demais dispositivos.
Estrela (Star): Os hosts se conectam de forma individual e exclusiva a um dispositivo central (que pode ser um regenerador físico ou um comutador inteligente). Se um link individual quebrar, apenas aquele host é isolado.
Anel (Ring): Os hosts são conectados em uma estrutura circular fechada unidirecional. O sinal trafega de nó em nó até retornar ao remetente original.
Árvore (Tree): Estrutura hierárquica baseada em ramificações, frequentemente empregada para conectar grupos massivos de usuários com excelente custo-benefício (como redes de TV a cabo.

3. Modos de Transmissão de Dados
   
Para acomodar diferentes necessidades de comunicação, as redes suportam quatro modos principais de transmissão de mensagens:
Unicast: Comunicação ponto a ponto direta, na qual as informações são transmitidas de um único remetente para um único destinatário de maneira individualizada.
Multicast: Entrega eficiente de um mesmo fluxo de dados a um grupo seletivo de múltiplos destinatários simultâneos, de modo que a infraestrutura física de rede cuida de duplicar as mensagens apenas nos pontos em que os caminhos se separam.
Broadcast: Envio simultâneo de uma informação a absolutamente todos os hosts pertencentes àquela rede ou segmento físico, comumente limitado a redes locais (LANs).
Anycast: Transmissão para um grupo de dispositivos receptores que compartilham o mesmo endereço de destino, na qual os mecanismos da interrede garantem que a informação seja entregue apenas a um deles (geralmente o dispositivo fisicamente mais próximo da origem).
Interrede (Internetwork)
Quando redes geograficamente dispersas e baseadas em tecnologias de enlace de dados heterogêneas são unidas fisicamente por roteadores (gateways), surge uma interrede (do inglês internetwork). A infraestrutura mundial conhecida como Internet fundamenta-se exatamente nesse princípio de interconexão de dezenas de milhares de redes locais ou de trânsito sob diferentes domínios e políticas econômicas.

---

## 6.2 Modelo OSI

Modelo OSI O Modelo OSI (Open Systems Interconnection) é um modelo de referência conceitual estruturado em sete camadas desenvolvido no âmbito da ISO durante a década de 1970 para estabelecer uma base comum de padronização para redes de computadores. Ele define uma divisão teórica detalhada e estrita das funções de comunicação. Contudo, muitas de suas especificações eram extremamente complexas e difíceis de implementar de forma completa, o que limitou sua adoção direta em comparação com alternativas mais pragmáticas

---

## 6.3 Modelo TCP/IP

Modelo TCP/IP O Modelo TCP/IP, detalhado na RFC 1122, constitui a arquitetura de rede real e amplamente implantada sobre a qual a Internet foi construída. Ele simplifica a estrutura do modelo OSI ao consolidar as funções em apenas quatro camadas hierárquicas: Aplicação, Transporte, Internet e Link. Um dos seus principais diferenciais pragmáticos foi mover de forma implícita as funções das camadas de apresentação e sessão do modelo OSI para dentro da própria camada de aplicação

---

## 6.4 Endereçamento IP

Endereçamento IP O Endereçamento IP é o mecanismo de identificação lógica e única atribuído a cada interface de rede física ou lógica de um host ou roteador. Na versão clássica da arquitetura (IPv4), o endereço possui um tamanho fixo de 32 bits e é representado em formato decimal separado por pontos. Para suprir a escassez de espaço, a versão moderna (IPv6) utiliza endereços de 128 bits, subdivididos de forma hierárquica em prefixo de roteamento global, identificador de sub-rede e identificador de interface de 64 bits

---

## 6.5 Máscara de Sub-rede

Máscara de Sub-rede A Máscara de Sub-rede (netmask) é um parâmetro de 32 bits constituído por bits sequenciais de valor 1 seguidos por bits de valor 0, onde a quantidade de bits em 1 indica o comprimento do identificador de rede. Ela é associada ao IP local do dispositivo para viabilizar a decisão de roteamento local ou remoto. Ao realizar uma operação lógica com a máscara, o host verifica se os bits de rede do IP de destino coincidem com os seus próprios; caso coincidam, os dados são entregues diretamente pela rede física local.

---

## 6.6 Gateway

Um Gateway (comumente denominado roteador IP) é um sistema intermediário de comutação de pacotes responsável por interconectar redes geograficamente dispersas e baseadas em diferentes tecnologias físicas. Por questões de robustez e tolerância a falhas, os gateways da Internet são projetados para atuar de forma livre de estado (stateless), encaminhando cada datagrama IP de forma totalmente independente e sem guardar registros de fluxos. Com isso, toda a responsabilidade de gerenciar a integridade e o fluxo de dados ponta a ponta é deliberadamente transferida para as máquinas das extremidades.

---

## 6.7 DNS

DNS O Domain Name System (DNS) é um banco de dados hierárquico e distribuído operado sob o modelo cliente-servidor, projetado para traduzir nomes de domínio legíveis por humanos em endereços IP interpretáveis pelas máquinas. Embora possa rodar sobre conexões TCP para transferências volumosas, o protocolo DNS utiliza prioritariamente pacotes de datagramas UDP para realizar consultas e respostas rápidas na rede. Suas mensagens estruturam-se em um cabeçalho fixo com identificador numérico de 16 bits (utilizado pelo cliente para parear perguntas e respostas) seguido pelas seções de Pergunta, Resposta, Autoridade e Recursos Adicionais.

---

## 6.8 DHCP

DHCP O Dynamic Host Configuration Protocol (DHCP), normatizado na RFC 2131, elimina a necessidade de configuração manual ao prover a atribuição automatizada de parâmetros de rede a hosts novos na sub-rede. Utilizando mensagens UDP trocadas com o servidor na porta 67, o dispositivo obtém temporariamente um IP livre de um pool de endereços gerido localmente. No mesmo pacote de resposta, o servidor DHCP envia informações de suporte vitais, incluindo a máscara de sub-rede, o IP do gateway padrão da rede e as rotas dos resolvedores DNS locais.

---

## 6.9 TCP e UDP

TCP O Transmission Control Protocol (TCP) é um protocolo de transporte orientado a conexões que provê uma entrega de fluxo de bytes bidirecional, confiável e estritamente ordenada para as aplicações. Ele garante que os dados cheguem íntegros através de números de sequência para remontagem, somas de verificação para integridade e retransmissões de pacotes perdidos. O estabelecimento desse canal requer o processo de negociação de três etapas (three-way handshake usando flags SYN e ACK), e os estados da sessão são armazenados no host em uma estrutura chamada Bloco de Controle de Transmissão (TCB).

UDP O User Datagram Protocol (UDP) é um protocolo de transporte extremamente minimalista, sem conexão e não confiável que foca na entrega rápida de pacotes sem garantias de chegada ou ordenamento. Para manter o menor overhead possível, o UDP utiliza um cabeçalho simplificado de apenas 8 bytes que armazena unicamente as portas de comunicação, o comprimento e o checksum. A soma de verificação serve para identificar corrupção de dados física, fazendo com que pacotes com erros sejam descartados sem serem repassados à aplicação. É altamente preferido por sistemas que priorizam latência mínima, como jogos online rápidos, sistemas de arquivos locais como o NFS ou conexões VoIP.

---

# 📖 7. Glossário

IP
Protocolo da camada de rede que provê um serviço de entrega de datagramas não confiável, sem conexão (best-effort) e sem garantias de entrega de ponta a ponta. É responsável pelas funções essenciais de endereçamento, roteamento através de sistemas intermediários (roteadores/gateways) e fragmentação/remontagem de datagramas.
IPv4
Versão de IP que utiliza identificadores de interface com endereçamento lógico de 32 bits, geralmente representado em formato decimal separado por pontos (ex: 127.0.0.1). Ele fornece um serviço de transporte de datagramas não confiável e sem conexão.
IPv6
Versão sucessora do IPv4 que utiliza endereços de 128 bits, representados como conjuntos hexadecimais separados por dois-pontos (ex: fe80::1). Foi projetada para permitir autoconfiguração de endereços, processamento de cabeçalho simplificado para hardware e integração nativa de segurança.
TCP
Protocolo de transporte orientado a conexões que provê entrega de dados virtual, bidirecional (full-duplex), em sequência estrita e livre de erros (confiável) para as aplicações. Suas sessões armazenam estados de controle em uma estrutura do host chamada Bloco de controle de Transmissão (TCB).
UDP
Protocolo de transporte minimalista, sem conexão (connectionless) e não confiável que oferece apenas multiplexação de portas e verificação básica de integridade por meio de checksum, repassando o datagrama IP quase diretamente à aplicação.
DNS
Banco de dados distribuído e hierárquico operado sob o modelo cliente-servidor que realiza o mapeamento entre nomes de domínio amigáveis (legíveis por humanos, como FQDNs) e endereços IP numéricos interpretáveis pelas máquinas.
DHCP
Protocolo da camada de aplicação que automatiza a configuração de rede de novos hosts ao atribuir temporariamente (via concessão/lease) endereços IP disponíveis em um pool local e fornecer parâmetros cruciais como máscara de sub-rede, IP do gateway padrão e resolvedores DNS.
Gateway
Computador de comutação de pacotes responsável por interconectar redes físicas. No modelo de comunicação da Internet, gateways (ou roteadores IP) operam de forma livre de estado (stateless), tratando cada datagrama IP independentemente para otimizar a tolerância a falhas na rede.
Roteador
Dispositivo de retransmissão intermediário que opera na camada de rede para viabilizar a entrega de pacotes entre sistemas finais de diferentes sub-redes. Toma decisões de encaminhamento (forwarding) para cada pacote consultando tabelas de roteamento locais.
Switch
Dispositivo de retransmissão que opera na camada de enlace de dados (datalink). Ele inspeciona o cabeçalho de quadros Ethernet físicos e os encaminha seletivamente para portas específicas baseado em uma tabela dinâmica de endereçamento MAC.
MAC Address
Endereço físico e exclusivo de hardware de 48 bits (ou 64 bits em tecnologias recentes) atribuído na fábrica a uma interface ou adaptador de rede para viabilizar a entrega de quadros de dados na camada de enlace local.
Porta
Identificador numérico de 16 bits usado em nível de transporte (TCP/UDP) para demultiplexar conexões concorrentes e rotear dados recebidos até a aplicação ou processo correto no host de destino.
Protocolo
Conjunto de regras semânticas e sintáticas preestabelecidas que definem o formato exato das mensagens trocadas, como a informação é codificada em bits e a ordenação do fluxo de dados para que os dispositivos em rede se compreendam.
Sub-rede
Divisão lógica ou agrupamento de hosts de acordo com sua localização física para melhorar a escalabilidade do roteamento global. O endereço IP é dividido em uma máscara lógica com identificador de sub-rede (bits superiores) e identificador de host (bits inferiores).
Firewall
Dispositivo de hardware ou software (que pode rodar localmente no host) encarregado de aplicar a política de segurança de uma rede através da análise dos campos de cabeçalho (IP/transporte) e de payload dos pacotes para aceitá-los ou descartá-los.

---

# ♻️ 8. Prompts Reutilizáveis

### 📌 Explicação de conceito

> Com base exclusivamente nas fontes deste notebook, explique [CONCEITO] de forma clara e progressiva. Comece pela definição, explique como funciona, apresente um exemplo prático e indique as fontes utilizadas.

### 📌 Comparação

> Compare [CONCEITO A] e [CONCEITO B] com base nas fontes disponíveis. Apresente as diferenças em uma tabela e explique em quais situações cada um é utilizado.

### 📌 Revisão

> Crie 10 perguntas de revisão sobre [TEMA], utilizando exclusivamente as fontes deste notebook. Comece com perguntas básicas e aumente gradualmente a dificuldade. Não apresente as respostas inicialmente.

### 📌 Teste de conhecimento

> Faça um teste sobre [TEMA] com 10 questões de múltipla escolha. Apresente uma questão por vez, aguarde minha resposta e explique por que minha resposta está correta ou incorreta utilizando as fontes do notebook.

### 📌 Identificação de lacunas

> Analise os principais conceitos relacionados a [TEMA] presentes nas fontes deste notebook e identifique quais conceitos são fundamentais para compreender o assunto, mas ainda não foram abordados suficientemente neste estudo.

### 📌 Aprendizado baseado em cenário

> Crie um cenário prático de redes em que seja necessário utilizar os conceitos de [CONCEITO 1], [CONCEITO 2] e [CONCEITO 3]. Apresente o problema e peça para que eu proponha uma solução antes de explicar a resposta.

---

# 💭 9. Reflexão Final

A utilização do NotebookLM permitiu transformar diferentes fontes de estudo em um ambiente de consulta mais organizado e interativo.

Durante o projeto, foi possível perceber que a qualidade das respostas depende não apenas da ferramenta utilizada, mas também da qualidade das fontes selecionadas e da maneira como as perguntas são formuladas.

Os experimentos demonstraram que prompts mais específicos, contextualizados e orientados às fontes produzem respostas mais úteis para o processo de aprendizagem.

O principal resultado deste projeto foi a consolidação de um método de estudo no qual a IA atua como ferramenta de apoio à investigação, revisão e organização do conhecimento, sem substituir a análise crítica das fontes originais.

---

## 🛠️ Tecnologias e Ferramentas

* [NotebookLM](https://notebooklm.google.com/)
* GitHub
* Markdown

---

## 👨‍💻 Autor

**Vinícius Rodrigues Leite**

Projeto desenvolvido para o Desafio de Projeto da DIO.
