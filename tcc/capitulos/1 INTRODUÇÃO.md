A cadeia produtiva de caprinos e ovinos possui relevância social e econômica para o Semiárido brasileiro, por contribuir para a geração de renda, a ocupação e a produção de alimentos para famílias rurais [[melo-01|(Melo, 2011, p. 15) ]]. Segundo dados da Pesquisa da Pecuária Municipal (PPM), realizada pelo Instituto Brasileiro de Geografia e Estatística (IBGE), o rebanho ovino brasileiro alcançou 21,8 milhões de cabeças em 2023 [[ibge-01|(IBGE, 2024)]]. No contexto estadual, o Ceará registrou aproximadamente 2,6 milhões de ovinos em 2024, com crescimento de 3,04% em relação ao ano anterior. Municípios como Tauá, Independência, Morada Nova, Quixeramobim e Quixadá destacam-se entre os principais rebanhos ovinos cearenses, enquanto regiões como o Sertão dos Inhamuns, o Vale do Jaguaribe, o Sertão dos Crateús e o Sertão Central concentram parcela significativa do rebanho de caprinos e ovinos do estado, reforçando a importância dessas áreas para a manutenção e o crescimento da atividade [[ceara-01|(CEARÁ, 2025)]].

--- ---

Nesse cenário, a modernização da ovinocultura torna-se um aspecto importante para o fortalecimento da atividade no contexto regional. Em sistemas pecuários, os métodos
tradicionais de acompanhamento dos animais podem demandar maior esforço operacional e depender de observações manuais, o que pode limitar a identificação rápida de alterações no rebanho. Nesse sentido, ferramentas de pecuária de precisão baseadas em sensores, Internet das Coisas (IoT) e análise de dados podem fornecer informações de forma contínua ou em tempo real sobre os animais, contribuindo para melhorar o manejo, apoiar a tomada de decisão do produtor e tornar mais eficiente o uso dos recursos disponíveis [[bhaskaran-et-al-2024-01|(Bhaskaran et al., 2024)]].

--- ---

A adoção dessas tecnologias aproxima a ovinocultura dos princípios da pecuária de precisão, na qual sensores, sistemas de comunicação e plataformas de dados são utilizados para acompanhar animais e ambientes de produção de forma mais contínua. [[terence-et-al-2024-01|Terence et al. (2024) ]]destacam que a IoT tem sido aplicada em sistemas de manejo pecuário para permitir a coleta de informações em locais remotos, automatizar atividades da propriedade e apoiar o acompanhamento dos animais. Dessa forma, o uso de sensores e dispositivos conectados pode auxiliar o produtor no monitoramento de informações relacionadas ao comportamento, à saúde e às condições do ambiente de criação.

--- ---

Entretanto, a aplicação de sistemas de monitoramento em propriedades rurais depende de tecnologias de comunicação adequadas às condições do campo. [[macedo-et-al-2023-01|Macedo et al. (2023)]] destacam que a conexão de dispositivos remotos em áreas rurais representa um caso de uso desafiador para tecnologias de comunicação voltadas à IoT, exigindo soluções capazes de cobrir áreas extensas, com baixo consumo de energia e custo reduzido. Nesse sentido, redes do tipo Low-Power Wide-Area Network (LPWAN), como a Long Range Wide Area Network (LoRaWAN), apresentam-se como alternativas compatíveis com aplicações agropecuárias que não exigem altas taxas de transmissão de dados e precisam operar em ambientes rurais extensos [[pagano-et-al-2023-01|(Pagano et al., 2023)]]. Essa característica é relevante para cenários de monitoramento animal, nos quais os dispositivos precisam funcionar em campo, muitas vezes alimentados por bateria, e transmitir dados em intervalos definidos, de acordo com a aplicação de monitoramento proposta.

--- ---

No contexto do Sertão cearense, [[araujo-2024-01|Araújo (2024)]] apresenta um exemplo aplicado dessa abordagem ao desenvolver um protótipo para o monitoramento de sinais vitais de ovinos utilizando comunicação por Long Range (LoRa). O sistema proposto realiza a coleta de parâmetros fisiológicos, como temperatura corporal e frequência cardíaca, e transmite os dados para armazenamento e visualização em uma plataforma computacional. Nos testes realizados, o protótipo foi fixado ao animal, com os sensores posicionados em contato com a pele do ovino, e os dados foram coletados periodicamente, a cada cinco minutos, durante dois dias, permitindo acompanhar as variações dos sinais vitais em ambiente rural. Dessa forma, o trabalho evidencia a possibilidade de utilizar dispositivos conectados para apoiar o monitoramento remoto de ovinos em regiões com limitações de infraestrutura de comunicação.

--- ---

Embora a LoRaWAN apresente características adequadas para aplicações rurais de baixo consumo e longo alcance, seu desempenho pode ser afetado pelo aumento da quantidade
de dispositivos, pela distribuição espacial dos nós sensores e pelas variações nas condições de co-
municação. [[sarmento-neto-et-al-2025-01|Sarmento Neto et al. (2025)]] destacam que o mecanismo Adaptive Data Rate (ADR),
utilizado para ajustar dinamicamente parâmetros de transmissão, foi originalmente projetado
para dispositivos estáticos, apresentando limitações em ambientes móveis, nos quais as condições
do canal variam com maior frequência. No estudo, os autores avaliaram a escalabilidade de redes
LoRaWAN com até 1.000 dispositivos finais, considerando diferentes modelos de mobilidade
e métricas como taxa de entrega de pacotes, do inglês Packet Delivery Ratio (PDR), eficiência
energética, vazão e razão de colisões. Dessa forma, em aplicações de monitoramento de ovinos,
nas quais os dispositivos podem estar distribuídos em diferentes condições espaciais e transmitir
dados periodicamente, torna-se necessário analisar como a rede se comporta diante do aumento
da quantidade de nós sensores.

--- --- 

Nesse contexto, observa-se uma oportunidade de investigação voltada à análise da escalabilidade da comunicação em sistemas de monitoramento de ovinos. Embora Araújo (2024) tenha demonstrado a viabilidade de um protótipo para coleta e transmissão de sinais vitais
de ovinos no Sertão cearense utilizando comunicação por Long Range (LoRa), o estudo não
teve como foco avaliar o desempenho da rede diante do aumento da quantidade de animais
monitorados. Desse modo, este projeto propõe avaliar, por meio de simulação computacional,
uma rede Long Range Wide Area Network (LoRaWAN) aplicada ao monitoramento de ovinos
no Sertão Central, considerando cenários de confinamento e pastagem, a variação no número
de nós sensores e os efeitos dessa variação sobre o desempenho da comunicação. A proposta
limita-se à análise do comportamento da rede simulada, não abrangendo o desenvolvimento de
novos dispositivos, protocolos ou algoritmos de adaptação.