# 馃殌 Modulo de conceptos de seguridad y cumplimiento. 

A medida que se obtiene acceso a m谩s datos empresariales desde ubicaciones fuera de la red corporativa tradicional, la seguridad y el cumplimiento se han convertido en **preocupaciones importantes**. Las organizaciones deben comprender c贸mo pueden **proteger** mejor sus datos, _independientemente de d贸nde se tenga acceso a ellos y de si se encuentran en la red corporativa o en la nube._ Adem谩s, las organizaciones deben asegurarse de que cumplen los **requisitos normativos** y del sector para garantizar la- protecci贸n y la privacidad de los datos.

En este modulo, podremos entender:

- Modelos de respopnsabilidad compartida.
- Defensa en profundidad.
- Confianza Cero (Zero Trust).
- Conceptos de cifrado (Hash).

## 馃憠 Modelo de responsabilidad compartida.

Comenzaremos sabiendo que existen organizaciones que solo ejecutan **hardware y software local**, la organizaci贸n es un 100 % responsable de la implementaci贸n de la seguridad y el cumplimiento. Con los servicios basados en la nube, esa responsabilidad se comparte entre el cliente y el proveedor de la nube.

**El modelo de responsabilidad compartida** _identifica qu茅 tareas de seguridad administra el proveedor de la nube y qu茅 tareas de seguridad administra usted como cliente._ Igualmente, las responsabilidades var铆an en funci贸n de d贸nde se hospede la carga de trabajo:

- Software como servicio (SaaS).
- Plataforma como servicio (PaaS).
- Infraestructura como servicio (IaaS).
- Centro de datos local.

> El modelo de responsabilidad compartida hace que las responsabilidades resulten claras. Cuando las organizaciones realizan migraciones a la nube, algunas responsabilidades se transfieren al proveedor de la nube y otras a la organizaci贸n del cliente.

