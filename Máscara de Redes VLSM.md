Máscara de Redes VLSM

Em muitos casos, ao dividir uma rede apenas utilizando CIDR, ocorre desperdício de diversos endereços IP que poderiam ser utilizados. Esse problema pode ser corrigido com o uso de VLSM (Variable Length Subnet Mask).

Exemplo: Suponha que seja necessário criar sub-redes para 2, 10 e 50 hosts. Com o VLSM, é possível dividir a rede de forma eficiente, atribuindo a cada sub-rede uma máscara adequada à sua necessidade, evitando o desperdício de endereços IP.

|Requisitos|Calculo|Máscara|
| --- | --- | --- | 
|50|$2^6$=64 256-64=192|255.255.255.192|
|10|$2^3$=12 256-12=240|255.255.255.240|
|2|$2^2$=4 256-4=252|255.255.255.252|
