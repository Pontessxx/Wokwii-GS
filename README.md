# Projeto de Monitoramento e Controle de Ambiente com ESP32 e MQTT
https://youtu.be/-sYkNRkb33Q - link do vídeo</br>
Este projeto utiliza um microcontrolador ESP32 para monitorar e controlar o ambiente, incluindo a leitura de temperatura, umidade, luminosidade, além de permitir o controle remoto de um dispositivo conectado.

Problema de Saúde Abordado

Este projeto foi implementado para a fototerapia, com o sistema iot podemos utilizar protocolos MQTT para realizar graficos visto o tempo e a temperatura do ambiente onde o bebe necessitou o tratamento, futuramente é possivel implementar um machine learning para aprender e otimizar a fototerapia para cada bebe.

**Solução Proposta**

O ESP32 é utilizado para coletar dados de sensores DHT22 (temperatura e umidade) e um LDR (sensor de luminosidade). Os dados são publicados em tópicos MQTT para permitir o monitoramento remoto. Além disso, o projeto inclui a capacidade de controlar um dispositivo (como um LED) remotamente via MQTT.

O código também incorpora um display LCD I2C para exibir informações locais e indicar visualmente o estado do ambiente.

**Configuração e Execução**

1. **Configuração do Ambiente:**
   - Certifique-se de ter o Arduino IDE instalado com suporte para ESP32.
   - Instale as bibliotecas necessárias (WiFi, PubSubClient, DHT, LiquidCrystal_I2C).

2. **Configuração do MQTT:**
   - Substitua as constantes `SSID`, `PASSWORD`, `BROKER_MQTT`, `TOPICO_SUBSCRIBE`, `TOPICO_PUBLISH`, `TOPICO_PUBLISH_2`, e `ID_MQTT` com suas configurações específicas.

3. **Configuração do Hardware:**
   - Conecte os sensores DHT22 e LDR conforme especificado no código.
   - Conecte os LEDs (ou outros dispositivos) aos pinos D32, D33 e D25.

4. **Execução:**
   - Carregue o código no ESP32 usando o Arduino IDE.
   - Abra o monitor serial para verificar as leituras dos sensores e os status de conexão MQTT.
   - Utilize um cliente MQTT para monitorar e controlar o ambiente através dos tópicos definidos.

**Simulação no Wokwi**

Você pode simular o projeto no Wokwi, uma plataforma de simulação online. [Clique aqui para acessar a simulação](https://wokwi.com/projects/381919403313250305). Certifique-se de ajustar as configurações de pinos conforme necessário na plataforma de simulação.
                                                                                                               
**Observações Importantes:**
- Certifique-se de configurar corretamente as credenciais Wi-Fi e o endereço do broker MQTT.
- Este README fornece uma visão geral básica do projeto. Consulte o código-fonte para detalhes adicionais e ajustes específicos.
- Para qualquer problema, consulte a documentação do ESP32, Arduino IDE, e outras bibliotecas utilizadas.

**Aviso:**
Este projeto é fornecido "como está" sem garantias de qualquer tipo. Certifique-se de entender e concordar com as implicações antes de implantar ou modificar o projeto.
