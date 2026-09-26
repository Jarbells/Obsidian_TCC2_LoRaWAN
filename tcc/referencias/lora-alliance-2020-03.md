*PDF Página 07*
![[Pasted image 20260914182752.png]]

A comunicação entre dispositivos finais e gateways é distribuída por diferentes canais de frequência e taxas de dados. A seleção da taxa de dados envolve um compromisso entre o alcance da comunicação e a duração da transmissão; comunicações com diferentes taxas de dados LoRa não interferem entre si. Para maximizar tanto a vida útil da bateria dos dispositivos finais quanto a capacidade geral da rede, a infraestrutura da rede LoRaWAN PODE gerenciar a taxa de dados e a potência de transmissão de RF de cada dispositivo final individualmente, por meio de um esquema de taxa de dados adaptativa (ADR).

*PDF Página 18*
![[Pasted image 20260914183619.png]]

4.3.1.1 Controle adaptativo de taxa de dados no cabeçalho do quadro (ADR, ADRACKReq em FCtrl) 
O LoRaWAN permite que os dispositivos finais utilizem qualquer uma das taxas de dados e potências de transmissão (TX) possíveis, de forma individual. Esse recurso é utilizado pelos Servidores de Rede para adaptar e otimizar o número de retransmissões, a taxa de dados e a potência de transmissão dos dispositivos finais. Esse mecanismo é denominado taxa de dados adaptativa (ADR) e, quando habilitado, os dispositivos finais são otimizados para utilizar a taxa de dados mais rápida e a menor potência de transmissão possível.

*PDF Página 19*
![[Pasted image 20260914185853.png]]

O dispositivo final DEVE tentar restabelecer a conectividade definindo inicialmente a potência de transmissão (TX) para o valor padrão e, em seguida, alternando para a próxima taxa de dados mais baixa que ofereça um maior alcance de rádio. O dispositivo final DEVE reduzir ainda mais sua taxa de dados, passo a passo, a cada transmissão de quadros de uplink ADR_ACK_DELAY.
