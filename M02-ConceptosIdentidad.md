# 馃啍 Conceptos de identidad.

Es importante tener en claro que, todos los usuarios y todos los dispositivos **tienen una identidad que se puede usar para tener acceso a los recursos.** La identidad es la forma en que se identifican las personas y las cosas en la red corporativa y en la nube. Tener la seguridad de qui茅n o qu茅 est谩 accediendo a los datos de la organizaci贸n y otros recursos es una parte fundamental de la protecci贸n del entorno.

## Autenticaci贸n (AuthN).

**La autenticaci贸n** _es el proceso de demostrar que una persona es quien dice ser._ 

> Cuando alguien compra un art铆culo con una tarjeta de cr茅dito, es posible que tenga que mostrar una forma adicional de identificaci贸n. De esta manera, demuestra que es la persona cuyo nombre aparece en la tarjeta. En este ejemplo, el usuario puede mostrar el DNI, que sirve como forma de autenticaci贸n y verifica su identidad.

Ahora bien, actualmente tenemos cosas de valor digitalmente, por eso **si desea acceder a un equipo o un dispositivo,** se encontrar谩 con un tipo de autenticaci贸n similar. Es posible que se le pida que escriba un nombre de usuario y una contrase帽a. El nombre de usuario indica qui茅n es, pero no es suficiente por s铆 solo para concederle acceso. Cuando lo combina con la contrase帽a, que solo usted debe conocer, obtiene acceso a los sistemas. **El nombre de usuario y la contrase帽a, juntos, son una forma de autenticaci贸n. A veces, la autenticaci贸n se abrevia como AuthN.**

