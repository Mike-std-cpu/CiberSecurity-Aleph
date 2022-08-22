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

## Control de acceso.

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