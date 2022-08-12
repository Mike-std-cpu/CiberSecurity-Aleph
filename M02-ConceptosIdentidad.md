# 🆔 Conceptos de identidad.

Es importante tener en claro que, todos los usuarios y todos los dispositivos **tienen una identidad que se puede usar para tener acceso a los recursos.** La identidad es la forma en que se identifican las personas y las cosas en la red corporativa y en la nube. Tener la seguridad de quién o qué está accediendo a los datos de la organización y otros recursos es una parte fundamental de la protección del entorno.

## Autenticación (AuthN).

**La autenticación** _es el proceso de demostrar que una persona es quien dice ser._ 

> Cuando alguien compra un artículo con una tarjeta de crédito, es posible que tenga que mostrar una forma adicional de identificación. De esta manera, demuestra que es la persona cuyo nombre aparece en la tarjeta. En este ejemplo, el usuario puede mostrar el DNI, que sirve como forma de autenticación y verifica su identidad.

Ahora bien, actualmente tenemos cosas de valor digitalmente, por eso **si desea acceder a un equipo o un dispositivo,** se encontrará con un tipo de autenticación similar. Es posible que se le pida que escriba un nombre de usuario y una contraseña. El nombre de usuario indica quién es, pero no es suficiente por sí solo para concederle acceso. Cuando lo combina con la contraseña, que solo usted debe conocer, obtiene acceso a los sistemas. **El nombre de usuario y la contraseña, juntos, son una forma de autenticación. A veces, la autenticación se abrevia como AuthN.**

