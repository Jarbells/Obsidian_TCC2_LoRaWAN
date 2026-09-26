*PDF Página 01*
![[Pasted image 20260728155025.png]]

No entanto, o ADR foi projetado principalmente para dispositivos estáticos, o que
limita sua eficácia em ambientes móveis, onde as condições de sinal flutuantes podem degradar o desempenho.

*PDF Página 02*
![[Pasted image 20260920161824.png]]

Uma característica essencial da tecnologia LoRaWAN é o mecanismo ADR, que ajusta dinamicamente as configurações de transmissão para melhorar a eficiência da rede e prolongar a vida útil da bateria, estimando a qualidade do canal usando valores de relação sinal-ruído (SNR). Embora seja eficaz para dispositivos estáticos, o ADR tem limitações em cenários móveis, onde mudanças frequentes nas condições do canal podem reduzir seu desempenho. À medida que aplicações móveis de IoT, como rastreamento de ativos, comunicação veicular e monitoramento ambiental, estão se tornando cada vez mais comuns, há uma necessidade crescente de protocolos adaptativos que possam responder a essas condições dinâmicas. Em tais ambientes móveis, o mecanismo ADR padrão pode levar a uma maior perda de pacotes e ao aumento do consumo de energia devido à sua capacidade limitada de se ajustar rapidamente às mudanças nas condições da rede. Portanto, melhorar a ADR para levar em conta a mobilidade é essencial para garantir a confiabilidade e a eficiência necessárias para redes IoT dinâmicas e em grande escala.

*PDF Página 06*
![[Pasted image 20260920161241.png]]

Como discutido anteriormente, o ADR padrão utiliza uma função de máximo para estimar a qualidade do sinal, conforme ilustrado na Fig. 2. No entanto, em ambientes sujeitos a mudanças frequentes nas condições do canal e com dispositivos terminais móveis, a aplicação de indicadores estatísticos como valores máximos, mínimos ou médios para estimar uma SNR representativa pode levar a estimativas inadequadas, resultando em ajustes imprecisos dos parâmetros de transmissão [32].

*PDF Página 08*
![[Pasted image 20260728161133.png]]

Nas simulações realizadas, todos os cenários foram implementados em C++ e executados utilizando o NS-3, com a integração do módulo LoRaWAN [10, 20, 22]. O ambiente de simulação compreende uma rede com um único gateway e um servidor de rede, juntamente com 200 a 1.000 dispositivos finais LoRa distribuídos em uma área quadrada com 10 km de lado, de forma semelhante à configuração proposta em [11]. Os dispositivos finais transmitem 144 pacotes periodicamente ao longo de um período de 24 horas.
Para modelar um canal mais realista, utilizou-se o modelo de perda de percurso log-distância [39]. Além disso, simularam-se efeitos de sombreamento mediante a aplicação de variações estocásticas de sinal associadas a obstáculos ambientais e reflexões [40].

![[Pasted image 20260728161410.png]]

Os cenários utilizados para avaliar a escalabilidade do MB-ADR empregam os modelos de mobilidade discutidos na Seção 5: Random Walk, Steady-State Random Waypoint e Gauss–Markov. Além disso, de forma semelhante à abordagem em [17], este estudo adota intervalos de velocidade que representam diversas aplicações com diferentes objetos móveis:

*PDF Página 09*
![[Pasted image 20260925182315.png]]

Para discutir os resultados, foram adotadas diversas métricas frequentemente utilizadas em simulações de protocolos de comunicação sem fio, especialmente em redes LoRaWAN. Essas métricas incluem a taxa de entrega de pacotes, a eficiência energética e a latência. Cada uma delas fornece informações relevantes sobre diferentes aspectos do desempenho da rede, como confiabilidade, consumo de energia e os efeitos de interferência e das condições do canal.
A PDR é definida como a razão entre o número de pacotes recebidos com sucesso pelo gateway e o total de pacotes transmitidos pelo dispositivo, conforme mostrado na Eq. (12). Essa métrica é essencial para avaliar a confiabilidade da comunicação, indicando a eficácia da entrega de dados na rede.

*PDF Página 10*

![[Pasted image 20260925181916.png]]

7.1. Escalabilidade em relação ao número de dispositivos finais.

Esta subseção apresenta uma análise detalhada dos modelos de mobilidade, incluindo RW, SSRWP e GM. Conforme mencionado anteriormente, um número variável de dispositivos finais é implantado neste cenário, com velocidades situadas na faixa da Classe 3, a qual representa uma categoria de mobilidade intermediária com velocidades aleatórias entre 8 e 12 m/s.

*PDF Página 11*
![[Pasted image 20260728163342.png]]
