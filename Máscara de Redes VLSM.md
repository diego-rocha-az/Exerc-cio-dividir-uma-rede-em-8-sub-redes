Máscara de Redes VLSM

Em muitos casos, ao dividir uma rede apenas utilizando CIDR, ocorre desperdício de diversos endereços IP que poderiam ser utilizados. Esse problema pode ser corrigido com o uso de VLSM (Variable Length Subnet Mask).

Exemplo: Suponha que seja necessário criar sub-redes para 2, 10 e 50 hosts. Com o VLSM, é possível dividir a rede de forma eficiente, atribuindo a cada sub-rede uma máscara adequada à sua necessidade, evitando o desperdício de endereços IP.

|Requisitos|Calculo|Máscara|
| --- | --- | --- | 
|50|2^6=64 256-64=192|255.255.255.192|
|10|2^3=12 256-12=240|255.255.255.240|
|2|2^2=4 256-4=252|255.255.255.252|

Exercícios de Fixação: VLSM com Múltiplas Classes
Instruções: Para cada exercício, utilize a Rede Base e o Prefixo Inicial fornecidos. Planeje o endereçamento
VLSM para atender a TODOS os requisitos de hosts listados, alocando os blocos de endereços na ordem do
maior para o menor requisito. Preencha a tabela para cada sub-rede alocada.
Exercício 1 (Rede Classe C)
Rede Base: 192.168.20.0/24
|Setor|Hosts Necessários|Ordem de Alocação|Calculo|Máscara CIDR|Endereço de Rede|Intervalo de Hosts|Endereço de Broadcast|
| --- | --- | --- | --- | --- | --- | --- | --- |
|Treinamento|60|1|2^6=64 256-64=192|/26|192.168.20.0|64|192.168.20.63|
|RH|28|2|2^5=32 256-32=224|/27|192.168.20.64|32|192.168.20.95|
|TI|12|3|2^4=16 256-16=240|/28|192.168.20.96|16|192.168.20.111|
|Vendas|5|4|2^3=8 256-8=248|/29|192.168.20.112|8|192.168.20.121|
|Link|2|5|2^2=4 256-4=254|/31|192.168.20.120|4|192.168.20.123|

Exercício 2 (Rede Classe B)
Rede Base: 172.16.1.0/24
|Setor|Hosts Necessários|Ordem de Alocação|Calculo|Máscara CIDR|Endereço de Rede|Intervalo de Hosts|Endereço de Broadcast|
| --- | --- | --- | --- | --- | --- | --- | --- |
|Desenvolvimento|100|1|2^7=128 256-128=128|/25|172.16.1.0|128|172.16.1.127|
|Operacional|50|2|2^6=64 256-192=192|/26|172.16.1.128|64|172.16.1.191|
|Administração|25|3|2^5=32 256-32=224|/27|172.16.1.192|32|172.16.1.223|
|Financeiro|10|4|2^4=16 256-16=240|/28|172.16.1.224|16|172.16.1.239|
