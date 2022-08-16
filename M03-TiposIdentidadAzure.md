# Descripcion de los servicios y los tipos de identidades de Azure AD.

En esta secciòn podremos enteder de una manera mas sencilla ¿Que es? **Azure Active Directory (Azure AD),** que es un servicio de administración de acceso y de identidades basado en la nube de Microsoft. 

> En cuanto a la seguridad, su organización ya no puede confiar en el límite de su red. Para permitir que empleados, asociados y clientes colaboren de forma segura, las organizaciones deben cambiar a un enfoque en el que la identidad se convierta en el nuevo perímetro de seguridad. El uso de un proveedor de identidades ayuda a las organizaciones a administrar ese cambio y todos los aspectos de la seguridad de las identidades.

## Descripcion de Azure Active Directory.

Azure Active Directory (Azure AD) basicamente **es un servicio de administración de acceso y de identidades basado en la nube de Microsoft.** Las organizaciones usan este servicio de Azure para permitir que sus empleados, invitados y otros usuarios inicien sesión y tengan acceso a los recursos que necesitan, incluidos:

1. Recursos internos, como las aplicaciones de la red corporativa y la intranet, junto con todas las aplicaciones en la nube que haya desarrollado su propia organización.

2. Servicios externos, como Microsoft Office 365, Azure Portal y cualquier aplicación SaaS que use su organización.

Azure AD de igual manera permite a las organizaciones habilitar de manera segura el uso de dispositivos personales:

- Tablets.
- Moviles.

Permitiendo la colaboración con clientes y asociados comerciales, a continuacion se aneara una imagen explicativa d elas funciones generales de Azure AD:

![Azure AD](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-basic-services-identity-types/media/azure-active-directory-diagram-expanded.png)

- Todo esto es manejado por lso **Administradores de TI usando Azure AD para asi "Controlar los accesos a los recursos y a las aplicaciones corporativas, en cuestion y base a los requisitos empresariales de la organziación".

-  También puede configurarse para requerir la autenticación multifactor cuando el usuario intenta acceder a recursos importantes de la organización. 

- , Azure AD se puede usar para automatizar el aprovisionamiento de usuarios entre una instancia de Windows Server AD existente y aplicaciones en la nube, incluyendo Microsoft 365.

- Azure AD proporciona herramientas eficaces que le ayudarán a proteger automáticamente las identidades y credenciales de los usuarios y a cumplir los requisitos de gobernanza de acceso de la empresa.

- En desarrollo, los developers usan Azure AD como un enfoque basado en estándares para agregar el inicio de sesión único (SSO) a sus aplicaciones, de modo que los usuarios puedan iniciar sesión con credenciales ya existentes. Asimismo, Azure AD también proporciona varias API que permiten que los desarrolladores creen experiencias de aplicación personalizadas que usen los datos existentes de la organización.

> Los suscriptores de servicios de Azure, Microsoft 365 o Dynamics 365 tienen acceso automático a Azure AD. Los usuarios de estos servicios pueden sacar provecho de los servicios de Azure AD incluidos y también pueden mejorar su implementación de Azure AD mediante la actualización a licencias Premium de Azure AD.

---

## Descripciones de las ediciones de Azure AD.

Azzure AD esta descrita en 4 ediciones:

1. Free (Gratuita)
2. Apliaciones de Office 365.
3. Premium P1.
4. Premium P2.

### Azure AD Free:

La versión gratuita le permite:
- Administrar usuarios y crear grupos.
- Sincronizarse con la instancia local de Active Directory.
- Crear informes básicos.
- Configurar el cambio de contraseña de autoservicio para usuarios en la nube y habilitar el inicio de sesión único en Azure.
- Microsoft 365 y muchas otras aplicaciones populares de SaaS.

>  La edición gratuita se incluye con las suscripciones a Office 365, Azure, Dynamics 365, Intune y Power Platform.

### Aplicaciones de Office 365:

La edición de Aplicaciones de Office 365 le permite:

- Hacer todo lo que se incluye en la versión gratuita.
- Más la opción de restablecer la contraseña de autoservicio para usuarios en la nube y la reescritura de dispositivos.
- Ofrece una sincronización bidireccional entre directorios locales y Azure AD. 
- La edición de Aplicaciones de Office 365 de Azure Active Directory se incluye en las suscripciones a Office 365 E1, E3, E5, F1 y F3.

### Azure AD Premium P1:

- Admite la administración avanzada, como grupos dinámicos, administración de grupos de autoservicio.
- Microsoft Identity Manager (un conjunto de administración local de identidades y acceso) y funcionalidades de reescritura en la nube, que permiten el restablecimiento de contraseña de autoservicio a los usuarios locales.

> La edición Premium P1 incluye todas las características de las ediciones Gratis y Aplicaciones de Office 365.

### Azure AD Premium P2:

eSTA  edición P2 también le proporciona la instancia de **Privileged Identity Management** que le permitirá detectar, restringir y supervisar a los administradores y su acceso a los recursos y proporcionar acceso de tipo "Just-in-Time" cuando sea necesario.

>  La versión P2 le ofrece todas las características de la edición Premium P1 y Azure Active Directory Identity Protection para facilitar el acceso condicional basado en riesgos a las aplicaciones y a los datos críticos de la empresa.

