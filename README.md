# PCOM-WiFi-Bluetooth-ESP32---Portuguese

Conexão Automática entre WiFi e Bluetooth no ESP32 para Arduino.

Funcionalidades básicas do PCOM WiFi-Bluetooth:

O PCOM WiFi/Bluetooh é um mecanismo que gerencia as conexões WiFi e Bluetooth para um código do usuário executando em uma placa ESP32 na Plataforma Arduino. Este gerenciamento disponibiliza uma interface para o código do usuário, que é capaz das seguintes funcionalidades:

	1) Gerenciar automaticamente a conexão do ESP32 à rede WiFi especificada, e mesmo que esta rede caia ou fique temporariamente indisponível, o PCOM será capaz de reconectar assim que a rede especificada estiver novamente ao alcance.

	2) Instanciar um WiFi Server, para que este sirva como elemento de comunicação entre o código do usuário e um Cliente WiFi. As funcionalidades da comunicação são as mesmas existentes no WiFi convencional do ESP32 para a Plataforma Arduino.

	3) Disponibilizar um Mecanismo de Gerenciamento da Comunicação com o Cliente WiFi, funcionando com uma Interface entre ambos, simplificando e padronizando a forma de acesso no código. Este mecanismo pode ser utilizado para gerenciar inúmeras Páginas HTML (normalmente em uma comunicação com um Navegador de Internet), ou então utilizando qualquer protocolo sobre o TCP/IP (seja um protocolo padrão ou dedicado). Um mecanismo de Timeout simples também está implementado, para o caso do Cliente WiFi parar de responder e não completar uma requisição em andamento.

	4) Gerenciar automaticamente a conexão do ESP32 a um Cliente Bluetooth “Classic”, quando o WiFi não estiver disponível, permitindo que este Cliente possa acessar as mesmas funcionalidades implementadas no Sistema da placa ESP32 que podem ser acessadas através do WiFi.

	5) Instanciar uma Interface Bluetooth SPP (Serial Port Profile), para ser utilizada como meio de comunicação entre o Cliente Bluetooth e o código executando no Arduino/ESP32.

	6) Gerenciar um Mecanismo de Autenticação para o Cliente Bluetooth, mantendo uma Lista de Clientes Autenticados. A Lista é não-volátil, sendo armazenada na EEPROM do ESP32.

As funcionalidades listadas são as básicas, e poderão ser ampliadas em revisões da implementação do PCOM WiFi/Bluetooth.

Não há obrigatoriedade em se usar ambos os PCOMs WiFi e Bluetooth. O código do Arduino pode sistematicamente habilitar/desabilitar um ou outro PCOM (ou ambos), a qualquer momento. O default é ambos habilitados, mas caso se use apenas um dos PCOMs, nenhuma ação é necessária, já que o Mecanismo de conexão é automático e utilizará a conexão que estiver disponível e ao alcance.


Link para o contexto:   http://labdegaragem.com/forum/topics/implementa-o-do-pcom-wifi-bluetooth-esp32-para-arduino

