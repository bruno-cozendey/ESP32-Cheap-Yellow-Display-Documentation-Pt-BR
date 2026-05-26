## O que é uma Cheap Yellow Display (CYD)?

Uma CYD é uma ESP32-2432S028, uma placa de desenvolvimento ESP32 com uma tela de 2,8" sensível ao toque resistivo.

Existem outras placas com telas de tamanhos diferentes que parecem semelhantes, mas **não são** uma CYD. O objetivo não é excluir ninguém, mas há tantos tipos e tamanhos diferentes de tela que seria extremamente difícil e confuso oferecer suporte a todos eles.

Você pode verificar se tem a placa correta conferindo o número na parte traseira da tela.

![imagem](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/assets/1562562/d23bf84f-f34b-4814-b609-87c359d6334e)

## Minha CYD tem duas portas USB

A CYD original tem apenas uma porta micro USB, mas existe um dispositivo também identificado como _ESP32-2432S028_ que tem duas portas USB: uma micro USB e uma USB-C.

Ter uma porta USB adicional seria um problema pequeno se essa fosse a única diferença, mas, infelizmente, a tela também funciona de forma diferente: as cores aparecem invertidas.

Isso pode ser corrigido de algumas maneiras:

- Use platformio - todos os exemplos no Github foram atualizados para serem usados com platformio; basta selecionar CYD ou CYD2USB para que funcionem
- Use o arquivo [User_setup.h específico para CYD2USB](/DisplayConfig/CYD2USB/) disponível no repositório; assim, você pode usar todos os exemplos normalmente
- Inverta a tela no código usando o método `tft.invertDisplay(1);`

### A porta USB-C não funciona

A porta USB-C tem uma falha: ela não possui os resistores nas linhas CC. Isso significa que ela não funcionará com cabos USB-C para USB-C. Se seu computador tiver apenas portas USB-C, você poderá usá-la por meio de um adaptador USB-C para USB-A.

### A tela não parece ter a mesma qualidade

Parece haver um problema de gamma no CYD2USB (eu nem sei o que é gamma).

Adicionar o trecho abaixo ao código parece ajudar:

```
tft.writecommand(ILI9341_GAMMASET); //Gamma curve selected
tft.writedata(2);
delay(120);
tft.writecommand(ILI9341_GAMMASET); //Gamma curve selected
tft.writedata(1);
```




