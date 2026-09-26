*PDF Página 02*

![[Pasted image 20260926155334.png]]

No entanto, existe um limite quanto ao número de transmissores que um sistema LoRa pode suportar. Neste artigo, investigamos os limites de capacidade das redes LoRa. Por meio de experimentos, desenvolvemos modelos que descrevem o comportamento da comunicação LoRa. Utilizamos esses modelos para parametrizar uma simulação LoRa e estudar a escalabilidade.

*PDF Página 06*

![[Pasted image 20260926153513.png]]

Utilizamos um simulador para examinar e compreender a escalabilidade de redes LoRa. Não é viável avaliar a escalabilidade de redes LoRa em larga escala na prática, uma vez que a implementação de tais redes seria proibitivamente cara. Além disso, uma implementação real não nos permitiria testar uma variedade maior de configurações e topologias, conforme necessário para um estudo abrangente sobre escalabilidade. No entanto, para garantir que nossos resultados tenham relevância prática, utilizamos os experimentos práticos mencionados anteriormente para calibrar nossa simulação.

![[Pasted image 20260926154616.png]]

O LoRaSim nos permite posicionar N nós LoRa em um espaço bidimensional (disposição em grade ou distribuição aleatória).

![[Pasted image 20260926154801.png]]

Cada nó LoRa possui uma característica de comunicação específica definida pelos parâmetros de transmissão TP, CF, SF, BW e CR. Para um experimento, o comportamento de transmissão de cada nó é descrito pela taxa média de transmissão de pacotes λ e pela carga útil (payload) do pacote B.

**TP — Transmission Power** → potência de transmissão;
**CF — Carrier Frequency** → frequência central;
**SF — Spreading Factor** → fator de espalhamento;
**BW — Bandwidth** → largura de banda;
**CR — Coding Rate** → taxa de codificação.

*PDF Página 06*

![[Pasted image 20260926161639.png]]

Para avaliar a escalabilidade e o desempenho de implantações LoRa, definimos duas métricas: Taxa de Extração de Dados (DER) e Consumo de Energia da Rede (NEC).

*PDF Página 07*

![[Pasted image 20260926161808.png]]

DER: Em uma implementação LoRa eficaz, todas as mensagens transmitidas devem ser recebidas pelo sistema de *backend*. Isso significa que cada mensagem transmitida deve ser recebida corretamente por pelo menos um *sink* LoRa. Definimos a Taxa de Extração de Dados (DER) como a razão entre as mensagens recebidas e as mensagens transmitidas ao longo de um período de tempo. A DER alcançável depende da posição, do número e do comportamento dos nós e *sinks* LoRa, definidos por N, M e SN. A DER é um valor entre 0 e 1; quanto mais próximo de 1 for o valor, mais eficaz será a implementação LoRa. Em uma implementação perfeita, esperar-se-ia que a DER fosse igual a 1. Essa métrica não avalia o desempenho individual dos nós, mas sim a implementação da rede como um todo.

![[Pasted image 20260926162443.png]]

NEC: O consumo de energia de um nó LoRa dependerá, na maioria dos cenários, principalmente do consumo de energia do transceptor. Como os nós serão frequentemente implantados utilizando baterias, é essencial manter o consumo de energia das transmissões no nível mínimo. O consumo de energia de transmissão para cada mensagem depende da potência de transmissão (TP) e da duração da transmissão, a qual é influenciada pelos parâmetros SF, BW e CR. Definimos o NEC (Consumo de Energia da Rede) como a energia gasta pela rede para extrair uma mensagem com sucesso. O NEC depende do número de nós, da frequência das transmissões e dos parâmetros de comunicação do transmissor. Quanto menor o valor dessa métrica, mais eficiente é a implantação, pois a vida útil dos nós é prolongada. A energia necessária para extrair uma mensagem deve ser independente do número de nós implantados na rede. Ressalta-se que essa métrica não reflete o comportamento individual dos nós, mas sim a implantação da rede como um todo.

![[Pasted image 20260926161131.png]]

*PDF Página 09*

![[Pasted image 20260926155737.png]]

Conforme aumenta o número de dispositivos, a Data Extraction Rate (DER) diminui.

![[Pasted image 20260926160649.png]]

![[Pasted image 20260926160830.png]]

Nossa expectativa era que, com o aumento do número de *sinks*, a rede ficasse saturada e a DER, de fato, diminuísse. A figura, no entanto, mostra que não é isso o que ocorre. Acreditamos que isso se deve ao fato de ser necessário apenas um *sink* onde o efeito de captura atue para garantir que um pacote possa, eventualmente, ser recebido. Com mais *sinks*, aumentam as chances de um pacote encontrar um *sink* onde o efeito de captura opere a seu favor. Com um número infinito de *sinks*, cada nó poderia encontrar tal *sink*, evitando a perda de pacotes.

