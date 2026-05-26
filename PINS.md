# Pinos

Esta página apresenta informações sobre os pinos do CYD.

## Tipos de conectores

Os conectores são frequentemente chamados de "JST de 1,25 mm", mas o nome correto é "Molex PicoBlade".
Clones às vezes são chamados de "mx1.25".

|Conector       |Tipo    |Observação                       |
|---------------|-----------------------------|------------|
|[**P1**](#p1)  |Molex PicoBlade 4P de 1,25 mm|Serial      |
|[**P3**](#p3)  |Molex PicoBlade 4P de 1,25 mm|GPIO        |
|[**P4**](#p4)  |Molex PicoBlade 2P de 1,25 mm|Alto-falante|
|[**CN1**](#cn1)|Molex PicoBlade 4P de 1,25 mm|GPIO (I2C)  |

## Quais pinos estão disponíveis no CYD?

Há 3 pinos GPIO facilmente acessíveis.

|Pino|Localização|Observação|
|----|-------------------------------------------|-------------------------------------------------------------|
|IO35|Conector Molex PicoBlade **P3**.           |Pino somente de entrada; não há pull-ups internos disponíveis|
|IO22|Conectores Molex PicoBlade **P3** e **CN1**|.                                                            |
|IO27|Conector Molex PicoBlade **CN1**.          |.                                                            |

Se precisar de mais pinos, será necessário obtê-los de outro componente. Um SD Card sniffer, como mencionado em [Complementos](/ADDONS.md), provavelmente é a próxima opção mais simples.

Depois disso, provavelmente será necessário dessoldar algum componente!

## Pinos disponibilizados

Há três conectores Molex PicoBlade 4P de 1,25 mm na placa.

### P3
|Pino|Uso|Observação|
|---|---|----|
|GND|||
|IO35||Pino somente de entrada; não há pull-ups internos disponíveis|
|IO22||Também presente no conector **CN1**|
|IO21||Usado para a iluminação de fundo do TFT, portanto não é realmente utilizável|

### CN1
Este é um ótimo candidato para dispositivos I2C.

|Pino|Uso|Observação|
|---|---|----|
|GND|||
|IO22||Também presente no conector **P3**|
|IO27|||
|3.3V|||

### P1
|Pino|Uso|Observação|
|---|---|----|
|VIN|||
|IO1(?)|TX|Talvez possa ser usado como GPIO?|
|IO3(?)|RX|Talvez possa ser usado como GPIO?|
|GND|||


## Botões

O CYD tem dois botões: reset e boot.

|Pino|Uso|Observação|
|---|---|----|
|IO0|BOOT|Pode ser usado como entrada em códigos|

## Alto-falante

O conector do alto-falante é um conector Molex PicoBlade 2P de 1,25 mm conectado ao amplificador, portanto não pode ser usado como GPIO no conector do alto-falante.

|Pino|Uso|Observação|
|---|---|----|
|IO26|Conectado ao amplificador|`i2s_set_dac_mode(I2S_DAC_CHANNEL_LEFT_EN);`|

## LED RGB

Se seu projeto precisar de pinos adicionais além dos disponíveis em outros locais, este pode ser um bom candidato para ser sacrificado.

Observação: os LEDs são "active low", o que significa que HIGH == desligado e LOW == ligado.

|Pino|Uso|Observação|
|---|---|----|
|IO4|LED vermelho||
|IO16|LED verde||
|IO17|LED azul||

## Cartão SD
Usa o VSPI.
Os nomes dos pinos são predefinidos em SPI.h.

|Pino|Uso|Observação|
|---|---|----|
|IO5|SS||
|IO18|SCK||
|IO19|MISO||
|IO23|MOSI||

## Tela sensível ao toque

|Pino|Uso|Observação|
|---|---|----|
|IO25|XPT2046_CLK||
|IO32|XPT2046_MOSI||
|IO33|XPT2046_CS||
|IO36|XPT2046_IRQ||
|IO39|XPT2046_MISO||

## LDR (sensor de luz)

|Pino|Uso|Observação|
|---|---|----|
|IO34|||

## Tela
Usa o HSPI.

|Pino|Uso|Observação|
|---|---|----|
|IO2|TFT_RS|AKA: TFT_DC|
|IO12|TFT_SDO|AKA: TFT_MISO|
|IO13|TFT_SDI|AKA: TFT_MOSI|
|IO14|TFT_SCK||
|IO15|TFT_CS||
|IO21|TFT_BL|Também presente no conector P3, por algum motivo|

## Pontos de teste
|Pad|Uso|Observação|
|---|---|----|
|S1|GND|próximo ao USB-SERIAL|
|S2|3.3v|para o ESP32|
|S3|5v|próximo ao USB-SERIAL|
|S4|GND|para o ESP32|
|S5|3.3v|para o TFT|
|JP0 (pad mais próximo da porta USB)|5v|TFT LDO|
|JP0|3.3v|TFT LDO|
|JP3 (pad mais próximo da porta USB)|5v|ESP32 LDO|
|JP3|3.3v|ESP32 LDO|
