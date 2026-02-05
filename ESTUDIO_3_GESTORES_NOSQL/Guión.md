Grupo 4: [Enlace](https://docs.google.com/document/d/1_hbLONLLSiP2u0k_T3qtpgM3OyZ7HPfW5CRrX8S_mew/edit?tab=t.0) 

[Presentación](https://docs.google.com/presentation/d/1bwbVLl38XZ_Llg3EcCZO_HXwPh7T4uZeNeFcEHCM_IQ/edit?usp=sharing)



### 4 puntos a tener en cuenta:
Las bases de datos SQL(como MySQL o PostgreSQL) priorizan la integridad y coherencia de los datos.
Las bases de datos NoSQL (como MongoDB, Cassandra o Redis) priorizan la disponibilidad y la velocidad de crecimiento. 
Las bases de datos NoSQL son mejores cuando se necesita manejar volúmenes masivos de datos o cuando la estructura de la información es impredecible. 
Las bases de datos SQL son mejores para aplicaciones de gestión de datos con estructuras fijas y acotados (por ejemplo un inventario de una tienda local).


### Estudio de los siguientes gestores nosql
-Redis
-Cassandra
-Amazon DynamoDB

## REDIS

**Redis (Remote Dictionary Server)** no es solo una base de datos; es un almacén de estructuras de datos en memoria. Su principal característica es que reside en la RAM, lo que elimina el "cuello de botella" del disco duro.

### Características Clave:

- **Rendimiento en Microsegundos:** Mientras que otras bases de datos miden su latencia en milisegundos ($ms$), Redis lo hace en microsegundos ($\mu s$).

- **Estructuras de Datos Avanzadas:** A diferencia de un simple clave-valor (como Memcached), Redis permite usar:

    - Lists: Para colas de mensajes (LPUSH, RPOP).
    
    - Sets / Sorted Sets: Ideales para rankings de juegos o listas de amigos únicas.

    - Hashes: Para representar objetos (ej. perfiles de usuario).
    
    - Streams: Para procesamiento de eventos en tiempo real.

- **Persistencia configurable:** Aunque vive en RAM, puedes guardar datos en disco mediante RDB (snapshots periódicos) o AOF (registro de cada operación).

- **Pub/Sub nativo:** Funciona perfectamente como un broker de mensajería para aplicaciones en tiempo real (chats, notificaciones).


## CASSANDRA

Apache Cassandra es una base de datos NoSQL distribuida y orientada a columnas, diseñada para manejar grandes volúmenes de datos con alta disponibilidad y sin puntos únicos de fallo.

Características Clave:

1. Arquitectura Masterless: No existe un nodo principal; todos los nodos son iguales. Esto permite que el sistema siga funcionando aunque fallen varios nodos.
2. Escalabilidad Horizontal Lineal: Se pueden agregar nodos fácilmente al cluster para aumentar capacidad y rendimiento sin detener el sistema.
3. Consistencia Sintonizable: Permite elegir entre consistencia eventual o fuerte según la necesidad de cada operación (priorizando velocidad o precisión).
4. Optimizada para Escrituras Masivas: Ideal para sistemas donde los datos se insertan de forma continua, como logs, métricas o eventos.
5. Alta Tolerancia a Fallos: Replicación automática de datos entre nodos y, si se desea, entre distintos centros de datos.
6. Uso ideal: Big Data, análisis de logs, IoT, series temporales y aplicaciones que requieren disponibilidad constante y gran volumen de escrituras.

## AMAZON DYNAMODB

### 1. ¿Qué es Amazon DynamoDB?
Es un servicio de base de datos NoSQL de tipo clave-valor y documentos, totalmente gestionado por AWS (Amazon Web Services). Se define como Serverless, lo que significa que no tienes que gestionar servidores, parches o mantenimiento de hardware.

* Prioridad: Alta disponibilidad y escalabilidad masiva.

* Rendimiento: Latencia de milisegundos de un solo dígito (consistente incluso con peticiones masivas).

### 2. Arquitectura y Modelo de Datos
A diferencia de SQL, DynamoDB utiliza una estructura de tablas, pero sin esquemas fijos (schemaless).

* Tablas: Colección de datos.

* Items (Elementos): Equivale a una fila en SQL. Cada ítem puede tener atributos diferentes.

* Atributos: Equivale a una columna. Soporta tipos escalares (números, strings), sets y listas/mapas (JSON).

* Clave Primaria (Obligatoria):

    * Partition Key (Hash): Determina en qué partición física se guardan los datos.

    * Sort Key (Range): Permite ordenar datos que comparten la misma Partition Key (ideal para series temporales o historiales).

### 3. Características Principales

* Escalabilidad Automática (Auto-scaling): Ajusta la capacidad de lectura/escritura según el tráfico en tiempo real.

* Tablas Globales: Replicación automática entre diferentes regiones de AWS (ideal para apps con usuarios en todo el mundo).

* DynamoDB Streams: Captura cambios en los datos (inserciones, borrados) para disparar acciones automáticas (ej: enviar un email vía AWS Lambda cuando alguien se registra).

* Seguridad: Integración nativa con IAM (Identity and Access Management) para control de permisos detallado.






## Comparativa: Redis vs Cassandra vs DynamoDB

Cada una de estas bases de datos fue diseñada para resolver problemas distintos:

| **Característica** | **Redis** | **Apache Cassandra** | **Amazon DynamoDB** |
| -- | -- | -- | -- |
**Tipo de NoSQL** | Clave-Valor (en memoria) | Orientada a Columnas (Wide-column) | Clave-Valor y Documento
**Ubicación Datos** | Principalmente RAM | Disco (optimizado para escritura) | SSD (totalmente gestionado)
**Escalabilidad** | Vertical (RAM) y Cluster | "Horizontal (lineal, excelente)" | Horizontal (automática/serverless)
**Consistencia** | Alta (en un solo nodo) | Sintonizable (Eventual a Fuerte) | Eventual o Fuerte (configurable)
**Uso Ideal** | "Caché, sesiones | tiempo real" | "Big Data, logs, escritura masiva" | Apps web escalables en AWS

### Diferencias 1 contra 1:

- Redis vs. Cassandra:

Velocidad vs. Volumen: Redis es mucho más rápido para lecturas/escrituras individuales, pero Cassandra es mejor para almacenar petabytes de datos que no caben en la memoria RAM.

Arquitectura: Cassandra es "Masterless" (todos los nodos son iguales), lo que la hace ultra-resistente a fallos. Redis suele usar una arquitectura Primario-Réplica.

- Redis vs. DynamoDB:

Gestión: DynamoDB es "Serverless"; no configuras servidores, solo tablas. Redis requiere gestionar instancias (a menos que uses Redis Cloud o AWS ElastiCache).


Latencia: Redis es consistentemente más rápido (sub-milisegundo). DynamoDB suele estar en el rango de 1-10ms, a menos que le añadas DAX (que es básicamente una capa de caché tipo Redis encima de DynamoDB).

- Cassandra vs. DynamoDB:

Control: Cassandra te da control total sobre cómo se guardan los datos, pero es muy compleja de operar. DynamoDB sacrifica ese control a cambio de una operatividad casi nula para el desarrollador.

## ¿Cuándo elegir cuál?

- Eligiriamos Redis: Necesitas la latencia más baja posible, vas a manejar sesiones de usuario, rankings en vivo o necesitas un sistema de mensajes rápido.

- Eligiriamos Cassandra: Tienes una cantidad ingente de datos (Big Data) que nunca dejan de llegar (como logs de sensores o historial de transacciones) y necesitas que el sistema nunca se caiga.

- Eligiriamos DynamoDB: Estás en el ecosistema de AWS, quieres olvidarte de la administración de servidores y tu carga de trabajo fluctúa mucho (escalado automático).

- Nota técnica: En arquitecturas modernas, es muy común ver a Redis trabajando junto a Cassandra o DynamoDB. Redis actúa como la "cara rápida" (caché) y las otras como el "almacén persistente" de largo plazo.


### Requisitos:
- Se hace en clanes.
- Se pide:
- Documentación del estudio de cada uno.
- Documentación de las diferencias de cada uno.
- Eporfolio individual de cada persona.
- Exposición en clase sin leer, repartiendolo equitativamente.
- PD: Acuerdate del commit por sesión trabajada en clase y casa. 
- (DIA/HORA PRESENTACIÓN …)