_También hay una opción para las licencias de característicasde "Pago por uso". Puede obtener otras licencias de características por separado, como la opción Negocio a cliente (B2C) de Azure Active Directory. B2C puede ayudarle a proporcionar soluciones de administración de acceso y de identidad para las aplicaciones orientadas al cliente. Para más información, consulte Documentación de Azure Active Directory B2C._

---

## Descripcion de los tipos de identidad de Azure AD.

En azure AD existen distintos tipos de identidades:

1. Uusarios.
2. Entidades de servicios.
3. Identidades administradas.
4. Dispositivos.

### Usarios.

Los empleados e invitados se representan como usuarios en Azure AD. Si tiene varios usuarios con las mismas necesidades de acceso, puede crear un grupo.

> Los grupos se usan para conceder permisos de acceso a todos los miembros del grupo, en lugar de tener que asignar derechos de acceso individualmente.

**La colaboración de negocio a negocio (B2B)** de Azure AD es una característica de External Identities e incluye una funcionalidad **para agregar usuarios invitados**. Gracias a la colaboración B2B, _una organización puede compartir aplicaciones y servicios de forma segura con usuarios invitados de otra organización._

### Entidad de servicios.

Una entidad de servicio es, básicamente, **una identidad para una aplicación**. Para que una aplicación delegue su identidad y funciones de acceso a Azure AD, primero se debe registrar con Azure AD a fin de habilitar su integración. Una vez que se registra, **se crea una entidad de servicio en cada inquilino de Azure AD donde se usa la aplicación.** La entidad de servicio habilita características básicas como la autenticación y autorización de la aplicación en los recursos protegidos por el inquilino de Azure AD.

Para que las entidades de servicio puedan acceder a los recursos protegidos por el inquilino de Azure AD, los desarrolladores de aplicaciones deben administrar y proteger las credenciales.

### Identidad Administrada.

Las identidades administradas son un tipo de entidad de servicio que se administran de forma automática en Azure AD y eliminan la necesidad de que los desarrolladores administren las credenciales. Las identidades administradas proporcionan una identidad para que la usen las aplicaciones al conectarse a recursos de Azure compatibles con la autenticación de Azure AD, sin costo adicional.

>> En otras palabras, es la conceccion de apliaciones conservicios de Azure para el mismo azure.
>>                              **CONEXION DE AZURE CON AZURE**

- **Asignadas por el sistema.** Algunos servicios de Azure permiten habilitar una identidad administrada directamente en una instancia de servicio. Cuando se habilita una identidad administrada asignada por el sistema, se crea una identidad en Azure AD que está vinculada al ciclo de vida de esa instancia de servicio. Por tanto, cuando se elimina el recurso, Azure elimina automáticamente la identidad. Por diseño, solo ese recurso de Azure puede usar esta identidad para solicitar tokens de Azure AD.

- **Asignadas por el usuario.** También es posible crear una identidad administrada como un recurso independiente de Azure. Una vez que se crea una identidad administrada asignada por el usuario, puede asignarla a una o varias instancias de un servicio de Azure. En el caso de las identidades administradas asignadas por el usuario, la identidad se administra independientemente de los recursos que la utilicen.

### Dispositivos.

Un dispositivo es un producto de hardware, como los dispositivos móviles, los equipos portátiles, los servidores o las impresoras. **Una identidad de dispositivo proporciona a los administradores información que pueden usar al tomar decisiones de acceso o configuración.** Hay varias formas de configurar las identidades de dispositivo en Azure AD.

1. **Dispositivos registrados en Azure AD.** El objetivo es proporcionar a los usuarios la **compatibilidad** con escenarios **Bring Your Own Device (BYOD)** o de dispositivos móviles. En estos escenarios, **el usuario puede acceder a los recursos de la organización con un dispositivo personal.**

> Los dispositivos registrados en Azure AD se registran sin necesidad de que una cuenta de la organización inicie sesión en el dispositivo. Los sistemas operativos compatibles con los dispositivos registrados de Azure AD incluyen Windows 10 y versiones posteriores, iOS, Android y macOS.

2. **Unido a Azure AD.** Es el que se une mediante una cuenta de la organización, que luego se usa para iniciar sesión en el dispositivo. 

> Los dispositivos unidos a Azure AD suelen ser propiedad de la organización. Los sistemas operativos compatibles con dispositivos unidos a Azure AD incluyen Windows 10 o versiones posteriores (excepto Home Edition) y máquinas virtuales con Windows Server 2019 que se ejecutan en Azure.

3. **Dispositivos unidos a Azure AD híbrido.** Las organizaciones con implementaciones locales de Active Directory existentes se pueden beneficiar de algunas de las funcionalidades proporcionadas por Azure AD mediante la implementación de dispositivos unidos a Azure AD híbrido. 

> **Estos dispositivos están unidos a la instancia local de Active Directory y Azure AD exige que la cuenta de la organización inicie sesión en el dispositivo.**

El registro y la unión de dispositivos a Azure AD proporciona a los usuarios el inicio de sesión único (SSO) a los recursos en la nube. Además, los dispositivos que están unidos a Azure AD se benefician de la experiencia de inicio de sesión único en los recursos y aplicaciones que dependen de la instancia de Active Directory local.

---

