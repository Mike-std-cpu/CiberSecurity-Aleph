# Describir las funcionalidades de administración de acceso de Azure AD

## Descripcion del acceso condicional en Azurer AD.

Se describe a este acceso condicional, es una caracteristica que proporciona una capa de seguridad **ADCIONAL** antes de permitir que los usuarios autenticados tengan acceso a los datos o a otros recursos. _Esto nos sirve a no tener que confiar en que un usuario que acceda, necesariamente deba ser quien dice ser_.

**El acceso condicional** se implementa a través de las directivas que se crean y administran en Azure AD. **_Una directiva de acceso condicional analiza las señales que incluyen el usuario, la ubicación, el dispositivo, la aplicación y el riesgo para automatizar las decisiones de autorización de acceso a los recursos (aplicaciones y datos)._**

![condicionalAccess](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-access-management-capabilities/media/2-conditional-access-policies.png)

> Es posible que una directiva de acceso condicional indique que si un usuario pertenece a un grupo determinado, se le pida que proporcione autenticación multifactor para iniciar sesión en una aplicación.

Las condiciones de accesos nos sirven para poder doblegar nuestra certeza de que el usuario pueda ser quien dice ser, como ya se menciono analizando:

- Señales de usuario.
- Ubicación.
- Dispositivo.

### 🟥 Señales de acceso condicional.

Segun la documentación, nos brinda señales comunes que pueden tener en cuenta el **Acceso condicional para tomar una desicion** sobre as directivas que pueden ser...

1. ** Pertenencia a grupo o usuario**. Las directivas se pueden dirigir a todos los usuarios, grupos específicos de usuarios, roles de directorio o usuarios invitados externos, lo que proporciona a los administradores un control específico sobre el acceso.

2. **Información de la ubicación con nombre.** La información de ubicación con nombre se puede crear con intervalos IP y usarse al tomar decisiones relacionadas con las directivas. Además, los administradores pueden optar por bloquear o permitir el tráfico desde el intervalo IP de todo un país o una región.

3. **Dispositivo.** Se pueden usar los usuarios con dispositivos de plataformas específicas o marcados con un estado específico.

4. **Aplicación.** Los usuarios que intentan acceder a aplicaciones específicas pueden desencadenar distintas directivas de acceso condicional.

5. **Detección de riesgo de inicio de sesión en tiempo real.** La integración de señales con Azure AD Identity Protection permite que las directivas de acceso condicional identifiquen el comportamiento de riesgo de inicio de sesión, la probabilidad de que un inicio de sesión determinado o una solicitud de autenticación, no estén autorizados por el propietario de la identidad. Luego, las directivas pueden obligar a los usuarios a realizar cambios de contraseña o a usar la autenticación multifactor para reducir su nivel de riesgo, o a bloquear su acceso hasta que algún administrador lleve a cabo una acción manual.

6. **Acciones o aplicaciones en la nube.** Las aplicaciones o acciones en la nube pueden incluir o excluir las aplicaciones en la nube o acciones del usuario que estarán sujetas a la directiva.

7. **Riesgo de usuario.** En el caso de los clientes con acceso a Identity Protection, el riesgo del usuario se puede evaluar como parte de una directiva de acceso condicional. Un riesgo de usuario representa la probabilidad de que una identidad o cuenta determinada esté en peligro. El riesgo de los usuarios se puede configurar para una probabilidad alta, media o baja.

---

## Nota.

> Al crear una directiva de acceso condicional, los administradores pueden determinar qué señales usar a través de asignaciones. La parte de asignaciones de la directiva controla el quién, el qué y el dónde de una directiva de acceso condicional. A todas las asignaciones se les asigna la operación lógica AND. Si tiene más de una asignación configurada, se deben satisfacer todas las asignaciones para desencadenar una directiva.

---

### Control de acceso.

