# Describir las funcionalidades de autentificacion de Azure AD.

## Metodos de Autentificaci贸n.

Este modulo nos deja en claro la funcionalidad principal y caracteristicas que  una plataforma de identidades puede llegar hacer, tales como:

**Comprobar y Autentificar credenciales cuando un usuario inicia sesi贸n en un dispositivo, aplicacion o servicio.**

### 馃攽 Contrase帽as.

**Las contrase帽as son la forma m谩s com煤n de autenticaci贸n,** pero tienen muchos problemas, especialmente si se usan en la autenticaci贸n de un solo factor, donde solo se usa una forma de autenticaci贸n. Si son bastante f谩ciles de recordar, un hacker podr谩 vulnerarlas f谩cilmente. Las contrase帽as seguras que no son f谩ciles de atacar son dif铆ciles de recordar, y afectan a la productividad de los usuarios cuando las olvidan.

![password](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-authentication-capabilities/media/3-passwords-supplemented-replaced.png)

> El uso de contrase帽as debe complementarse o reemplazarse por m茅todos de autenticaci贸n m谩s seguros disponibles en Azure AD.

---

### 馃摬 Telefono.

Azure AD permite formas de autentificaci贸n basada en telefonos.

1. **Autenticaci贸n basada en SMS.** El servicio de mensajes cortos (SMS) usado en la mensajer铆a de texto del dispositivo m贸vil se puede usar como forma principal de autenticaci贸n. 

> Con el inicio de sesi贸n basado en SMS, los usuarios no necesitan conocer un nombre de usuario y una contrase帽a para acceder a las aplicaciones y servicios. En su lugar, el usuario escribe su n煤mero de tel茅fono m贸vil registrado, recibe un mensaje de texto con un c贸digo de verificaci贸n, y escribe el c贸digo en la interfaz de inicio de sesi贸n.

