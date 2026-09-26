*PDF página 1*
![[Pasted image 20260705151127.png]]

![[Pasted image 20260831164237.png]]

Apesar de tais benefícios potenciais, a implementação de sistemas de agricultura inteligente ainda está em estágio inicial. De fato, um obstáculo à digitalização da agricultura é a ausência ou as limitações de conectividade à Internet em muitas áreas. Na literatura, diversos protocolos de comunicação foram propostos, apresentando características distintas em termos de custo, cobertura, consumo de energia e confiabilidade [9]. Dentre as tecnologias disponíveis (resumidas na Fig. 1 quanto ao consumo de energia e alcance de cobertura), as redes de longa distância e baixo consumo (LPWANs) destacadas em uma caixa tracejada na Fig. 1 representam a melhor solução para atender aos requisitos da agricultura inteligente. Uma das tecnologias LPWAN mais adotadas é a LoRaWAN, que oferece ampla cobertura de rede, segurança integrada, baixo custo e baixo consumo de energia durante a operação [10].

*PDF página 2*
![[Pasted image 20260705153010.png]]

A tecnologia LoRa tem sido amplamente empregada e testada no setor agrícola, conectando sensores ambientais que medem temperatura, umidade do ar e do solo, entre outros, ou controlando diversos tipos de atuadores (por exemplo, válvulas de irrigação), bem como em aplicações como comunicação entre tratores, monitoramento de rebanhos e rastreamento de localização.

![[Pasted image 20260705151708.png]]

![[Pasted image 20260705153330.png]]

Ele oferece suporte à conectividade sem fio com taxas de dados limitadas em grandes áreas e sem a necessidade de uma operadora. O LoRaWAN é amplamente utilizado na indústria inteligente, em casas inteligentes, cidades inteligentes e, cada vez mais, no ambiente da agricultura inteligente.

![[Pasted image 20260920172857.png]]

Embora a tecnologia LoRa se limite à camada física, diferentes soluções de rede podem ser construídas sobre ela, aproveitando suas interfaces de transmissão. Entre elas, a mais consolidada é a solução de código aberto promovida pela LoRa Alliance, denominada LoRaWAN. As redes LoRaWAN baseiam-se em uma topologia simples de "estrela de estrelas" (Fig. 2): dispositivos finais (EDs) como sensores ou atuadores implantados em campo transmitem pacotes pelo meio sem fio para nós fixos chamados gateways (GWs), os quais, por sua vez, encaminham os pacotes coletados para um servidor de rede (NS) central que interage com diversos servidores de aplicação (ASs).

*PDF Página 09*
![[Pasted image 20260920174006.png]]

Na presença de grandes rebanhos, a alta densidade de nós poderia causar um aumento nas colisões entre pacotes enviados.