Cuando se ha aplicado la directiva de acceso condicional, se toma una decisión informada sobre si se debe conceder acceso, bloquear el acceso o requerir una comprobación adicional. La decisión se conoce como la parte de controles de acceso de la directiva de acceso condicional y define cómo se aplica una directiva. Las decisiones comunes son las siguientes:

- Bloquear Acceso.

- Conceder Acceso.

- Se reqeurira que se cumplan una o más condiciones para conceder el Acceso:

    * Exigir la autenticación multifactor.
    * Requerir que el dispositivo esté marcado como compatible.
    * Requerir un dispositivo unido a Azure AD híbrido.
    * Requerir aplicación cliente aprobada.
    * Requerir la directiva de protección de aplicaciones.
    * Requerir cambio de contraseña.

    Es clave mencionar que **controlar el acceso del usuario** en función de controles de sesión para habilitar experiencias limitadas en aplicaciones en la nube determinadas. **Por ejemplo,** _Control de aplicaciones de acceso condicional usa las señales de aplicaciones de Microsoft Defender for Cloud para bloquear las funciones de descargar, cortar, copiar e imprimir documentos confidenciales, o bien para exigir el etiquetado de archivos confidenciales._ Otros controles de sesión incluyen la frecuencia de inicio de sesión y las restricciones aplicadas a la aplicación que, en el caso de las aplicaciones seleccionadas, usan la información del dispositivo para proporcionar a los usuarios una experiencia limitada o completa, según el estado del dispositivo.

    ---

 ## 👨‍💼📇 Roles de Azure AD y el control de Acceso basado en roles.

**_Los roles de Azure AD controlan los permisos para administrar los recursos de Azure AD. Por ejemplo, permitir la creación de cuentas de usuario o ver la información de facturación. Azure AD admite roles integrados y personalizados._**

> Se ha conciderado al control de acceso basado en roles **(RBAC)** Ya que los roles integrados y personalizados desde Azure AD son una forma de que los roles controlan el mismo accesoa los recurso en Azure AD. **Esto se denomina RBAC de Azure AD**

### Ventajas.

* Permitir que un usuario administre las máquinas virtuales de una suscripción y que otro usuario administre las redes virtuales
* Permitir que un grupo de DBA administre bases de datos SQL en una suscripción
* Permitir que un usuario administre todos los recursos de un grupo de recursos, como las máquinas virtuales, los sitios web y las subredes
* Permitir que una aplicación acceda a todos los recursos de un grupo de recursos.

### Solo se debe conceder el acceso que los usuarios necesitan

> *Es un procedimiento recomendado, y más seguro, para conceder a los usuarios el privilegio mínimo que necesitan para realizar su trabajo. Esto significa que si alguien administra principalmente usuarios, debe asignarle el rol de administrador de usuarios y no el de administrador global. Mediante la asignación de privilegios mínimos, se limitan los daños que podrían ocurrir con una cuenta en peligro.*

### Roles integrados.

En Azure AD hay muchos roles integrados, que son los que tienen un conjunto fijo de permisos de rol. Algunos de los roles integrados más comunes son los siguientes:

1. **Administrador global:** los usuarios con este rol tienen acceso a todas las características administrativas de Azure Active Directory. El usuario que se suscribe al inquilino de Azure Active Directory se convierte en administrador global de manera automática.
2. **Administrador de usuarios:** los usuarios con este rol pueden crear y administrar todos los aspectos de los usuarios y grupos. Además, este rol incluye la capacidad de administrar incidencias de soporte técnico y supervisar el estado del servicio.
3. **Administrador de facturación:** los usuarios que tienen este rol realizan compras, administra suscripciones e incidencias de soporte técnico y supervisan el estado del servicio.

Todos los roles integrados son agrupaciones preconfiguradas de permisos que se diseñaron para tareas específicas. El conjunto fijo de permisos incluidos en los roles integrados no se puede modificar.

### Roles Perzonalizados.

Los roles personalizados** proporcionan flexibilidad a la hora de conceder acceso.** Una definición de roles personalizada _es una colección de permisos que se seleccionan en una lista preestablecida._ La lista de permisos entre los que se puede elegir son los mismos que usan los roles integrados. La diferencia es que puede elegir qué permisos quiere incluir en un rol personalizado.

