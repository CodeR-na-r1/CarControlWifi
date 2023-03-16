Используйте Arduino и esp8266. Arduino управляет двух колесной платформой (машину состояний реализовывать не нужно, оставьте только функции управленя моторами).

1. Обеспичим питанием esp:

Подключите пин Vin esp к пину 5v Arduino; соедините пины G (Gnd) двух плат.​

2. Сделаем подключение по Serial:

Подключите Rx, Tx плат (Rx соединияется с Tx).Подключение и код Arduino можно взять здесь код для esp должен быть на python.  Пример использования UART посмотрите здесь. Что бы не нарушать подключение по USB используйте SoftSerial.

3. Написать класс на Python для управления платформой c методами forward, backward, turn_left, turn_right, rotate_left, rotate_right, stop. Внутри методов происходит отправка по Serial (так же как мы управляли светодиодом отправляя 'u' и 'd').

4. Загрузить файл с классом на esp и проверить что он импортируется.

5. Написать код на Arduino который будет принимать символы, которые отправляет esp и вызывает соотвествующие функции управления моторами (проверить можно через Serial monitor в Arduino IDE).