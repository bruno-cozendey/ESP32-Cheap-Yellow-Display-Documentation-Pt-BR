# Complementos

Aqui está uma lista de complementos de hardware que podem adicionar funcionalidades ao seu CYD.

## Adaptador para cartão SD

Se quiser usar os pinos do cartão SD para outra finalidade, a maneira mais fácil é usar um "SD card sniffer", que basicamente se conecta ao slot do cartão SD e disponibiliza os pinos. Ele é especialmente útil para dispositivos SPI.

## Pinagem da placa Sniffer

| Identificação na placa Sniffer | Pino do ESP32 | Uso SPI   |
| ------------------------------ | ------------- | --------- |
| DAT2                           | -             | -         |
| CD                             | IO5           | CS        |
| CMD                            | IO23          | DI / MOSI |
| GND                            | GND           | -         |
| VCC                            | 3.3V          | -         |
| CLK                            | IO18          | SCLK      |
| DAT0                           | IO19          | DO / MISO |
| DAT1                           | -             | -         |

### Links

- [Micro SD Card Sniffer - Aliexpress\*](https://s.click.aliexpress.com/e/_Ddwcy9h)

## Nintendo Wii Nunchuck

Um controle Nunchuck de Nintendo Wii é um excelente dispositivo de entrada para projetos com o CYD, pois é barato e, como usa i2c para comunicação, requer apenas 2 pinos GPIO para conexão.

Com esses dois pinos, você obtém:

- Um controle analógico
- 2 botões
- Um acelerômetro

### Hardware necessário

#### Controles Nunchuck

Os controles oficiais da Nintendo geralmente são melhores (peças usadas), mas os de terceiros/paralelos também funcionam bem.

- [Busca na Amazon.co.uk\*](https://amzn.to/3nQrXcE)
- [Busca na Amazon.com\*](https://amzn.to/3nRJTUd)
- [Aliexpress (terceiros)\*](https://s.click.aliexpress.com/e/_AaQbXh)

#### Adaptadores Nunchuck

Há várias opções disponíveis; até os modelos baratos do Aliexpress funcionam perfeitamente.

- [Aliexpress](https://s.click.aliexpress.com/e/_AEEtc3)
- [Meu adaptador open source na Oshpark](https://oshpark.com/shared_projects/RcIxSx2D)
- [Adafruit](https://www.adafruit.com/product/4836)

### Conexão

A maneira mais fácil de realizar a conexão é usar o fio fornecido com o CYD e o conector JST **CN1** (o mais próximo do slot para cartão Micro SD).

Conecte o fio à sua placa breakout da seguinte forma:

| CYD CN1 | Adaptador   | Observação            |
| ------- | ----------- | --------------------- |
| GND     | - (AKA GND) | Fio preto no meu caso |
| 3.3V    | + (AKA 3V)  | Fio vermelho no meu caso |
| IO22    | d (AKA SDA) | Fio azul no meu caso  |
| IO27    | c (AKA SCL) | Fio amarelo no meu caso |

Observação: constatei que resistores pull-up não são necessários em SDA e SCL.

### Exemplo

Consulte o exemplo [NunchuckTest](/Examples/InputTests/NunchuckTest) para ver o código de uso.

## Alto-falantes

Um alto-falante pode ser conectado à tela usando um conector JST de 1,25 mm no conector identificado como "SPEAK" (ou pode ser soldado).

Consulte o exemplo [HelloRadio](/Examples/Basics/7-HelloRadio) para ver o código de uso.

A maioria dos alto-falantes pequenos de 8 Ohm deve funcionar. Pode ser interessante adicionar um conector JST de 1,25 mm para facilitar sua instalação e remoção.

### Links

- [Alto-falante com conector JST de 1,25 mm (2 unidades) - Aliexpress\*](https://s.click.aliexpress.com/e/_DBOJoh7) - Testado, funciona imediatamente após sair da embalagem.
- [Conectores JST de 2 pinos e 1,25 mm - Aliexpress\*](https://s.click.aliexpress.com/e/_DlbPkWH) - Não foram comprados por mim, mas devem funcionar.

\* = Link de afiliado - isso não gera nenhum custo adicional para você, mas recebo uma pequena parte da venda.
