# Gobernanza de Identidades.

Como concepto principal para poder entender la gobernanza es que, **La gobernanza de identidades consiste en equilibrar la seguridad de identidades con la productividad de los usuarios de tal manera, que se puedan JUSTIFICAR Y AUDITAR** Como ya hemos manejado, Azure AD ofrece muchas funcionalidades de proteccion de gobernnaza de identidades:

- Privileged Identity Management (PIM).
- Identity Protection y los términos de uso.

## ✨ Gobernanza de identidades.

**Azure AD Identity Governance** ofrece a las organizaciones la posibilidad de realizar las siguientes tareas:

- Administrar el ciclo de vida de las identidades.
- Administrar el ciclo de vida de los accesos.
- Proteger el acceso con privilegios para la administración.

> Estas acciones se pueden completar para empleados, socios comerciales y proveedores en varios servicios y aplicaciones, tanto locales como en la nube.

Están diseñadas para ayudar a las organizaciones a abordar las siguientes cuatro preguntas clave:

> * ¿Qué usuarios deben tener acceso a qué recursos?
> * ¿Qué hacen esos usuarios con el acceso concedido?
> * ¿La organización cuenta con controles eficaces para administrar el acceso?
> * ¿Los auditores pueden comprobar qué controles funcionan?

---

## ✨ Ciclo de vida de las identidades.

Este punto es importante ya que la administración de ciclos de vida de identidades de los usuarios es el alama de la gobernanza de identidades.

> Por ejemplo, muchas organizaciones modelan el proceso de "unirse, trasladar y abandonar". Cuando una persona se une por primera vez a una organización, se crea una nueva identidad digital si aún no hay ninguna disponible. Cuando una persona se mueve entre límites organizativos, es posible que se deban agregar o eliminar autorizaciones de acceso adicionales a su identidad digital. Cuando una persona se va, es posible que sea necesario eliminar el acceso, y la identidad puede ya no ser necesaria, salvo con fines de auditoría.

![ciclo](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-identity-protection-governance-capabilities/media/2-identify-lifecycle-management.png)

**Azure AD Premium** ofrece integración con los sistemas de recursos humanos basados en la nube. Cuando se agrega un nuevo empleado a un sistema de recursos humanos, Azure AD puede crear la cuenta de usuario correspondiente. De manera similar, si las propiedades como, por ejemplo, el departamento o estado laboral, cambian en el sistema de RR. HH., la sincronización de esas actualizaciones con Azure AD garantiza la coherencia.

En general, la administración del ciclo de vida de una identidad consiste en actualizar el acceso que necesitan los usuarios, ya sea a través de la integración con un sistema de recursos humanos, o a través de aplicaciones de aprovisionamiento de usuarios.

## ✨ Ciclo de vida de los accesos.

El ciclo de vida de acceso es el proceso para administrar el acceso todo el tiempo que el usuario permanece en la organización. Los usuarios requieren distintos niveles de acceso desde el momento en el que se unen a una organización hasta que la abandonan. En varias fases intermedias, necesitarán derechos de acceso a distintos recursos en función de su rol y sus responsabilidades.

Las organizaciones pueden automatizar el proceso del ciclo de vida de los accesos con determinadas tecnologías, como los grupos dinámicos. Los grupos dinámicos permiten a los administradores crear reglas basadas en atributos para determinar la pertenencia a grupos. Cuando cambia cualquier atributo de un usuario o dispositivo, el sistema evalúa todas las reglas de grupos dinámicos de un directorio para ver si la modificación desencadenaría la adición o retirada de usuarios en un grupo. Si un usuario o dispositivo cumple una regla de un grupo, se agrega a este como miembro. Si ya no cumple la regla, se quita del grupo.

### Ciclo de vida a los accesos con privilegios.

La supervisión del acceso con **privilegios** _es una parte fundamental de la gobernanza de identidades. Cuando se asignan derechos administrativos a los empleados, proveedores y contratistas, debe haber un proceso de gobernanza debido a la posibilidad de un uso incorrecto._

**Azure AD Privileged Identity Management (PIM)** _ofrece controles adicionales que están adaptados para proteger los derechos de acceso._ PIM le ayuda a minimizar el número de personas que tienen acceso a los recursos a través de Azure AD, Azure y otras servicios en línea de Microsoft. PIM proporciona un conjunto completo de controles de gobernanza para ayudar a proteger los recursos de la empresa. PIM es una característica de Azure AD Premium P2.

---

## 🔓 Administración de derechos a las revisiones de acceso.

La administración de derechos es una característica de gobernanza de identidades que permite a las organizaciones administrar el ciclo de vida de las identidades y el acceso a escala. La administración de derechos automatiza los flujos de trabajo de las solicitudes de acceso, las asignaciones de acceso, las revisiones y la expiración.

Las empresas por frecuencia se topan con desafios de administrar el acceso de los empleados a recursos:

- Es posible que los usuarios no sepan qué acceso deben tener e, incluso si lo saben, pueden tener dificultades para encontrar los usuarios adecuados que lo aprueben.

- Una vez que los usuarios buscan y reciben acceso a un recurso, puede que conserven el acceso por más tiempo del necesario para los fines empresariales.

- Administración del acceso para usuarios externos.

### Revisiones de acceso de Azure AD.

Las revisiones de acceso de Azure Active Directory (AD) **permiten a las organizaciones administrar de forma eficiente la pertenencia a grupos, el acceso a las aplicaciones empresariales y la asignación de roles.** Las revisiones de acceso periódicas **garantizan que solo las personas adecuadas tienen acceso a los recursos.** Los derechos de acceso excesivos suponen un riesgo de seguridad conocido. Sin embargo, cuando las personas se transfieren de un equipo a otro, o cuando asumen o ceden responsabilidades, los derechos de acceso pueden ser difíciles de controlar.

Las revisiones de acceso son útiles cuando:

- Demasiados usuarios tienen roles con privilegios, como el administrador global.

- No es posible la automatización; por ejemplo, cuando los datos de recursos humanos no están en Azure AD.

- Quiere controlar el acceso a datos críticos para la empresa.

- Las directivas de gobernanza requieren revisiones periódicas de los permisos de acceso.

#### Usos:

* Las revisiones de acceso _se pueden crear a través de las revisiones de acceso de Azure AD o de Azure AD Privileged Identity Management (PIM)_. 
* Las revisiones de acceso _se pueden usar para revisar y administrar el acceso tanto para usuarios como para invitados._
* Cuando se crea una revisión de acceso, se puede configurar para que cada usuario revise su propio acceso, o para que uno o varios usuarios revisen el acceso de todos. Del mismo modo, se puede solicitar a todos los invitados que revisen su propio acceso, o que lo examinen uno o varios usuarios.

#### Condiciones de uso.

Los términos de uso de Azure AD permiten que se presente información a los usuarios antes de que tengan acceso a los datos o a una aplicación. Los términos de uso garantizan que los usuarios lean las declinaciones de responsabilidad pertinentes para conocer los requisitos legales o de cumplimiento.

Entre los casos de uso de ejemplo en los que es posible que los empleados o invitados deban aceptar condiciones de uso se incluyen los siguientes:

* Antes de acceder a datos confidenciales o a una aplicación.
* De forma periódica, a fin de recordarles las regulaciones.
* En función de los atributos del usuario, como los términos aplicables a roles concretos.
* Presentación de los términos a todos los usuarios de su organización.

> Los términos de uso se presentan en formato PDF, con contenido que crea el usuario, como un documento de contrato existente. Los términos de uso también se pueden presentar a los usuarios en dispositivos móviles.