![sms](https://www.audienciaelectronica.net/wp-content/uploads/2018/07/Verificacion-2-pasos.png)

Los usuarios tambi茅n pueden optar por comprobar su identidad a trav茅s de la mensajer铆a de texto SMS en un tel茅fono m贸vil, como forma secundaria de autenticaci贸n durante el autoservicio de restablecimiento de contrase帽a (SSPR) o Azure AD Multi-Factor Authentication. 

>> Por ejemplo, los usuarios pueden complementar su contrase帽a mediante la mensajer铆a de texto SMS. Se env铆a un SMS al n煤mero de tel茅fono m贸vil con un c贸digo de verificaci贸n. Para completar el proceso de inicio de sesi贸n, el c贸digo de verificaci贸n entregado debe introducirse en la interfaz de inicio de sesi贸n.

2.** Comprobaci贸n por llamada de voz.** Los usuarios pueden usar llamadas de voz como forma secundaria de autenticaci贸n, para comprobar su identidad, durante el autoservicio de restablecimiento de contrase帽a (SSPR) o Azure AD Multi-Factor Authentication. Con la verificaci贸n por llamada telef贸nica, se hace una llamada de voz automatizada al n煤mero de tel茅fono registrado por el usuario. Para completar el proceso de inicio de sesi贸n, se le pide al usuario que presione # en el teclado. Las llamadas de voz no se admiten como una forma principal de autenticaci贸n en Azure AD.

---

### OATH.

OATH (Open Authentication)** es un est谩ndar abierto que especifica c贸mo se generan los c贸digos de contrase帽a de un solo uso y duraci贸n definida (TOTP)**. Los c贸digos de contrase帽a de un solo uso se pueden usar para autenticar a un usuario. Los TOTP de OATH se implementan mediante software o hardware para generar los c贸digos.

> _TOTP --> significa Contrase帽as de un solo uso basadas en el tiempo y es una forma com煤n de autenticaci贸n de dos factores (2FA). Las contrase帽as num茅ricas 煤nicas se generan con un algoritmo estandarizado que utiliza la hora actual como entrada._

![TOTP](https://twilio-cms-prod.s3.amazonaws.com/images/IMG_104859B58E5F-1.width-500.jpg)

Los tokens de software OATH suelen ser aplicaciones. Azure AD genera la clave secreta, o valor de inicializaci贸n, que se introduce en la aplicaci贸n y se usa para generar cada OTP.

**Los tokens de hardware OATH TOTP (compatibles con la versi贸n preliminar p煤blica) son dispositivos de hardware peque帽os que parecen un fob de clave que muestra un c贸digo que se actualiza cada 30 o 60 segundos.** Los tokens de hardware TOTP de OATH suelen incluir una clave secreta, o valor de inicializaci贸n, programada previamente en el token. Estas claves y otra informaci贸n espec铆fica de cada token deben introducirse en Azure AD y, a continuaci贸n, activarse para su uso por parte de los usuarios finales.

> Los tokens de hardware y software OATH solo se admiten como formas secundarias de autenticaci贸n en Azure AD para comprobar una identidad durante el autoservicio de restablecimiento de contrase帽a (SSPR) o Azure AD Multi-Factor Authentication.

---

### 馃敁 Autentificaci贸n sin contrase帽as.

En muchas organizaciones, el objetivo final es eliminar el uso de contrase帽as como parte de los eventos de inicio de sesi贸n. Cuando un usuario inicia sesi贸n con un m茅todo sin contrase帽a, las credenciales se proporcionan mediante el uso de m茅todos como la informaci贸n biom茅trica en Windows Hello para empresas o una clave de seguridad FIDO2. Un atacante no puede duplicar f谩cilmente estos m茅todos de autenticaci贸n.

**Azure AD ofrece formas de autenticaci贸n nativa sin contrase帽a con el fin de simplificar la experiencia de inicio de sesi贸n de los usuarios y reducir el riesgo de ataques.**

Windows hello es una nueva implementacion biometrico con el SO de microsoft, donde se empiexza a despegar y ofreciendo seguridad aparte, de la seguridad de 2 factores que ya se han mencionado antes.

#### Windows Hello.

Windows Hello para empresas reemplaza las contrase帽as con una autenticaci贸n de dos factores s贸lida en dispositivos. Esta autenticaci贸n en dos fases es una combinaci贸n de una clave o un certificado vinculado a un dispositivo y algo que la persona conoce (un PIN) o algo que la persona es (biometr铆a). La entrada de PIN y el gesto biom茅trico desencadenan el uso de la clave privada para firmar criptogr谩ficamente los datos que se env铆an al proveedor de identidades. El proveedor de identidades comprueba la identidad del usuario y autentica al usuario.

>> Windows Hello para empresas ayuda a protegerse contra el robo de credenciales, ya que un atacante debe tener tanto el dispositivo como la informaci贸n biom茅tr
ica o el PIN, lo que dificulta el acceso sin el conocimiento del empleado.

### FIDO2

Fast Identity Online (FIDO) **es un est谩ndar abierto para la autenticaci贸n sin contrase帽a. FIDO permite a los usuarios y a las organizaciones aprovechar el est谩ndar para iniciar sesi贸n en sus recursos mediante una clave de seguridad externa o una clave de plataforma integrada en un dispositivo, lo que elimina la necesidad de usar usuario y contrase帽a.**

>> **FIDO2 es el est谩ndar m谩s reciente que incorpora el est谩ndar de autenticaci贸n web (WebAuthn) y es compatible con Azure AD. Las claves de seguridad FIDO2 son un m茅todo de autenticaci贸n sin contrase帽a basado en est谩ndares que no permite la suplantaci贸n de identidad y que puede venir en cualquier factor de forma. Estas claves de seguridad FIDO2 suelen ser dispositivos USB, pero tambi茅n pueden ser dispositivos basados en Bluetooth o comunicaci贸n de campo cercano (NFC), que se usan para la transferencia de datos inal谩mbricas de corto alcance. Con un dispositivo de hardware que controla la autenticaci贸n, se aumenta la seguridad de una cuenta, ya que no hay ninguna contrase帽a que pueda quedar expuesta ni adivinarse.**

![fido2](https://www.ionos.mx/digitalguide/fileadmin/DigitalGuide/Schaubilder/fido2-es.png)

Con las claves de seguridad FIDO2, los usuarios pueden iniciar sesi贸n en dispositivos Windows 10 unidos a Azure AD o Azure AD h铆brido y lograr el inicio de sesi贸n 煤nico en sus recursos de nube y locales. Los usuarios tambi茅n pueden iniciar sesi贸n en exploradores compatibles.

---

### 馃殌 Aplicaci贸n Microsoft Authenticator.

Como m茅todo de autenticaci贸n sin contrase帽a, la aplicaci贸n Microsoft Authenticator se puede usar como forma principal de autenticaci贸n para iniciar sesi贸n en cualquier cuenta de Azure AD o como opci贸n de verificaci贸n adicional durante el autoservicio de restablecimiento de contrase帽a (SSPR) o Azure AD eventos de Multi-Factor Authentication.

![aunth](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-authentication-capabilities/media/authenticator-passwordless.png)

> - Para usar Microsoft Authenticator, un usuario debe descargar la aplicaci贸n de tel茅fono desde Microsoft Store y registrar su cuenta. Microsoft Authenticator est谩 disponible para Android e iOS.
> - Con la informaci贸n de inicio de sesi贸n, la aplicaci贸n Authenticator convierte cualquier tel茅fono Android o iOS en una credencial segura sin contrase帽a. Para iniciar sesi贸n en su cuenta de Azure AD, un usuario escribe su nombre de usuario, coincide con un n煤mero mostrado en la pantalla en el que se encuentra en su tel茅fono y, a continuaci贸n, usa su biom茅trica o PIN para confirmar.

![2](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-authentication-capabilities/media/3-microsoft-authenticator-app-approval-request.png)

Cuando un usuario elige Authenticator como m茅todo de autenticaci贸n secundario, para verificar su identidad, se env铆a una notificaci贸n push al tel茅fono o tableta. Si la notificaci贸n es leg铆tima, el usuario selecciona Aprobar; de lo contrario, selecciona Denegar.

--- 

## Autentificaci贸n multifactor (MFA) en Azure AD.

Esta parter del modulo, se definira la autentifiacion multifactor donde se requiere m谩s de una forma de comprobaci贸n para demostrar que una identidad es leg铆tima, como un dispositivo de confianza o una detecci贸n de huellas digitales. Esto implica que, aunque la contrase帽a de una identidad se haya puesto en peligro, un hacker no podr谩 acceder al recurso.

> La autenticaci贸n multifactor **mejora dr谩sticamente la seguridad de las identidades**, a la vez que sigue siendo simple para los usuarios. El factor de autenticaci贸n adicional debe ser algo dif铆cil de obtener o duplicar para un atacante.

El funcionamiento de la autenticaci贸n multifactor de Azure Active Directory solicita lo siguiente:

- 馃攽 **Algo que sabe:** normalmente una contrase帽a o un PIN y
- 馃摬 **Algo que tiene:** como un dispositivo de confianza que no se duplica f谩cilmente; por ejemplo, un tel茅fono o una clave de hardware, o
- 馃懆鈥嶐煉? **Algo que forma parte de usted:** informaci贸n biom茅trica como una huella digital o una detecci贸n de rostro.

Las solicitudes de comprobaci贸n de la autenticaci贸n multifactor est谩n configuradas para formar parte del evento de inicio de sesi贸n en Azure AD. Azure AD solicita y procesa autom谩ticamente la autenticaci贸n multifactor, sin realizar cambios en las aplicaciones o servicios. Cuando un usuario inicia sesi贸n, recibe una solicitud de autenticaci贸n multifactor y puede elegir una de las formas de verificaci贸n adicionales que haya registrado.

**Un administrador puede requerir ciertos m茅todos de comprobaci贸n, o el usuario puede acceder a la secci贸n Mi cuenta para editar o agregar m茅todos de comprobaci贸n.**

Las siguientes formas adicionales de verificaci贸n, se pueden usar con la autenticaci贸n multifactor de Azure AD:

- Aplicaci贸n Microsoft Authenticator
- Windows Hello para empresas
- Clave de seguridad FIDO2
- Token de hardware OATH (versi贸n preliminar)
- Token de software OATH
- sms
- Llamada de voz

![factor](https://docs.microsoft.com/es-es/learn/wwl-sci/explore-authentication-capabilities/media/2-microsoft-authenticator-app.png)

#### Valores predeterminados de seguridad y Autentificaci贸n multifactor.

**Son un conjunto de mecanismos de seguridad de identidad b谩sicos recomendados por Microsoft. Cuando est茅n habilitadas, estas recomendaciones se aplicar谩n autom谩ticamente en su organizaci贸n.** 

> El objetivo es asegurarse de que todas las organizaciones gocen de un nivel b谩sico de seguridad sin ning煤n costo adicional. Estos valores predeterminados habilitan algunas de las caracter铆sticas y controles de seguridad m谩s comunes, entre los que se incluyen los siguientes:

- Aplicar el registro de autenticaci贸n multifactor de Azure Active Directory para todos los usuarios.
- Forzar a los administradores a usar la autenticaci贸n multifactor.
- Requerir a todos los usuarios que realicen la autenticaci贸n multifactor cuando sea necesario.

--- 

## Autoservicio de restablecimiento de contrase帽as (SSPR) en Azure AD.

Se habla de que el SSPR es una caracteristica de productividad de Azure AD, donde permite a los usurios a cambiar o restablecer su contrase帽a, sin la necesidad de que tengan que intervenir los administradores o el departamento de soporte, evitando perdida de tiempo y productividad.

> Si la cuenta de un usuario est谩 bloqueada o se ha olvidado de la contrase帽a, puede seguir la indicaci贸n para restablecerla y volver al trabajo. Esta capacidad reduce las llamadas al departamento de soporte t茅cnico y la p茅rdida de productividad cuando un usuario no puede iniciar sesi贸n en su dispositivo o en una aplicaci贸n.

El autoservicio de restablecimiento de contrase帽a funciona en los siguientes escenarios:

- **Cambio de contrase帽a:** el usuario conoce la contrase帽a, pero quiere cambiarla por una nueva.
- **Restablecimiento de contrase帽a:** el usuario no puede iniciar sesi贸n, por ejemplo, cuando ha olvidado la contrase帽a, y quiere restablecerla.
- **Desbloqueo de cuenta:** el usuario no puede iniciar sesi贸n porque su cuenta est谩 bloqueada.

Para usar el autoservicio de restablecimiento de contrase帽a, los usuarios deben cumplir lo siguiente:

1. Tener asignada una licencia de Azure AD. Consulte la secci贸n M谩s informaci贸n de la unidad de resumen y recursos para obtener un v铆nculo a los requisitos de licencia para el autoservicio de restablecimiento de contrase帽a de Azure Active Directory.
2. Estar habilitados para SSPR por un administrador.
3. Estar registrado con los m茅todos de autenticaci贸n que quieren usar. Se recomiendan dos o m谩s m茅todos de autenticaci贸n en caso de que uno no est茅 disponible.

Est谩n disponibles los siguientes m茅todos de autenticaci贸n:

- Notificaci贸n en aplicaci贸n m贸vil
- C贸digo de aplicaci贸n m贸vil
- Email
- Tel茅fono m贸vil
- Tel茅fono del trabajo
- Preguntas de seguridad

> Cuando un usuario restablece su contrase帽a mediante el autoservicio de restablecimiento de contrase帽a, dicha contrase帽a tambi茅n puede reescribirse en una instancia de Active Directory local. La reescritura de contrase帽as permite a los usuarios usar sus credenciales actualizadas con las aplicaciones y dispositivos locales sin ninguna demora.

---

## Funcionalidades de administraci贸n y proteccion de contrase帽as de Azure AD.

El uso y administraci贸n de contrase帽as es una de las mejores ventajas de Azure AD, donde esta reduce el riesgo que los usuarios establezcan contrase帽as no seguras , esta detecta y bloquea las contrase帽as no seguras conocidas.

### 1. Lista global de contrase帽as prohibidas
Microsoft actualiza y aplica autom谩ticamente una lista global de contrase帽as prohibidas que incluye contrase帽as no seguras conocidas. Esta lista la mantiene el equipo de Azure AD Identity Protection, que analiza los datos de telemetr铆a de seguridad para buscar contrase帽as poco seguras o vulneradas. Algunos ejemplos de contrase帽as que podr铆an estar bloqueadas son P@$$w0rd o Passw0rd1 y todas sus variaciones.

Las variaciones se crean mediante un algoritmo que transpone may煤sculas y min煤sculas, as铆 como letras a n煤meros; por ejemplo, "1" a "l". Las variaciones de Password1 pueden incluir a Passw0rd1, Pass0rd1 y otras. A continuaci贸n, estas contrase帽as se comprueban y se agregan a la lista global de contrase帽as prohibidas y se ponen a disposici贸n de todos los usuarios de Azure AD. La lista global de contrase帽as prohibidas se aplica autom谩ticamente y no se puede deshabilitar.

> Si un usuario de Azure AD intenta usar como contrase帽a una de estas contrase帽as no seguras, recibir谩 una notificaci贸n para elegir otra m谩s segura. La lista global prohibida se crea a partir de ataques de difusi贸n de contrase帽as reales. Este enfoque mejora la seguridad y eficacia generales, y el algoritmo de validaci贸n de contrase帽as tambi茅n usa t茅cnicas inteligentes de coincidencia aproximada que se usan para buscar cadenas que coincidan aproximadamente con un patr贸n. Protecci贸n de contrase帽as de Azure AD detecta y bloquea de manera eficaz millones de las contrase帽as poco seguras m谩s comunes que se usan en su empresa.

### 2. Listas personalizadas de contrase帽as prohibidas
Los administradores tambi茅n pueden crear listas personalizadas de contrase帽as prohibidas para satisfacer necesidades espec铆ficas de seguridad empresarial. La lista personalizada de contrase帽as prohibidas impide el uso de contrase帽as como el nombre o la ubicaci贸n de la organizaci贸n. Las contrase帽as agregadas a la lista personalizada de contrase帽as prohibidas deben centrarse en t茅rminos espec铆ficos de la organizaci贸n, como:

- Nombres de marca
- Nombres de producto
- Ubicaciones, por ejemplo, la oficina central de la empresa
- T茅rminos internos espec铆ficos de la empresa
- Abreviaturas que tienen un significado espec铆fico en la empresa

> La lista personalizada de contrase帽as prohibidas se combina con la lista global de contrase帽as prohibidas para bloquear las variaciones de todas las contrase帽as.

Las listas de contrase帽as prohibidas son una caracter铆stica de Azure AD Premium 1 o 2.

### 3. Protecci贸n contra la difusi贸n de contrase帽as
Protecci贸n con contrase帽a de Azure AD le ayuda a defenderse contra los ataques de difusi贸n de contrase帽a. La mayor铆a de los ataques de difusi贸n de contrase帽as env铆an solo algunas de las contrase帽as menos seguras conocidas en cada una de las cuentas de una empresa. Esta t茅cnica permite al atacante buscar r谩pidamente una cuenta en peligro y evitar posibles umbrales de detecci贸n.

Protecci贸n con contrase帽a de Azure AD bloquea de forma eficaz todas las contrase帽as no seguras conocidas que se puedan usar en los ataques de difusi贸n de contrase帽a. Esta protecci贸n se basa en los datos de telemetr铆a de seguridad del mundo real que genera Azure AD, los cuales se usan para crear la lista global de contrase帽as prohibidas.

### 4. Seguridad h铆brida
Si busca seguridad h铆brida, los administradores pueden integrar la Protecci贸n de contrase帽as de Azure AD en un entorno de Active Directory local. Un componente instalado en el entorno local recibe la lista global de contrase帽as prohibidas y las directivas personalizadas de protecci贸n de contrase帽as de Azure AD. A continuaci贸n, los controladores de dominio las usan para procesar los eventos de cambio de contrase帽a. Este enfoque h铆brido garantiza que, siempre que un usuario cambie su contrase帽a, se aplique la Protecci贸n de contrase帽as de Azure AD.

Aunque la protecci贸n de contrase帽as mejora la seguridad de las contrase帽as, debe seguir usando las caracter铆sticas recomendadas, como la autenticaci贸n multifactor de Azure Active Directory. Las contrase帽as por s铆 solas, incluso las seguras, no lo proteger谩n tanto como varias capas de seguridad.