![AunthN](https://dinahosting.com/blog/cont/uploads/2019/10/autenticacion2pasos-scaled.jpg)

## Autorizaci贸n (AuthZ).

Cuando autentique a un usuario, tendr谩 que decidir ad贸nde puede ir y qu茅 se le permite ver y tocar. Este proceso se denomina autorizaci贸n.

> Supongamos que quiere pasar la noche en un hotel. Lo primero que har谩 es ir a la recepci贸n para iniciar el "proceso de autenticaci贸n". Una vez que el recepcionista haya comprobado qui茅n es, le dar谩 una tarjeta-llave y ya podr谩 dirigirse a su habitaci贸n. Piense en la tarjeta-llave como el proceso de autorizaci贸n. La tarjeta-llave solo le permitir谩 abrir las puertas y los ascensores a los que puede acceder, como la puerta de su habitaci贸n.

**En t茅rminos de ciberseguridad, la autorizaci贸n determina el nivel de acceso o los permisos de una persona autenticada a los datos y los recursos. A veces, la autorizaci贸n se abrevia como AuthZ.**

![authZ](https://www.albertcoronado.com/wp-content/uploads/2019/08/permisos-ciberseguridad-liferay.jpg)

---

## 馃啍 Identidad como perimetro de seguridad principal.

Actualmente con todo lo que ha sucedido, es normal entender que los empleados de una organizacion ahora necesitan colaborar y acceder a los recursos de la organizacion desde cualquier lugar, en **cualquier dispositivo donde no pueda ser afectada su productividad.**

 Tambi茅n se ha producido una aceleraci贸n en el n煤mero de personas que trabajan desde casa. 

 **La seguridad de la empresa debe adaptarse a esta nueva realidad.** El per铆metro de seguridad ya no se puede ver como la red local. Ahora se extiende a:

- Aplicaciones SaaS para cargas de trabajo cr铆ticas para la empresa que se pueden hospedar fuera de la red corporativa.

- Los dispositivos personales que los empleados usan para tener acceso a los recursos corporativos (BYOD o Bring Your Own Device) mientras trabajan desde casa.

> Bring your own device, abreviado BYOD, es una pol铆tica empresarial consistente en que los empleados lleven sus propios dispositivos personales a su lugar de trabajo para tener acceso a recursos de la empresa tales como correos electr贸nicos, bases de datos y archivos en servidores as铆 como datos y aplicaciones personales.

- Los dispositivos no administrados que usan los asociados o clientes al interactuar con los datos corporativos o colaborar con los empleados.

- Internet de las cosas, conocido como dispositivos IoT, instalado en la red corporativa y dentro de las ubicaciones de los clientes.

Para eos debemos de tener en claro que la **Idetidad es un conjunto de aspectos que definen o caracterizan a alguien o algo**. Dado como ejemplo, podremos decir que la identidad de una persona incluye la informacion que usa para autentificarse, como su nombre de usuario y password y su nivel de autorizaci贸n.

> _El modelo de seguridad tradicional basado en el per铆metro ya no es suficiente. **La identidad** se ha convertido en el nuevo per铆metro de seguridad que permite a las organizaciones proteger sus recursos._

![identidad](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-identity-principles-concepts/media/3-identity-new-security-perimeter.png)

## 馃啍 4 pilares de una infrestructura de identidad.

Esto debe ser una base para toda organizaci贸n ya que la seguridad interna debe de estar altamente organizada, en esta hay una colecci贸n de procesos, tecnolog铆as y directivas **para administrar identidades digitales y controlar c贸mo se usan para tener acceso a los recursos.** Pueden organizarse en cuatro pilares fundamentales que las organizaciones deben tener en cuenta al crear una infraestructura de identidad.

1. **Administraci贸n.** La administraci贸n consiste en la creaci贸n y la administraci贸n o gobernanza de identidades para los usuarios, dispositivos y servicios _(Creando un ambiente seguro)_. Como administrador, _puede administrar c贸mo y en qu茅 circunstancias pueden cambiar las caracter铆sticas de las identidades_ (se pueden crear, actualizar y eliminar).

2. **Autenticaci贸n.** Indica _cu谩nto necesita saber un sistema de TI sobre una identidad para tener pruebas suficientes de que realmente son quienes dicen ser. Implica el acto de solicitar a un usuario credenciales leg铆timas._

3. **Autorizaci贸n.** Esta trata sobre el procesamiento de los datos de identidad entrante para determinar el nivel de acceso de una persona o servicio autenticado dentro de la aplicaci贸n o servicio al que quiere obtener acceso.

4. **Auditor铆a.** Esta consiste en realizar un seguimiento de qui茅n realiza qu茅, cu谩ndo, d贸nde y c贸mo. _La auditor铆a incluye la creaci贸n de informes, alertas y gobernanza de identidades en profundidad._

---

## 馃搰 Rol del proveedor de identidades.

Entrando a la modernidad, esxiste el teminoi de **Autenticaci贸n moderna**, este es un t茅rmino gen茅rico para los m茅todos de autenticaci贸n y autorizaci贸n entre un cliente, como un port谩til o un tel茅fono, y un servidor, como un sitio web o una aplicaci贸n. En el centro de la autenticaci贸n moderna est谩 el rol del proveedor de identidades. 

> Un proveedor de identidades crea, mantiene y administra la informaci贸n de identidad al tiempo que proporciona servicios de autenticaci贸n, autorizaci贸n y auditor铆a.

> Con la autenticaci贸n moderna, quien proporciona todos los servicios, incluidos todos los servicios de autenticaci贸n, es un proveedor de identidades central. El proveedor de identidades almacena y administra de forma centralizada la informaci贸n que se usa para autenticar el usuario en el servidor.

### 馃 驴Que son los token?

Pues bien, los token son un tipo  de documento firmado *criptograficamente*, que coniene elementos sobre la persona que usa el cliente y a los que llamamos notificaci贸nes --> Estas notificaciones no son m谩s que **informaci贸n** sobre la identidad que lamna al servidor, y no tiene que ser una persona. _(Son pares de valores de atributos que contienen informaci贸n sobre la identidad que esta usando el servicio)_

Teniendo en cuenta lo de los tokens **gracias a la autenticaci贸n moderna,** el cliente se comunica con el proveedor de identidades mediante la asignaci贸n de una identidad que se puede autenticar. Cuando se ha comprobado la identidad (que puede ser un usuario o una aplicaci贸n), el proveedor de identidades emite un token de seguridad que el cliente env铆a al servidor.

> El servidor valida el token de seguridad a trav茅s de su relaci贸n de confianza con el proveedor de identidades. Mediante el uso del token de seguridad y la informaci贸n que contiene, el usuario o la aplicaci贸n accede a los recursos necesarios en el servidor. En este escenario, el proveedor de identidades almacena y administra el token y la informaci贸n que contiene. El proveedor de identidades centralizado proporciona el servicio de autenticaci贸n.

### Inicio de sesion Unica.

Otra funcionalidad fundamental de un proveedor de identidades y "autenticaci贸n moderna" es la compatibilidad con el inicio de sesi贸n 煤nico (SSO). Con el SSO, el usuario inicia sesi贸n una vez y esa credencial se usa para tener acceso a varias aplicaciones o recursos. A la acci贸n de configurar el SSO para que funcione entre varios proveedores de identidades se le conoce como federaci贸n.

---

## 馃摎 Concepto de servicios de directorios y Active Directory.

En el contexto de una red de equipos, **un directorio es una estructura jer谩rquica que almacena informaci贸n acerca de los objetos de la red.** Un servicio de directorio almacena los datos del directorio y los pone a disposici贸n de los usuarios de red, los administradores, los servicios y las aplicaciones.

> **Active Directory (AD)** es un conjunto de servicios de directorio desarrollados por Microsoft como parte de Windows 2000 para redes locales basadas en dominio. El servicio m谩s conocido de este tipo es Active Directory Domain Services (AD DS). Almacena informaci贸n sobre los miembros del dominio, incluidos los dispositivos y los usuarios, comprueba sus credenciales y define sus derechos de acceso. Un servidor que ejecuta AD DS es un controlador de dominio.

*AD DS* es un componente central de las organizaciones con una infraestructura de TI local. **AD DS ofrece a las organizaciones la capacidad de administrar varios sistemas y componentes de la infraestructura local mediante una 煤nica identidad por usuario.** Sin embargo, AD DS no es compatible de forma nativa con los dispositivos m贸viles, las aplicaciones SaaS o las aplicaciones de l铆nea de negocio que requieren m茅todos de autenticaci贸n moderna.

El crecimiento de Cloud Services, las aplicaciones SaaS y los dispositivos personales que se usan en el trabajo, ha dado como resultado la necesidad de la autenticaci贸n moderna y una evoluci贸n de las soluciones de identidad basadas en Active Directory.

Azure Active Directory es la siguiente evoluci贸n de las soluciones de administraci贸n de identidad y acceso. Proporciona a las organizaciones una soluci贸n de identidad como servicio (IDaaS) para todas sus aplicaciones en la nube y en el entorno local. 

---

## 馃懆鈥嶐煉? Conceptos de Federaci贸n.

**La federaci贸n permite el acceso a los servicios a trav茅s de los l铆mites de la organizaci贸n o del dominio mediante el establecimiento de relaciones de confianza entre el proveedor de identidades del dominio correspondiente.**

![federacion](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-identity-principles-concepts/media/5-federated-identification.png)

> Con la federaci贸n, no es necesario que un usuario mantenga un nombre de usuario y una contrase帽a diferentes al acceder a los recursos de otros dominios, podremos visualizarlo de esta manera: 

- El sitio web, en el dominio A, usa los servicios de autenticaci贸n del proveedor de identidades A (IdP-A).
- El usuario, en el dominio B, se autentica con el proveedor de identidades B (IdP-B).
- IdP-A tiene una relaci贸n de confianza configurada con IdP-B.
- Cuando el usuario, que desea acceder al sitio web, proporciona sus credenciales, el sitio web conf铆a en el usuario y permite el acceso. Este acceso se permite debido a la confianza que ya se ha establecido entre los dos proveedores de identidades.

