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