Acontinuacion, podremos visualziar las responsabiliades que cada agente puede tener dependiendo su funcionalidad
![Responsabilidades](https://docs.microsoft.com/es-mx/learn/wwl-sci/describe-security-concepts-methodologies/media/3-shared-responsibility-model.png)

---

- Centro de datos Locales: _Aqui es responsabilidad directa de uno mismo, tanto la seguridad fisica y el cifrado de la informaci貌n confidencial que se maneje._

- Infraestructura como servicio (IaaS): En IaaS requiere que el cliente en la nube se encargue casi totalmente de la administraci贸n, aqui el cliente de la nube no es responsable de el hardware, sino del software (SO, controle de red, redes y protecci贸n de los datos.)

- Plataforma como Servicio (PaaS): PaaS proporciona un entorno para compilar, probar e implementar aplicaciones de software. Es de facil uso de la costruccion y administracuon de la aplicaci贸n.

> Responsabilidades:
> **Proveedor:** Hardware y Sistemas operativos
> **Cliente:** Aplicacion y sus datos.

- Software como Servicio (SaaS): El proveedor en la nube se encarga de hospedar y administrar SaaS para el cliente. Normalmente, esto se licencia a trav茅s de una suscripci贸n mensual o anual. Microsoft 365, Skype y Dynamics CRM Online son ejemplos del software de SaaS.

> Responsabilidades:
> **Proveedor:** Hospedaje y administraci贸n Saas para el cliente, casi todo en excepci贸n de los datos, identidades y recursos locales
> **Cliente:** Administraci贸n de los datos, identidades y recursos locales

---

> En cuanto a todos los tipos de implementaci贸n en la nube, usted es el propietario de sus datos e identidades como cliente de la nube. Asimismo, es responsable de proteger la seguridad de los datos, las identidades y los recursos locales.
> - La informacion y los datos.
> - Los dispositivosd ya sean moviles o locales.
> - Cuentas e identidades
> La ventaja del modelo de responsabilidad compartida es que las organizaciones tienen claras sus responsabilidades y las del proveedor de la nube.

---

## 馃洝锔? Descripcion de la defensa en profundiad.

La defensa en profundidad usa un enfoque por **capas** para la seguridad, en lugar de depender de un solo per铆metro. **Una estrategia de defensa en profundidad usa una serie de mecanismos para ralentizar el avance de un ataque.** Cada capa proporciona protecci贸n de modo que, si se infringe una de ellas, una capa posterior impedir谩 que un atacante obtenga acceso no autorizado a los datos.

### Niveles de Seguridad:

- **La seguridad f铆sica**, como limitar el acceso a un centro de datos solo al personal autorizado.
Controles de seguridad de identidad y acceso, como la autenticaci贸n multifactor o el acceso basado en condiciones, para controlar el acceso a la infraestructura y el control de cambios.

- **La seguridad perimetral** de la red corporativa incluye la protecci贸n frente a ataques de denegaci贸n de servicio distribuido (DDoS) para filtrar los ataques a gran escala antes de que puedan causar una denegaci贸n de servicio para los usuarios.

> DDoS : Es un ataque a un sistema de computadoras o red que **causa que un servicio o recurso sea inaccesible a los usuarios leg铆timos.** 鈥婨s decir, una vez que una p谩gina web es atacada por este medio deja de poder acceder a sus propios datos hasta que es capaz de parar la intrusi贸n. Para lograrlo el atacante satura el servidor en el que se aloja la p谩gina o alguno de sus servicios haciendo que dicho servidor no pueda funcionar correctamente.

- **Seguridad de red**, como la segmentaci贸n de red y los controles de acceso a la red, para limitar la comunicaci贸n entre los recursos.

- **Seguridad de capa de proceso**, como la protecci贸n del acceso a las m谩quinas virtuales, ya sea de forma local o en la nube, cerrando determinados puertos.

- **Seguridad de capa de aplicaci贸n**, que garantiza que las aplicaciones sean seguras y est茅n libres de vulnerabilidades de seguridad.

- **Seguridad de capa de datos** que incluye controles para administrar el acceso a los datos empresariales y de clientes, y el cifrado para proteger los datos.

![Capas](https://docs.microsoft.com/es-mx/learn/wwl-sci/describe-security-concepts-methodologies/media/4-defense-depth.png)

---

## 馃敿 CIA (Confidencialidad, Integridad y Disponibilidad)

Como ya hemops visto, la ciberseguridad esta con la finalidad de proteger y defender el uso correcto del **ciber Espacio** de todo tipo de ataques, y que **una estrategia de defensa en profundidad** usa una serie de mecanismos para ralentizar el avance de un ataque. Aqui entra el triangulo de la ciberseguridad.

![CIA](https://i.stack.imgur.com/nDLPC.png)

1. **La confidencialidad** se refiere a la necesidad de conservar datos confidenciales, como informaci贸n de clientes, contrase帽as o datos financieros. 

> Puede cifrar los datos para mantener la confidencialidad, pero tambi茅n debe mantener la confidencialidad de las claves de cifrado. La confidencialidad es la parte m谩s visible de la seguridad; gracias a ella, podemos ver claramente la necesidad de mantener la confidencialidad de los datos privados, las claves, las contrase帽as y otros secretos.

2. **La integridad** indica la necesidad de mantener los datos o mensajes correctos. 

> Cuando env铆e un mensaje de correo electr贸nico, probablemente quiera asegurarse de que el mensaje recibido sea el mismo que el mensaje enviado. Al almacenar datos en una base de datos, quiere asegurarse tambi茅n de que los datos que recupera son los mismos que los datos almacenados. El cifrado de datos hace que este proceso sea confidencial, pero debe ser capaz de descifrarlo para obtener el mismo contenido que antes del cifrado. La integridad consiste en tener la confianza de que los datos no se han alterado ni modificado.

3. **La disponibilidad** se refiere a poner los datos a disposici贸n de los usuarios cuando los necesiten. 

> Es importante para la organizaci贸n mantener seguros los datos de los clientes, pero al mismo tiempo tambi茅n debe estar disponible para los empleados que trabajan con los clientes. Aunque puede ser m谩s seguro almacenar los datos en un formato cifrado, los empleados necesitan obtener acceso a los datos descifrados.

---

## 馃 Confianza Cero (Zero Trust)

**La confianza cero presupone que todo est谩 en una red abierta y que no es de confianza,** incluso los recursos detr谩s de los firewalls de la red corporativa. El modelo de confianza cero funciona con el principio de "no confiar en nadie y comprobarlo todo".

> Un firewall es un dispositivo de seguridad de la red que monitorea el tr谩fico de red 鈥攅ntrante y saliente鈥? y decide si permite o bloquea tr谩fico espec铆fico en funci贸n de un conjunto definido de reglas de seguridad. 
> **Establecen una barrera entre las redes internas protegidas y controladas en las que se puede confiar y redes externas que no son de confianza, como Internet.**

La capacidad de los atacantes para eludir los controles de acceso convencionales est谩 acabando con cualquier ilusi贸n de que las estrategias de seguridad tradicionales son suficientes. Por lo tanto, al no confiar en la integridad de la red corporativa, se refuerza la seguridad.

_En la pr谩ctica, esto significa que ya no asumimos que una contrase帽a es suficiente para validar a un usuario, sino que agregamos la autenticaci贸n multifactor para proporcionar comprobaciones adicionales. En lugar de conceder acceso a todos los dispositivos de la red corporativa, solo se permite el acceso de los usuarios a las aplicaciones o a los datos espec铆ficos que necesiten._

### Principios de GUID de confianza cero.

Estos tres principio guian y respaldan el modo de implementar la seguridad:

1. **Comprobaci贸n de forma expl铆cita:** Autentique y autorice siempre el contenido en funci贸n de los puntos de datos disponibles, como la identidad del usuario, la ubicaci贸n, el dispositivo, el servicio o la carga de trabajo, la clasificaci贸n de los datos y las anomal铆as.

2. **Acceso con privilegios m铆nimos:** Limite el acceso de los usuarios con acceso Just-in-Time y Just-Enough Access (JIT/JEA), LAS directivas de adaptaci贸n basadas en riesgos y la protecci贸n de datos para proteger los datos y la productividad.

3. **Asumir infracciones de seguridad:** Acceda al segmento mediante la red, el usuario, los dispositivos y la aplicaci贸n. Use el cifrado para proteger los datos y el an谩lisis para obtener visibilidad, detectar amenazas y mejorar la seguridad.

### 6 pilares basicos de Confianza cero.

**En el modelo de confianza cero, todos los elementos funcionan juntos para proporcionar seguridad de un extremo a otro.**

1. **Las identidades** pueden ser usuarios, servicios o dispositivos. Cuando una identidad intenta obtener acceso a un recurso, debe comprobarse mediante la autenticaci贸n s贸lida y seguir los principios de acceso con privilegios m铆nimos.

2. **Los dispositivos** crean una superficie de ataque de gran tama帽o a medida que los datos fluyen desde los dispositivos hasta las cargas de trabajo locales y en la nube. La supervisi贸n del estado y el cumplimiento de los dispositivos es un aspecto importante de la seguridad.

3. **Las aplicaciones** son la manera en que se consumen los datos. Esto incluye la detecci贸n de todas las aplicaciones que se usan, lo que a veces se denomina Shadow IT, ya que no todas las aplicaciones se administran de forma centralizada. Este pilar tambi茅n incluye la administraci贸n de permisos y acceso.

4. **Los datos** se deben clasificar, etiquetar y cifrar en funci贸n de sus atributos. En 煤ltima instancia, los esfuerzos de seguridad est谩n relacionados con la protecci贸n de los datos y garantizan que permanecen seguros cuando salen de los dispositivos, las aplicaciones, la infraestructura y las redes que controla la organizaci贸n.

5. **La infraestructura**, ya sea local o en la nube, representa un vector de amenazas. Para mejorar la seguridad, debe evaluar la versi贸n, la configuraci贸n y el acceso JIT, y usar la telemetr铆a para detectar ataques y anomal铆as. Esto le permite bloquear o marcar autom谩ticamente el comportamiento de riesgo y tomar medidas de protecci贸n.

6. **Las redes** deben segmentarse, incluida la microsegmentaci贸n en la red m谩s profunda. Asimismo, es necesario emplear la protecci贸n contra amenazas en tiempo real, el cifrado, la supervisi贸n y el an谩lisis de un extremo a otro.

![seisP](https://docs.microsoft.com/es-mx/learn/wwl-sci/describe-security-concepts-methodologies/media/2-zero-trust-pillars-v2.png)

---

## 馃檴 Cifrados.

**Una manera de mitigar las amenazas de ciberseguridad m谩s comunes es cifrar datos confidenciales o valiosos.**

> El cifrado es el proceso para hacer que los datos aparezcan ilegibles e in煤tiles para visores no autorizados. Para usar o leer los datos cifrados, es necesario descifrarlos, lo que exige el uso de una clave secreta.

Hay dos tipos de cifrado de nivel superior: 

1. **Sim茅trico:** Usa la misma clave para cifrar y descifrar los datos.
2. **Asim茅trico:**  Usa un par de claves p煤blica y privada. 

Cualquiera de las claves puede cifrar los datos, pero no se puede usar una sola clave para descifrar los datos cifrados. Para descifrarlos se necesita la otra clave emparejada. El cifrado asim茅trico se usa para cosas como el acceso a sitios en Internet mediante el protocolo HTTPS y las soluciones de firma de datos electr贸nicas. El cifrado puede proteger los datos en reposo o en tr谩nsito.

![cifrados](https://docs.microsoft.com/es-mx/learn/wwl-sci/describe-security-concepts-methodologies/media/6-encryption.png)

### Cifrado de datos en reposo.

Los datos en reposo **son los datos que se almacenan en un dispositivo f铆sico, como un servidor.** Pueden estar almacenados en una base de datos o en una cuenta de almacenamiento, pero, independientemente de d贸nde est茅n almacenados, el cifrado de datos en reposo **garantiza** que los datos no se puedan leer sin las claves y los secretos necesarios para descifrarlos.

> Si un atacante obtuviera una unidad de disco duro con datos cifrados, pero no tuviera acceso a las claves de cifrado, no podr铆a leer los datos.

### Cifrado de datos en tr谩nsito.

**Los datos en tr谩nsito son los que se est谩n moviendo de una ubicaci贸n a otra**

> Por ejemplo, por Internet o a trav茅s de una red privada. La transferencia segura se puede controlar mediante varias capas diferentes. Esto se puede hacer mediante el cifrado de los datos en el nivel de aplicaci贸n antes de enviarlos a trav茅s de una red. HTTPS es un ejemplo de cifrado en tr谩nsito.

**El cifrado de datos en tr谩nsito protege los datos de observadores externos y proporciona un mecanismo para transmitirlos que limita el riesgo de exposici贸n.**

### Cifrado de datos en uso.

Un caso de uso com煤n para el cifrado de datos en uso **conlleva proteger los datos en un almacenamiento no persistente, como la RAM o la memoria cach茅 de CPU.** Esto se puede lograr mediante tecnolog铆as que crean un enclave (como si fuera una caja fuerte con llave) que protege los datos y los mantiene cifrados mientras la CPU los procesa.
 
 ---

## Aplicaci贸ne de algoritmos Hash.

**El hash utiliza un algoritmo para convertir el texto en un valor hash de longitud fija 煤nico denominado hash.** Cada vez que se aplica un algoritmo hash al mismo texto mediante el mismo algoritmo, se genera el mismo valor hash. Ese hash se puede usar como identificador 煤nico de los datos asociados.

![hash](https://criptomo.com/images/posts/201807/hashing-vs-encryption.png)

> El hash es diferente del cifrado, ya que no usa claves, y el valor al que se aplica el algoritmo hash no se descifra posteriormente en el original.

*El hash se usa para almacenar contrase帽as*. Cuando un usuario escribe su contrase帽a, el mismo algoritmo que cre贸 el hash almacenado crea un hash de la contrase帽a escrita. A continuaci贸n, se compara con la versi贸n hash almacenada de la contrase帽a. Si coinciden, es que el usuario ha escrito correctamente la contrase帽a. Esto es m谩s seguro que el almacenamiento de contrase帽as de texto sin formato, pero los hackers tambi茅n conocen los algoritmos hash. **Dado que las funciones hash son deterministas (esto es, la misma entrada produce el mismo resultado)**, los hackers pueden usar los ataques de **diccionario por fuerza bruta** mediante el hash de las contrase帽as. Por cada hash coincidente, obtienen la contrase帽a real. Para reducir este riesgo, a menudo las contrase帽as se "cifran con sal". Esto hace referencia a que se agrega un valor aleatorio de longitud fija a la entrada de las funciones hash para crear valores hash 煤nicos para la misma entrada.

---

## 馃摉 Descripci贸n de los conceptos de cumplimiento.

Es muy claro que mediante la tecnologia avanza, el uso de la misma y el generar datos e informaci贸n se ha hecho casi un caso normativo, es asi que al incremento de esta misma data, se ha hecho casi fundamental poder proteger y tener privada esta misma informaci贸n, tanto para usuarios como a proveedores de servicios.

Los organismos gubernamentales y los grupos del sector han aprobado reglamentos para **ayudar a proteger y controlar el uso de los datos. Desde la informaci贸n personal y financiera hasta la protecci贸n de datos y la privacidad, las organizaciones pueden tener la responsabilidad de cumplir decenas de reglamentos. A continuaci贸n se enumeran algunos conceptos y t茅rminos importantes relacionados con el cumplimiento de los datos.

1. **Residencia de datos:** cuando se trata de cumplimiento, los reglamentos de residencia de datos rigen las ubicaciones f铆sicas donde se pueden almacenar los datos y c贸mo y cu谩ndo se pueden transferir, procesar o acceder a escala internacional. Estos reglamentos pueden variar significativamente en funci贸n de la jurisdicci贸n.

2. **Soberan铆a de datos:** otra consideraci贸n importante es la soberan铆a de los datos, el concepto de que los datos, especialmente _los datos personales_, est谩n sujetos a las leyes y los reglamentos del pa铆s o la regi贸n donde se recopilan, conservan o procesan f铆sicamente. Esto puede agregar una capa de complejidad cuando se trata de cumplimiento porque se puede recopilar el mismo fragmento de datos en una ubicaci贸n, almacenarse en otra y procesarse en otra, por lo que estar铆a sujeto a las leyes de diferentes regiones o pa铆ses.

3. **Privacidad de los datos:** proporcionar avisos y ser transparentes sobre la recopilaci贸n, el procesamiento, el uso y el uso compartido de los datos personales constituyen los principios fundamentales de las leyes y los reglamentos sobre privacidad. "Datos personales" hace referencia a cualquier informaci贸n relativa a una persona f铆sica identificada o identificable. Las leyes sobre privacidad antes hac铆an referencia a "DCP" o "informaci贸n de identificaci贸n personal", pero las leyes han ampliado la definici贸n a cualquier dato que est茅 directamente vinculado o que se pueda vincular indirectamente a una persona. Las organizaciones est谩n sujetas a una multitud de leyes, reglamentos, c贸digos de conducta, est谩ndares espec铆ficos del sector y est谩ndares de cumplimiento que rigen la privacidad de los datos y, por tanto, deben operar conforme a ellos.