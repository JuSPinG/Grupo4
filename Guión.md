Grupo 4: [Enlace](https://docs.google.com/document/d/12CV2rnxYfPUkDMcCPOiK4URTfEbsgb3yttorbd1dQrA/edit?tab=t.0).

# Índice

- _Mobile malware_.
- _Spyware_.
- _Keylogger_.
- _Cryptojacking_.
- Técnicas de ataque.
- Bibliografía.

# _Mobile malware_

El  Mobile malwars es unsoftware malicioso diseñado para infiltrarse en dispositivos móviles, robar información personal (contraseñas, datos bancarios) o causar daños, como descargar aplicaciones no deseadas, enviar SMS costosos o mostrar anuncios intrusivos.





# _Spyware_

Un _spyware_ es un tipo de _malware_ que se encarga de espiar al cliente. Normalmente, los datos se extraen para venderlos, usarlos, o para extorsionar al atacado. Imagínate que te llega al número de teléfono unas fotos tuyas comprometidas, o que alguien adquiere tus credenciales bancarias, o que descubren todo lo que buscas en Internet.

Normalmente, los _spyware_ son muy insidiosos en ese sentido, es difícil darte cuenta que te están espiando. Por ejemplo, tengo un amigo que es espiado por su móvil constantemente. Siempre hacemos la misma prueba, habla de un tema muy específico, coge su móvil, accede a Instagram, y le salen cosas relacionadas con ese mismo tema.

Cada dato que se maneja es susceptible de ser recogido, procesado y usado.

# _Keylogger_

El _keylogger_ es un tipo de _spyware_ encargado de la recopilación de datos, de uno muy concreto: la entrada del teclado. Cada tecla pulsada es enviada al atacante, en algunos casos, la información es recopilada y por último enviada cuando el equipo se apaga. La secuencia de instrucciones es la siguiente:

1. Se encinde el equipo.
    1. El sistema operativo enciende los procesos no esenciales especificados por el usuario, en esta lista se encuentra el _spyware_.
2. Cada tecla es registrada dentro de un archivo de texto o en la propia RAM, o por otro lado puede ser enviada por Internet al atacante. Los carácteres especiales como el salto de línea, `pageup` o `home` son normalmente contempladas por el atacante, y tratadas correctamente.
3. En el caso de que la información se esté guardando en el equipo infectado, cuando este se apague, en su secuencia, se le añadirá una secuencia extra en el que mandará toda la información por Internet^[[Creación de un Keylogger y su Aplicación en Amenazas](https://oa.upm.es/82649/1/TFG_ADRIAN_ESTEBAN_SANTOS.pdf)].

Posibles consecuencias del keylogger:

- Suplantación de identidad y fraude
- Pérdidas económicas
- Acceso a sistemas corporativos

# _Cryptojacking_

El cryptojacking es una amenaza en línea que se oculta en una computadora o dispositivo móvil y utiliza los recursos de la máquina para "minar" formas de moneda en línea conocidas como criptomonedas. Los criptomineros maliciosos a menudo llegan a través de descargas del navegador web o aplicaciones móviles de origen dudoso. El cryptojacking puede comprometer todo tipo de dispositivos, incluidos escritorios, laptops, smartphones e incluso servidores de red.






# Técnicas de ataque

Las técnicas de ataque son comunes, y similares, a todos los _malware_ que hemos tratado. Se trata de lo mismo: atacar a un grupo de objetivos, obtener acceso a los equipos, en muchos casos, obtener permisos y realizar el hackeo propiamente dicho.

Una de las técnicas más usadas hoy en día consiste en el _phising_ y la "ingeniería social", pues actualmente los sistemas operativos son lo suficientemente seguros para que sea complicado acceder remotamente 



# Bibliografía