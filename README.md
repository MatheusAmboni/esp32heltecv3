# esp32heltecv3
Documentação para instalação e usar o Dispositivo Lora Heltec V3

Certifique de instalar os drivers apropriados:
https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads

O problema de instalação desta placa é que não é o método mais convencional e várias pessoas tiveram problema pra instalar a placa
Ex:
https://github.com/HelTecAutomation/Heltec_ESP32/issues/106

Tudo começa com esse Link de Quick Start que indica certinho o que deve fazer:

https://docs.heltec.org/en/node/esp32/esp32_general_docs/quick_start.html

O problema é que você deve fazer o link de instalação não com o disponibilizado no tutorial mas sim este aqui:

Instale em File -> preferences -> Additional Board Manager URLs
https://github.com/Heltec-Aaron-Lee/WiFi_Kit_series/releases/download/0.0.7/package_heltec_esp32_index.json

Depois vá em Tools --> Board --> Boards Manager, procure Heltec Esp32 até aparecer na lista a opção:
Heltec ESP32 Series Dev-boards
NESTE CASO INSTALE A VERSÃO 0.0.7

--------------------
Outra opção é utilizar via download do pacote ( o que pode demorar um pouco ). 
https://resource.heltec.cn/download/tools/WiFi_Kit_series.zip
Faça download deste arquivo e crie uma pasta chamada Hardware dentro da pasta Arduino. 
Extraia o arquivo baixado no link nesta pasta hardware
Restarte o Arduino IDE pra ver se a instalação está correta

--------------------
Uma informação muito importante é que você não deve utilizar os exemplos em Examples -> Heltec Esp32 Dev-boards
pois eles estão quebrados e não funcionam na placa Heltec V3
Aqui a jogada é utilizar o exemplo em Heltec-example
![image](https://github.com/MatheusAmboni/esp32heltecv3/assets/61568032/ffcdb8b8-b29a-449c-8977-864e627e85d0)
Neste caso utilize o exemplo em Examples -> FactoryTest -> WiFi_LoRa_32_V3_FactoryTest 

--------------------
Utilize a placa WiFi Lora 32 (V3) / Wireless shell (v3) / Wireless Stick Lite V3

--------------------
Não utilize um cabo USB A para USB C pois não terá energia suficiente para alimentar a placa

--------------------
Outra coisa importante é que você tem que ir na pasta do seu computador: 
C:Users/seu_nome/AppData/Local/Arduino15/packages/Heltec-esp32/hardware/esp32/0.0.7/libraries/Heltec-Example/src
Onde terá um arquivo heltec.h
Este arquivo está quebrado, você deve instalar o novo arquivo heltec.h e heltec.cpp neste link -> https://github.com/Heltec-Aaron-Lee/WiFi_Kit_series/files/10735664/heltec.zip

