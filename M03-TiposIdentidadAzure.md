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

