*PDF Página 09*
![[Pasted image 20260913160438.png]]

Uma rede LoRaWAN distingue entre o LoRaWAN básico (chamado de Classe A) e recursos opcionais (Classe B, Classe C...), conforme mostrado na Figura 1.

![[Pasted image 20260913160534.png]]

![[Pasted image 20260913160716.png]]

**Dispositivos finais bidirecionais (Classe A):** Os dispositivos finais de Classe A permitem comunicação bidirecional, na qual a transmissão de *uplink* de cada dispositivo é seguida por duas janelas curtas de recepção em *downlink*. O intervalo de transmissão programado pelo dispositivo baseia-se em suas próprias necessidades de comunicação, com uma pequena variação aleatória no tempo (protocolo do tipo ALOHA). A operação de Classe A representa o modo de menor consumo de energia para aplicações que exigem comunicação em *downlink* a partir do servidor apenas logo após o dispositivo ter realizado uma transmissão de *uplink*. Comunicações em *downlink* provenientes do servidor em qualquer outro momento terão de aguardar até o próximo *uplink* iniciado pelo dispositivo. 

**Dispositivos finais bidirecionais com intervalos de recepção programados (Classe B):** Dispositivos compatíveis com a Classe B permitem mais intervalos de recepção. Além das janelas de recepção da Classe A, os dispositivos habilitados para Classe B abrem janelas de recepção adicionais em horários programados. Para que o dispositivo abra suas janelas de recepção em um horário programado, ele recebe um sinalizador (*beacon*) sincronizado no tempo proveniente do *gateway*. Isso permite que o Servidor de Rede saiba quando o dispositivo está em escuta.

*PDF Página 10*

![[Pasted image 20260913161532.png]]

**Dispositivos finais bidirecionais com capacidade máxima de janelas de recepção (Classe C):** Dispositivos compatíveis com a Classe C permitem janelas de recepção praticamente sempre abertas, sendo fechadas apenas durante a transmissão. Dispositivos habilitados para a Classe C consomem mais energia para operar do que aqueles das Classes A ou B, mas apresentam a menor latência na comunicação entre servidores e dispositivos finais.

*PDF Página 11*
![[Pasted image 20260913162126.png]]

Todos os dispositivos finais LoRaWAN DEVEM implementar todos os recursos da Classe A que não estejam explicitamente marcados como opcionais.

*PDF Página 51*
![[Pasted image 20260913163132.png]]

Todos os dispositivos finais iniciam e ingressam na rede como dispositivos finais de Classe A, com a Classe B desabilitada. A aplicação do dispositivo final pode, então, decidir habilitar a Classe B. Dispositivos finais compatíveis com a Classe B ainda implementam todas as funcionalidades dos dispositivos finais de Classe A. Em particular, dispositivos finais com a Classe B habilitada DEVEM respeitar a definição das janelas de recepção RX1 e RX2 da Classe A após cada transmissão de *uplink* (ver Seção 3.3).

