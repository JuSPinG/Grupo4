Grupo 4: [Enlace](https://docs.google.com/document/d/12CV2rnxYfPUkDMcCPOiK4URTfEbsgb3yttorbd1dQrA/edit?tab=t.0) 

[Presentación](https://docs.google.com/presentation/d/1EbDBI2oBEWcwJtFExGCpWelJCKclIOTwDr_WcXz8SRI/edit?usp=sharing)

# Índice

- _Mobile malware_.
- _Spyware_.
- _Keylogger_.
- _Cryptojacking_.
- Técnicas de ataque.
- Bibliografía.
- Definición
- Técnicas de ataque
- Posibles consecuencias
- Algún caso real de la amenaza (hablar sobre una noticia referente a la amenaza que os ha tocado)

# _Mobile malware_

El  Mobile malwars es unsoftware malicioso diseñado para infiltrarse en dispositivos móviles, robar información personal (contraseñas, datos bancarios) o causar daños, como descargar aplicaciones no deseadas, enviar SMS costosos o mostrar anuncios intrusivos.

## Posibles consecuencias del mobile malware:

- Robo de credenciales: Los atacantes pueden acceder a información sensible, como contraseñas bancarias y de correo electrónico.
- Exposición de datos personales: Puede robar información como su número de teléfono, dirección de correo electrónico y lista de contactos.
- Uso de los contactos: La información de contacto puede ser utilizada para enviar enlaces maliciosos o más malware a sus conocidos. 

## Caso real de la amenaza: 

### Así es Rogue, el troyano más poderoso del mundo

El texto explica el troyano Rogue, un MRAT (Remote Access Trojan para móviles) descubierto por Check Point Research que afecta principalmente a dispositivos Android. Rogue llega oculto dentro de aplicaciones infectadas (fuera o dentro de tiendas no fiables), pide permisos aparentemente normales y luego oculta su icono; si el usuario intenta revocar permisos, muestra mensajes intimidatorios para evitarlo.

Con esos permisos el troyano puede controlar el teléfono por completo: acceder a fotos, contactos, ubicación, mensajes; usar cámara y micrófono para grabar en secreto; hacer capturas de pantalla; eliminar apps; leer bases de datos como la de WhatsApp; bloquear números; y almacenar notificaciones (usa Firebase para clasificar notificaciones de WhatsApp, Facebook, Instagram, etc.). Según los investigadores, podría haber cientos de miles de dispositivos afectados y estaría desarrollado por grupos conocidos en malware Android.

Recomendaciones que da el artículo: no instalar aplicaciones de fuentes dudosas, eliminar rápidamente cualquier app sospechosa, instalar un antivirus fiable y hacer revisiones periódicas del teléfono.

[Noticia](https://www.elconfidencial.com/tecnologia/2021-01-15/rogue-virus-telefono-movil-que-es-malware-android_2908699/)

# _Spyware_

Un _spyware_ es un tipo de _malware_ que se encarga de espiar al cliente. Normalmente, los datos se extraen para venderlos, usarlos, o para extorsionar al atacado. Imagínate que te llega al número de teléfono unas fotos tuyas comprometidas, o que alguien adquiere tus credenciales bancarias, o que descubren todo lo que buscas en Internet.

Normalmente, los _spyware_ son muy insidiosos en ese sentido, es difícil darte cuenta que te están espiando. Por ejemplo, tengo un amigo que es espiado por su móvil constantemente. Siempre hacemos la misma prueba, habla de un tema muy específico, coge su móvil, accede a Instagram, y le salen cosas relacionadas con ese mismo tema.

Cada dato que se maneja es susceptible de ser recogido, procesado y usado.

## Posibles consecuencias del spyware:

- Registro de tus hábitos: Rastrea tu navegación para enviarte anuncios personalizados, empleando cookies de rastreo.
- Datos personales: Incluso se sabe que el spyware graba mensajes instantáneos y llamadas de Skype, secuestra tu cámara web, instala keyloggers y toma fotos y vídeos.

## Caso real de la amenaza: 

### Infección por spyware en una guardería expone datos personales de menores

Se puso en contacto a través del teléfono gratuito y confidencial 017, la Línea de Ayuda de Ciberseguridad de INCIBE, una usuaria preocupada por lo que había descubierto, tras notar que el ordenador de la guardería donde trabaja funcionaba más lento de lo habitual. 

Nos comentó que, tras este indicio, también había descubierto que se añadía la extensión trackid=sp-006 en todas las búsquedas que realizaba, en el historial de navegación y al final de todas las URL.

Además, en sus búsquedas se indexaban resultados que ella no recordaba haber buscado, en su gran mayoría sitios con dominios no españoles.

Al realizar una búsqueda en Internet de esta extensión, descubrió que era una particularidad de una infección por un malware, en concreto el virus TrackID=sp-006, un secuestrador de navegador que mantiene un registro de la actividad de navegación, las entradas de las búsquedas y las pulsaciones del teclado y altera las webs que muestra, siendo estas páginas y los resultados de las búsquedas en alemán.

[Noticia](https://www.incibe.es/linea-de-ayuda-en-ciberseguridad/casos-reales/infeccion-por-spyware-en-una-guarderia-expone-datos-personales-de-menores)

# _Keylogger_

El _keylogger_ es un tipo de _spyware_ encargado de la recopilación de datos, de uno muy concreto: la entrada del teclado. Cada tecla pulsada es enviada al atacante, en algunos casos, la información es recopilada y por último enviada cuando el equipo se apaga. La secuencia de instrucciones es la siguiente:

1. Se encinde el equipo.
    1. El sistema operativo enciende los procesos no esenciales especificados por el usuario, en esta lista se encuentra el _spyware_.
2. Cada tecla es registrada dentro de un archivo de texto o en la propia RAM, o por otro lado puede ser enviada por Internet al atacante. Los carácteres especiales como el salto de línea, `pageup` o `home` son normalmente contempladas por el atacante, y tratadas correctamente.
3. En el caso de que la información se esté guardando en el equipo infectado, cuando este se apague, en su secuencia, se le añadirá una secuencia extra en el que mandará toda la información por Internet^[[Creación de un Keylogger y su Aplicación en Amenazas](https://oa.upm.es/82649/1/TFG_ADRIAN_ESTEBAN_SANTOS.pdf)].

## Posibles consecuencias del keylogger:

- Suplantación de identidad y fraude: Al sacar la contraseña de los usuarios los ciberdelincuentes pueden iniciar sesion en las cuentas de los usuarios pasandose por ellos. 
- Pérdidas económicas: En la mayoria de secuestros de contraseñas y con ello la perdida de las cuentas de los usuarios, los ciberdelincuentes piden algun intercambio económico para la devolución de la cuenta. 
- Acceso a sistemas corporativos: Los ciberdelincuentes que practican el keylogger se centran sobre todo en corporaciones medianas-grandes, las cuales tienen mucho que perder al quitarles algun acceso a algun servicion de estas. Consiguiendo asi una recompensa economica mayor. 

## Caso real de la amenaza: 

### Un estudiante irá preso por vender un keylogger que infectó a 16.000 personas

Zachary Shames, un estudiante universitario de 21 años, se declaró culpable de haber desarrollado un software malicioso bajo la categoría de keylogger, que luego comercializó para que sus clientes pudieran robar información sensible como contraseñas y credenciales bancarias. Logró venderlo a 3 mil personas que lo usaron para infectar más de 16.000 computadoras, y es por eso que el viernes pasado aceptó los cargos de ayuda e incitación a intrusiones informáticas.

Shames desarrolló las versiones iniciales del keylogger mientras asistía a la escuela secundaria. Luego continuó modificándolo y comenzó a venderlo en forma ilegal desde su dormitorio en la universidad James Madison University, hasta que la policía llegó con una orden de allanamiento en marzo de 2016.

Según documentos judiciales que publicó The Register, Shames vendía su keylogger vía PayPal a 25 dólares, aunque algunos agentes del FBI lo encontraron en el mercado underground por 40 dólares o menos. Además de robar credenciales y registrar las pulsaciones del teclado de sus víctimas, las reenviaba a un sitio web llamado limitlessproducts.org, que daba nombre al producto.

También trataba de cifrarse para esconderse de los antivirus, ofuscando el código de manera que no coincida con una detección; las instrucciones para usarlo y cifrarlo se proporcionaban en videos que los investigadores encontraron en YouTube.

Pero Shames registró el dominio del sitio web con su nombre, dirección y correo electrónico reales; también usó el mismo mail para concretar ventas desde una cuenta de PayPal que llevaba su nombre y para responder consultas de soporte. Naturalmente, estos datos ayudaron al FBI a dar con él.

[Noticia](https://www.welivesecurity.com/la-es/2017/01/16/preso-crear-vender-un-keylogger/)

# _Cryptojacking_

El cryptojacking es una amenaza en línea que se oculta en una computadora o dispositivo móvil y utiliza los recursos de la máquina para "minar" formas de moneda en línea conocidas como criptomonedas. Los criptomineros maliciosos a menudo llegan a través de descargas del navegador web o aplicaciones móviles de origen dudoso. El cryptojacking puede comprometer todo tipo de dispositivos, incluidos escritorios, laptops, smartphones e incluso servidores de red.

## Técnicas de ataque

Las técnicas de ataque son comunes, y similares, a todos los _malware_ que hemos tratado. Se trata de lo mismo: atacar a un grupo de objetivos, obtener acceso a los equipos, en muchos casos, obtener permisos y realizar el hackeo propiamente dicho.

Una de las técnicas más usadas hoy en día consiste en el _phising_ y la "ingeniería social", pues actualmente los sistemas operativos son lo suficientemente seguros para que sea complicado acceder remotamente. Sino, siempre será efectivo acercarse a la máquina física que hay que infectar, o encontrar un fallo en el sistema o un "0d" para poder hacer el ataque.

## Posibles consecuencias del cryptojacking:

- Consumo de recursos: La empresa acabará experimentando un tremendo aumento de la factura energética, ya que el cryptojacking exprimirá cada equipo y recurrirá a él siempre que pueda.
- Problemas técnicos: Los ordenadores normales no están preparados para funcionar mientras minan criptomonedas. 
- Ciberseguridad empresarial: Que los ciberdelincuentes entran en los ordenadores de una compañía supone una grave brecha en la ciberseguridad de la misma.

## Caso real de la amenaza: 

### Una campaña de cryptojacking afecta a más de 200.000 routers MikroTik

Fecha de publicación 10/08/2018

Un grupo de investigadores de SpiderLabs ha encontrado una nueva botnet formada por más de 200.000 routers MikroTik.
 
Inyecta una serie de scripts para minar criptomonedas utilizando los dispositivos de los usuarios conectados a estos routers.

[Noticia](https://www.incibe.es/incibe-cert/publicaciones/bitacora-de-seguridad/campana-cryptojacking-afecta-mas-200000-routers-mikrotik)

# Bibliografía

https://www.pandasecurity.com/es/security-info/cryptojacking/

https://www.kaspersky.es/resource-center/threats/malware-damage

https://www.incibe.es/aprendeciberseguridad/cryptojacking

https://www.checkpoint.com/es/cyber-hub/threat-prevention/what-is-malware/mobile-malware/