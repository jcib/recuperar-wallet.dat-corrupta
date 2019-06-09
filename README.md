# Corrupted wallet.dat FIX
Pasos para recuperar las claves privadas de la billetera de cualquier criptodivisa.

Si nos vemos en una situación parecida a la siguiente:

<img src="https://i.ibb.co/TPYrKgK/corrupt-wallet.png">

Significa que el cliente no puede abrir el fichero que contiene las claves privadas. Necesitamos un editor de textos en hexadecimal. Recomiendo wxHexEditor.

**Pasos para _recuperar_ las claves**:

1. Descarga el editor de textos en hexadecimal.

2. Haz una copia de tu "wallet.dat" en algún lugar seguro.

3. Ejecuta el editor. Abre la "wallet.dat" corrompida.

<img src="https://i.ibb.co/2v0Rm0z/1.png">

4. Dale a "Control + F" y busca los siguientes números: 0201010420. Dale a "Buscar todas". A mí me han aparecido 90.

<img src="https://i.ibb.co/RPzqNSC/2.png">

Las 32 parejas de bytes que hay después de esta secuencia de números son tus claves privadas.

5. Ahora viene el trabajo manual. Copia los 64 bytes que siguen a la secuencia "0201010420" (no incluida). Por ejemplo, una de mis claves privadas sería esta:

<img src="https://i.ibb.co/MR2TDZp/3.png">

6. Abre un Excel y ve copiando una a una todas las secuencias de 64 bytes en celdas distintas. Una debajo de otra preferiblemente.

<img src="https://i.ibb.co/SXcD8rg/4.png" height="128" width="128">

7. Cuando estén todas copiadas. Dale a "Control + H" (Control + F en Open Calc) y junta todos los espacios. Esto se hace poniendo un espacio en la barra de "Buscar" y dándole a "Reemplazar todo". Quedará así:

<img src="https://i.ibb.co/sgyJpmh/5.png">

8. Por cada secuencia de bytes tienes que ir a https://walletgenerator.net/. En "Elige criptodivisa" escoge la cripto deseada. Dale a "Skip" --> "Detalles de la cartera". En el recuadro blanco de "Introduce la clave privada" poned la secuencia de bytes. Dadle a "View details".

<img src="https://i.ibb.co/gWXtJdg/6.png">

9. Ya tienes tu clave privada. Impórtala y repite el proceso hasta dar con la que *contiene* vuestras monedas.