![AunthN](https://dinahosting.com/blog/cont/uploads/2019/10/autenticacion2pasos-scaled.jpg)

## Autorización (AuthZ).

Cuando autentique a un usuario, tendrá que decidir adónde puede ir y qué se le permite ver y tocar. Este proceso se denomina autorización.

> Supongamos que quiere pasar la noche en un hotel. Lo primero que hará es ir a la recepción para iniciar el "proceso de autenticación". Una vez que el recepcionista haya comprobado quién es, le dará una tarjeta-llave y ya podrá dirigirse a su habitación. Piense en la tarjeta-llave como el proceso de autorización. La tarjeta-llave solo le permitirá abrir las puertas y los ascensores a los que puede acceder, como la puerta de su habitación.

**En términos de ciberseguridad, la autorización determina el nivel de acceso o los permisos de una persona autenticada a los datos y los recursos. A veces, la autorización se abrevia como AuthZ.**

![authZ](https://www.albertcoronado.com/wp-content/uploads/2019/08/permisos-ciberseguridad-liferay.jpg)

---

## 🆔 Identidad como perimetro de seguridad principal.

Actualmente con todo lo que ha sucedido, es normal entender que los empleados de una organizacion ahora necesitan colaborar y acceder a los recursos de la organizacion desde cualquier lugar, en **cualquier dispositivo donde no pueda ser afectada su productividad.**

 También se ha producido una aceleración en el número de personas que trabajan desde casa. 

 **La seguridad de la empresa debe adaptarse a esta nueva realidad.** El perímetro de seguridad ya no se puede ver como la red local. Ahora se extiende a:

- Aplicaciones SaaS para cargas de trabajo críticas para la empresa que se pueden hospedar fuera de la red corporativa.

- Los dispositivos personales que los empleados usan para tener acceso a los recursos corporativos (BYOD o Bring Your Own Device) mientras trabajan desde casa.

> Bring your own device, abreviado BYOD, es una política empresarial consistente en que los empleados lleven sus propios dispositivos personales a su lugar de trabajo para tener acceso a recursos de la empresa tales como correos electrónicos, bases de datos y archivos en servidores así como datos y aplicaciones personales.

- Los dispositivos no administrados que usan los asociados o clientes al interactuar con los datos corporativos o colaborar con los empleados.

- Internet de las cosas, conocido como dispositivos IoT, instalado en la red corporativa y dentro de las ubicaciones de los clientes.

Para eos debemos de tener en claro que la **Idetidad es un conjunto de aspectos que definen o caracterizan a alguien o algo**. Dado como ejemplo, podremos decir que la identidad de una persona incluye la informacion que usa para autentificarse, como su nombre de usuario y password y su nivel de autorización.

> _El modelo de seguridad tradicional basado en el perímetro ya no es suficiente. **La identidad** se ha convertido en el nuevo perímetro de seguridad que permite a las organizaciones proteger sus recursos._

![identidad](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-identity-principles-concepts/media/3-identity-new-security-perimeter.png)

## 🆔 4 pilares de una infrestructura de identidad.

Esto debe ser una base para toda organización ya que la seguridad interna debe de estar altamente organizada, en esta hay una colección de procesos, tecnologías y directivas **para administrar identidades digitales y controlar cómo se usan para tener acceso a los recursos.** Pueden organizarse en cuatro pilares fundamentales que las organizaciones deben tener en cuenta al crear una infraestructura de identidad.

1. **Administración.** La administración consiste en la creación y la administración o gobernanza de identidades para los usuarios, dispositivos y servicios _(Creando un ambiente seguro)_. Como administrador, _puede administrar cómo y en qué circunstancias pueden cambiar las características de las identidades_ (se pueden crear, actualizar y eliminar).

2. **Autenticación.** Indica _cuánto necesita saber un sistema de TI sobre una identidad para tener pruebas suficientes de que realmente son quienes dicen ser. Implica el acto de solicitar a un usuario credenciales legítimas._

3. **Autorización.** Esta trata sobre el procesamiento de los datos de identidad entrante para determinar el nivel de acceso de una persona o servicio autenticado dentro de la aplicación o servicio al que quiere obtener acceso.

4. **Auditoría.** Esta consiste en realizar un seguimiento de quién realiza qué, cuándo, dónde y cómo. _La auditoría incluye la creación de informes, alertas y gobernanza de identidades en profundidad._

---

## 📇 Rol del proveedor de identidades.

Entrando a la modernidad, esxiste el teminoi de **Autenticación moderna**, este es un término genérico para los métodos de autenticación y autorización entre un cliente, como un portátil o un teléfono, y un servidor, como un sitio web o una aplicación. En el centro de la autenticación moderna está el rol del proveedor de identidades. 

> Un proveedor de identidades crea, mantiene y administra la información de identidad al tiempo que proporciona servicios de autenticación, autorización y auditoría.

> Con la autenticación moderna, quien proporciona todos los servicios, incluidos todos los servicios de autenticación, es un proveedor de identidades central. El proveedor de identidades almacena y administra de forma centralizada la información que se usa para autenticar el usuario en el servidor.

### 🤔 ¿Que son los token?

Pues bien, los token son un tipo  de documento firmado *criptograficamente*, que coniene elementos sobre la persona que usa el cliente y a los que llamamos notificaciónes --> Estas notificaciones no son más que **información** sobre la identidad que lamna al servidor, y no tiene que ser una persona. _(Son pares de valores de atributos que contienen información sobre la identidad que esta usando el servicio)_

Teniendo en cuenta lo de los tokens **gracias a la autenticación moderna,** el cliente se comunica con el proveedor de identidades mediante la asignación de una identidad que se puede autenticar. Cuando se ha comprobado la identidad (que puede ser un usuario o una aplicación), el proveedor de identidades emite un token de seguridad que el cliente envía al servidor.

> El servidor valida el token de seguridad a través de su relación de confianza con el proveedor de identidades. Mediante el uso del token de seguridad y la información que contiene, el usuario o la aplicación accede a los recursos necesarios en el servidor. En este escenario, el proveedor de identidades almacena y administra el token y la información que contiene. El proveedor de identidades centralizado proporciona el servicio de autenticación.

### Inicio de sesion Unica.

Otra funcionalidad fundamental de un proveedor de identidades y "autenticación moderna" es la compatibilidad con el inicio de sesión único (SSO). Con el SSO, el usuario inicia sesión una vez y esa credencial se usa para tener acceso a varias aplicaciones o recursos. A la acción de configurar el SSO para que funcione entre varios proveedores de identidades se le conoce como federación.

---

## 📚 Concepto de servicios de directorios y Active Directory.

En el contexto de una red de equipos, **un directorio es una estructura jerárquica que almacena información acerca de los objetos de la red.** Un servicio de directorio almacena los datos del directorio y los pone a disposición de los usuarios de red, los administradores, los servicios y las aplicaciones.

> **Active Directory (AD)** es un conjunto de servicios de directorio desarrollados por Microsoft como parte de Windows 2000 para redes locales basadas en dominio. El servicio más conocido de este tipo es Active Directory Domain Services (AD DS). Almacena información sobre los miembros del dominio, incluidos los dispositivos y los usuarios, comprueba sus credenciales y define sus derechos de acceso. Un servidor que ejecuta AD DS es un controlador de dominio.

*AD DS* es un componente central de las organizaciones con una infraestructura de TI local. **AD DS ofrece a las organizaciones la capacidad de administrar varios sistemas y componentes de la infraestructura local mediante una única identidad por usuario.** Sin embargo, AD DS no es compatible de forma nativa con los dispositivos móviles, las aplicaciones SaaS o las aplicaciones de línea de negocio que requieren métodos de autenticación moderna.

El crecimiento de Cloud Services, las aplicaciones SaaS y los dispositivos personales que se usan en el trabajo, ha dado como resultado la necesidad de la autenticación moderna y una evolución de las soluciones de identidad basadas en Active Directory.

Azure Active Directory es la siguiente evolución de las soluciones de administración de identidad y acceso. Proporciona a las organizaciones una solución de identidad como servicio (IDaaS) para todas sus aplicaciones en la nube y en el entorno local. 

---

## 👨‍💼 Conceptos de Federación.

**La federación permite el acceso a los servicios a través de los límites de la organización o del dominio mediante el establecimiento de relaciones de confianza entre el proveedor de identidades del dominio correspondiente.**

![federacion](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-identity-principles-concepts/media/5-federated-identification.png)

> Con la federación, no es necesario que un usuario mantenga un nombre de usuario y una contraseña diferentes al acceder a los recursos de otros dominios, podremos visualizarlo de esta manera: 

- El sitio web, en el dominio A, usa los servicios de autenticación del proveedor de identidades A (IdP-A).
- El usuario, en el dominio B, se autentica con el proveedor de identidades B (IdP-B).
- IdP-A tiene una relación de confianza configurada con IdP-B.
- Cuando el usuario, que desea acceder al sitio web, proporciona sus credenciales, el sitio web confía en el usuario y permite el acceso. Este acceso se permite debido a la confianza que ya se ha establecido entre los dos proveedores de identidades.

