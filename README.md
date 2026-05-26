# ESP32-Cheap-Yellow-Display

Existe um ESP32 com uma tela LCD integrada de 320 x 240, 2,8", sensível ao toque, chamado "ESP32-2432S028R". Como esse nome não é nada fácil de pronunciar, proponho renomeá-lo para "Cheap Yellow Display", ou CYD, de forma abreviada. Essa tela custa apenas cerca de US$ 15 com entrega, então acredito que ofereça um excelente custo-benefício.

## Recursos

O CYD tem os seguintes recursos:

- ESP32 (com Wi-Fi e Bluetooth)
- Tela LCD de 320 x 240 (2,8")
- Tela sensível ao toque (resistiva)
- USB para alimentação e programação
- Slot para cartão SD, LED e alguns pinos adicionais disponíveis

## Para quem ele é indicado?

Acredito que seja útil para os seguintes tipos de pessoas:

- **Pessoas que estão começando a trabalhar com hardware** - como tudo já está conectado, não é necessário soldar nem usar componentes adicionais
- **Pessoas familiarizadas com hardware, mas que têm preguiça** - (como eu) às vezes você só quer montar um projeto sem precisar montar nenhum componente de hardware
- **Pessoas que não estão exatamente procurando aprender algo, mas querem montar coisas interessantes** - mais sobre isso adiante.

## Qual é o objetivo desta página?

Este é um hardware bastante interessante por um preço baixo, mas as instruções e o suporte de software disponíveis para ele são muito limitados: há apenas um link para um arquivo zip em um site aleatório.

Há alguns anos, lancei o [ESP32 Trinity](https://github.com/witnessmenow/ESP32-Trinity), uma placa ESP32 de código aberto para controlar painéis de matriz. Acredito que o principal benefício que as pessoas obtêm do trabalho que fiz no Trinity não seja o hardware, mas a documentação, os códigos de exemplo e os projetos prontos para uso.

Não crio mais produtos de hardware, mas acho que seria interessante se pudéssemos criar o mesmo tipo de comunidade em torno desta tela, na qual as pessoas possam compartilhar exemplos e projetos feitos para ela.

## Como saber se uma tela é um CYD?
![Árvore de decisão do CYD](http://www.plantuml.com/plantuml/png/RP0nJyCm48Nt_8gZNIb3fge3LD2b2q92235UamDRE7PaNuhyxxda7DGgJBs-zxtSE-yJO-IXSzKD6-e8UeVMLyQs1DJrdA6br4JRims-4fW9LiS4bY6JS-47qBTWC052QvEayyCAvA-wS-8vi01F7mS8SVevOxJeUK9zu55QzzP_Nw-exxPmz8tHJzRRsJq4cdo3Pu98oIQsCd4O6WDIbyXF4LN-JNMsYG7UNXyXUAUTLHDfqVeMJWClUfSPrY_OOyPtO_ivUPcfnoMV3iyXJh4cj_MGJd8lEleQkvQKi9TYUT_DvbukXnraIfTQURMT39Nu8kcrXInIwQYO-gCyNwgm6al-ZneTNIRqjLokqS2UV3jqxXS0)

## Onde comprar?

Compre onde for mais barato para você:

- [Aliexpress\*](https://s.click.aliexpress.com/e/_DkSpIjB)
- [Aliexpress\*](https://s.click.aliexpress.com/e/_DkcmuCh)
- [Aliexpress](https://www.aliexpress.com/item/1005004502250619.html)
- [Makerfabs](https://www.makerfabs.com/sunton-esp32-2-8-inch-tft-with-touch.html) - Parece incluir um cartão SD de 16 GB. A Makerfabs também vende meu [ESP32 Trinity](https://github.com/witnessmenow/ESP32-Trinity) (OBSERVAÇÃO: haverá cobrança de imposto de importação na UE para compras da Makerfabs)

\* = Link de afiliado

## Primeiros passos com seu CYD

Para obter detalhes sobre como começar a usar seu CYD, consulte a página de [instalação e configuração](/SETUP.md).

## Exemplos de código

### Conceitos básicos

Há uma biblioteca com exemplos que demonstram como usar os diferentes recursos do CYD. Este é um bom lugar para começar. [Confira aqui.](/Examples/Basics)

### Bibliotecas de tela alternativas

Os exemplos básicos são baseados na biblioteca de tela TFT_eSPI, mas o CYD também funciona com outras bibliotecas de tela. Aqui estão alguns códigos de exemplo caso você prefira usar uma biblioteca Arduino alternativa. [Confira aqui.](/Examples/AlternativeLibraries)

### ESPHome

Alguns exemplos de uso do CYD no ESPHome. [Confira aqui.](/Examples/ESPHome)

## Informações e links adicionais

### Discord

Participe da discussão sobre o CYD no [meu canal do Discord](https://discord.gg/nnezpvq).

### Impressão 3D

Alguns exemplos de suportes e gabinetes impressos em 3D. [Confira aqui.](/3dModels)

### Informações sobre pinos

[Esta página](/PINS.md) contém informações sobre onde cada pino é usado e quais estão livres para utilização.

### Complementos

[Esta página](/ADDONS.md) contém informações sobre complementos de hardware que podem adicionar funcionalidades ao seu CYD.

### Solução de problemas

[Esta página](/TROUBLESHOOTING.md) contém informações sobre como solucionar problemas do seu dispositivo CYD.

### Modificações de hardware

[Esta página](/Mods/README.md) contém informações sobre algumas modificações de hardware que podem ser feitas no CYD para melhorar ou alterar parte de suas funcionalidades.

### Menções na mídia e em vídeos

[Esta página](/MEDIA.md) lista todas as ocasiões em que o projeto CYD foi mencionado em algum lugar!

## Informações da licença

Este projeto está licenciado sob a licença MIT, conforme o [arquivo de licença](/LICENSE).

A única exceção é a pasta [OriginalDocumentation](/OriginalDocumentation/), para a qual não tenho o direito de conceder licença.

## Outros idiomas

Alguns membros da comunidade adaptaram parte destas informações para outros idiomas!

Observe que não posso garantir a precisão das traduções, o quanto estão atualizadas nem seu conteúdo em geral.

- [French / Française](https://github.com/usini/ESP32-Cheap-Yellow-Display-Documentation-FR)
- [German / Deutsch](https://github.com/paelzer/ESP32-Cheap-Yellow-Display-Documentation-DE)
- [Portuguese / Português](https://github.com/paelzer/ESP32-Cheap-Yellow-Display-Documentation-Pt-BR)

Caso queira contribuir com uma tradução, inclua o nome ou o código do idioma no nome do repositório; assim, você poderá adicionar um link para ele aqui.

## Ajude a apoiar meu trabalho!

[Caso goste do meu trabalho, considere tornar-se um patrocinador no GitHub!](https://github.com/sponsors/witnessmenow/)
