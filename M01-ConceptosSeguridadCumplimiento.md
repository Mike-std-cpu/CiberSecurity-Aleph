# 🚀 Modulo de conceptos de seguridad y cumplimiento. 

A medida que se obtiene acceso a más datos empresariales desde ubicaciones fuera de la red corporativa tradicional, la seguridad y el cumplimiento se han convertido en **preocupaciones importantes**. Las organizaciones deben comprender cómo pueden **proteger** mejor sus datos, _independientemente de dónde se tenga acceso a ellos y de si se encuentran en la red corporativa o en la nube._ Además, las organizaciones deben asegurarse de que cumplen los **requisitos normativos** y del sector para garantizar la- protección y la privacidad de los datos.

En este modulo, podremos entender:

- Modelos de respopnsabilidad compartida.
- Defensa en profundidad.
- Confianza Cero (Zero Trust).
- Conceptos de cifrado (Hash).

## Modelo de responsabilidad compartida.

Comenzaremos sabiendo que existen organizaciones que solo ejecutan **hardware y software local**, la organización es un 100 % responsable de la implementación de la seguridad y el cumplimiento. Con los servicios basados en la nube, esa responsabilidad se comparte entre el cliente y el proveedor de la nube.

**El modelo de responsabilidad compartida** _identifica qué tareas de seguridad administra el proveedor de la nube y qué tareas de seguridad administra usted como cliente._ Igualmente, las responsabilidades varían en función de dónde se hospede la carga de trabajo:

- Software como servicio (SaaS).
- Plataforma como servicio (PaaS).
- Infraestructura como servicio (IaaS).
- Centro de datos local.

> El modelo de responsabilidad compartida hace que las responsabilidades resulten claras. Cuando las organizaciones realizan migraciones a la nube, algunas responsabilidades se transfieren al proveedor de la nube y otras a la organización del cliente.

