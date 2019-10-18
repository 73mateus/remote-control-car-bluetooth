# remote-control-car-bluetooth


Remote control car Bluetooth

Como o nome sugere, o projeto se trata de um carrinho de controle remoto, controlado pelo smatphone.

O carrinho terá duas rodas ativas e uma roda boba de apoio.
A comunicação entre o smartphone e o carrinho acontecerá via Bluetooth.
Para isso, será utilizado um módulo Bluetooth. Esse módulo recebrá os comandos do usuário e enviará para o Cortex-M0. Este por sua vez, processará a informação binária e enviará um código de 4 bits, através de suas potas de saídas para o driver dos motores (L298N) dos carrinhos.

O L298N receberá 4 bits (2 para cada motor). O funcionamento dos motores dependerá do código enviado. Por exemplo se o código enviado ao driver for 0101, as duas rodas andarão para frente, e o carrinho segue adiante. Se o comando enviado for 0111, Uma das rodas irá travar e a outra rodará nomalmente, fazendo o carrinho dobrar para um dos lados.

O principio por traz do L298N é a ponte H. Este tópico será explicado posteriormente.