#### Pasos para la creación de roles perzonalizados.

La concesión de permisos mediante roles de Azure AD personalizados es un proceso de dos pasos. 

1. El primero implica la creación de una definición de rol personalizado, que consta de una colección de permisos que se agregan desde una lista preestablecida. 

2. Una vez que se crea la definición de rol personalizado, el segundo paso consiste en asignar ese rol a usuarios o grupos mediante la creación de una asignación de roles.

Una asignación de roles concede al usuario los permisos de una definición de roles según un ámbito específico. Un ámbito define el conjunto de recursos de Azure AD a los que tiene acceso el miembro del rol. Un rol personalizado se puede asignar en el ámbito de toda la organización, lo que significa que el miembro del rol tiene los permisos de rol sobre todos los recursos. También se puede asignar un rol personalizado en un ámbito de objeto. 

> Un ejemplo del ámbito de objeto sería una aplicación única. Se puede asignar el mismo rol a un usuario en todas las aplicaciones de la organización y, luego, a otro usuario que solo tenga un ámbito de la aplicación de informes de gastos de Contoso.

> Los roles personalizados requieren una licencia Azure AD Premium P1 o P2.

---

### Categorías de roles de Azure AD.

Para que sea práctico administrar las identidades en los servicios de Microsoft 365, Azure AD ha agregado roles integrados de servicios específicos, y cada uno concede acceso administrativo a un servicio de Microsoft 365. Esto significa que los roles integrados de Azure AD difieren en dónde se pueden usar. Hay tres categorías principales.

1. **Roles específicos de Azure AD:** estos roles conceden permisos para administrar recursos solo en Azure AD. 

> Por ejemplo, Administrador de usuarios, Administrador de aplicaciones, Administrador de grupos, todos conceden permisos para administrar recursos que residen en Azure AD.

2. **Roles específicos del servicio:** para los servicios de Microsoft 365 principales, Azure AD incluye roles específicos del servicio integrados que conceden permisos para administrar las características de ese servicio. 

> Por ejemplo, Azure AD incluye roles integrados para Administrador de Exchange, Administrador de Intune, Administrador de SharePoint y Administrador de Teams que pueden administrar características de sus servicios respectivos.

3. **Roles multiservicio:** hay algunos roles de Azure AD que abarcan varios servicios. 

> Por ejemplo, Azure AD tiene roles relacionados con la seguridad, como Administrador de seguridad, que conceden acceso a varios servicios de seguridad dentro de Microsoft 365. Del mismo modo, en el rol Administrador de cumplimiento puede administrar la configuración relacionada con el cumplimiento en el Centro de cumplimiento de Microsoft 365, Exchange, etc.

![categorias](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-access-management-capabilities/media/role-overlap-diagram-v2.png)

---

## Diferencias entre roles de RBAC de Azure y Azure AD.

* **RBAC de Azure AD:** los roles de Azure AD controlan el acceso a recursos de Azure AD como usuarios, grupos y aplicaciones.

* **RBAC de Azure:** los roles de Azure controlan el acceso a recursos de Azure como máquinas virtuales o almacenamiento mediante la administración de recursos de Azure.

![azureADAzure](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-access-management-capabilities/media/azure-roles-azure-ad-roles.png)

Como se ha descrito antes, los roles integrados y personalizados de Azure AD son una forma de RBAC por la que los roles de Azure AD controlan el acceso a los recursos de Azure AD. Esto se denomina RBAC de Azure AD. De la misma manera que los roles de Azure AD pueden controlar el acceso a los recursos de Azure AD, los roles de Azure también pueden controlar el acceso a los recursos de Azure. Esto se denomina RBAC de Azure. Aunque el concepto de RBAC se aplica tanto a RBAC de Azure AD como a RBAC de Azure, controlan aspectos diferentes.