Acontinuacion, podremos visualziar las responsabiliades que cada agente puede tener dependiendo su funcionalidad
![Responsabilidades](https://docs.microsoft.com/es-mx/learn/wwl-sci/describe-security-concepts-methodologies/media/3-shared-responsibility-model.png)

---

- Centro de datos Locales: _Aqui es responsabilidad directa de uno mismo, tanto la seguridad fisica y el cifrado de la informaciòn confidencial que se maneje._

- Infraestructura como servicio (IaaS): En IaaS requiere que el cliente en la nube se encargue casi totalmente de la administración, aqui el cliente de la nube no es responsable de el hardware, sino del software (SO, controle de red, redes y protección de los datos.)

- Plataforma como Servicio (PaaS): PaaS proporciona un entorno para compilar, probar e implementar aplicaciones de software. Es de facil uso de la costruccion y administracuon de la aplicación.

> Responsabilidades:
> **Proveedor:** Hardware y Sistemas operativos
> **Cliente:** Aplicacion y sus datos.

- Software como Servicio (SaaS): El proveedor en la nube se encarga de hospedar y administrar SaaS para el cliente. Normalmente, esto se licencia a través de una suscripción mensual o anual. Microsoft 365, Skype y Dynamics CRM Online son ejemplos del software de SaaS.

> Responsabilidades:
> **Proveedor:** Hospedaje y administración Saas para el cliente, casi todo en excepción de los datos, identidades y recursos locales
> **Cliente:** Administración de los datos, identidades y recursos locales

---

> En cuanto a todos los tipos de implementación en la nube, usted es el propietario de sus datos e identidades como cliente de la nube. Asimismo, es responsable de proteger la seguridad de los datos, las identidades y los recursos locales.
> - La informacion y los datos.
> - Los dispositivosd ya sean moviles o locales.
> - Cuentas e identidades
> La ventaja del modelo de responsabilidad compartida es que las organizaciones tienen claras sus responsabilidades y las del proveedor de la nube.

---

## Descripcion de la defensa en profundiad.

La defensa en profundidad usa un enfoque por **capas** para la seguridad, en lugar de depender de un solo perímetro. **Una estrategia de defensa en profundidad usa una serie de mecanismos para ralentizar el avance de un ataque.** Cada capa proporciona protección de modo que, si se infringe una de ellas, una capa posterior impedirá que un atacante obtenga acceso no autorizado a los datos.

### Niveles de Seguridad:

- **La seguridad física**, como limitar el acceso a un centro de datos solo al personal autorizado.
Controles de seguridad de identidad y acceso, como la autenticación multifactor o el acceso basado en condiciones, para controlar el acceso a la infraestructura y el control de cambios.

- **La seguridad perimetral** de la red corporativa incluye la protección frente a ataques de denegación de servicio distribuido (DDoS) para filtrar los ataques a gran escala antes de que puedan causar una denegación de servicio para los usuarios.

> DDoS : Es un ataque a un sistema de computadoras o red que **causa que un servicio o recurso sea inaccesible a los usuarios legítimos.** ​Es decir, una vez que una página web es atacada por este medio deja de poder acceder a sus propios datos hasta que es capaz de parar la intrusión. Para lograrlo el atacante satura el servidor en el que se aloja la página o alguno de sus servicios haciendo que dicho servidor no pueda funcionar correctamente.

- **Seguridad de red**, como la segmentación de red y los controles de acceso a la red, para limitar la comunicación entre los recursos.

- **Seguridad de capa de proceso**, como la protección del acceso a las máquinas virtuales, ya sea de forma local o en la nube, cerrando determinados puertos.

- **Seguridad de capa de aplicación**, que garantiza que las aplicaciones sean seguras y estén libres de vulnerabilidades de seguridad.

- **Seguridad de capa de datos** que incluye controles para administrar el acceso a los datos empresariales y de clientes, y el cifrado para proteger los datos.

![Capas](https://docs.microsoft.com/es-mx/learn/wwl-sci/describe-security-concepts-methodologies/media/4-defense-depth.png)

---

## CIA (Confidencialidad, Integridad y Disponibilidad)

Como ya hemops visto, la ciberseguridad esta con la finalidad de proteger y defender el uso correcto del **ciber Espacio** de todo tipo de ataques, y que **una estrategia de defensa en profundidad** usa una serie de mecanismos para ralentizar el avance de un ataque. Aqui entra el triangulo de la ciberseguridad.

![CIA](https://i.stack.imgur.com/nDLPC.png)

1. **La confidencialidad** se refiere a la necesidad de conservar datos confidenciales, como información de clientes, contraseñas o datos financieros. 

> Puede cifrar los datos para mantener la confidencialidad, pero también debe mantener la confidencialidad de las claves de cifrado. La confidencialidad es la parte más visible de la seguridad; gracias a ella, podemos ver claramente la necesidad de mantener la confidencialidad de los datos privados, las claves, las contraseñas y otros secretos.

2. **La integridad** indica la necesidad de mantener los datos o mensajes correctos. 

> Cuando envíe un mensaje de correo electrónico, probablemente quiera asegurarse de que el mensaje recibido sea el mismo que el mensaje enviado. Al almacenar datos en una base de datos, quiere asegurarse también de que los datos que recupera son los mismos que los datos almacenados. El cifrado de datos hace que este proceso sea confidencial, pero debe ser capaz de descifrarlo para obtener el mismo contenido que antes del cifrado. La integridad consiste en tener la confianza de que los datos no se han alterado ni modificado.

3. **La disponibilidad** se refiere a poner los datos a disposición de los usuarios cuando los necesiten. 

> Es importante para la organización mantener seguros los datos de los clientes, pero al mismo tiempo también debe estar disponible para los empleados que trabajan con los clientes. Aunque puede ser más seguro almacenar los datos en un formato cifrado, los empleados necesitan obtener acceso a los datos descifrados.
