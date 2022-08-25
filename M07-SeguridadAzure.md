# Funcionalidades basicas de Azure.

*El perímetro de seguridad de red tradicional está cambiando a medida que más empresas se mueven o bien a un entorno de nube híbrida, donde algunos recursos se ubican localmente; y otros, en la nube; o bien a una solución de red totalmente basada en la nube. La protección de los recursos y datos de su organización es fundamental.*

Las amenazas pueden provenir de cualquier dirección: por ejemplo, un ataque por denegación de servicio a los servicios de su organización, o un pirata informático que intente acceder a la red probando a penetrar en el firewall. Azure ofrece una amplia gama de herramientas de seguridad configurables que se pueden personalizar para proporcionarle la seguridad y el control para satisfacer las necesidades de su organización.

![firewall](https://es.bestantiviruspro.org/wp-content/uploads/2019/06/1556-1-640x534.jpg)

En este módulo, explorará muchos servicios y características diferentes de Azure que pueden ayudar a proteger sus redes y recursos, incluidos la protección contra DDoS, Azure Firewall, los grupo de seguridad de red, etc. También conocerá las distintas maneras en que se usa el cifrado para proteger los datos.

---

## Proteccion contra DDoS.

> _Cualquier empresa, grande o pequeña, puede ser objeto de un grave ataque de red. La naturaleza de estos ataques podría ser para mostrar una postura o simplemente porque el atacante se había puesto un desafío._

### Ataques de denegación de servicio distribuido.

Basicmente, el objetivo **de un ataque de denegación de servicio distribuido (DDoS) es sobrecargar los recursos en las aplicaciones y servidores, lo que les deja sin responder o ralentiza a los usuarios auténticos. Un ataque DDoS normalmente se dirige a cualquier dispositivo de acceso público al que se pueda acceder a través de Internet.**

![DDoS](https://www.aratecnia.es/wp-content/uploads/2015/08/ataque-DDoS-seguridad-informatica.jpg)

Existen distintos tipos de ataques DDoS:

* Ataques volumétricos: Se tratan de ataques basados en volúmenes que inundan la red con tráfico aparentemente legítimo, sobrepasando el ancho de banda disponible. El tráfico legítimo no logra comunicarse. Estos tipos de ataques se miden en bits por segundo.

* Ataques de protocolo: Los ataques de protocolo representan un destino inaccesible al agotar los recursos del servidor con solicitudes de protocolo falsas que aprovechan los puntos débiles de los protocolos de nivel 3 (red) y nivel 4 (transporte). Estos tipos de ataques se miden normalmente en paquetes por segundo.

* Ataques de nivel de recurso (aplicación) : estos ataques van dirigidos a paquetes de aplicaciones web y su objetivo es interrumpir la transmisión de datos entre hosts.

---

## Azure DDoS Protection.

![adddos](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-basic-security-capabilities-azure/media/2-network-flow.png)

>> El servicio Azure DDoS Protection está diseñado para ayudar a proteger sus aplicaciones y servidores mediante el análisis del tráfico de red y el descarte de todo lo que parezca un ataque DDoS. **Azure DDoS Protection identifica el intento de un atacante de sobrecargar la red. Bloquea el tráfico del atacante, asegurándose de que no llegue a los recursos de Azure. El tráfico legítimo de los clientes sigue llegando a Azure sin ninguna interrupción del servicio.**

Azure DDoS Protection _usa la escala y la elasticidad de la red global de Microsoft_ para incorporar capacidad de mitigación de DDoS a cada región de Azure. Durante un ataque DDoS, Azure puede escalar las necesidades informáticas para satisfacer la demanda. Para administra el consumo de la nube, DDoS Protection se asegura de que la carga de red solo refleje el uso real de los clientes.

Dos niveles:

1. **Básico:** El nivel de servicio Básico está habilitado automáticamente para cada propiedad de Azure, sin costo adicional, _como parte de la plataforma Azure_. La supervisión continua de tráfico y la mitigación en tiempo real de ataques de nivel de red comunes ofrecen la misma defensa que usan los servicios en línea de Microsoft. La red global de Azure se usa para distribuir y mitigar el tráfico de ataques en las distintas regiones.

2. **Estándar:** _Este nivel de servicio Estándar ofrece funcionalidades adicionales de mitigación adaptadas específicamente a los recursos de Microsoft Azure Virtual Network._ 

DDoS Protection Estándar es fácil de habilitar y no requiere ningún cambio en la aplicación. Las directivas de protección se ajustan mediante algoritmos dedicados de supervisión del tráfico y aprendizaje automático. Las directivas se aplican a direcciones IP públicas asociadas a recursos implementados en redes virtuales, como Azure Load Balancer y Application Gateway. *El servicio Estándar de DDoS Protection tiene un cargo mensual fijo que incluye protección para 100 recursos. La protección de recursos adicionales se cobra mensualmente por cada recurso.*

---

## 🧱 Azure Firewall.

**Azure Firewall** es un servicio de seguridad de red administrado y basado en la nube que protege los recursos de redes virtuales (VNet) de Azure frente a los atacantes. **Puede implementar Azure Firewall en cualquier red virtual,** pero el mejor enfoque es usarlo en una red virtual centralizada. Todas las demás redes virtuales y locales se enrutarán a través de ella. La ventaja de este modelo es la capacidad de ejercer de forma centralizada el control del tráfico de red para todas las redes virtuales en diferentes suscripciones.

> Un firewall es un dispositivo de seguridad de la red que monitorea el tráfico de red —entrante y saliente— y decide si permite o bloquea tráfico específico en función de un conjunto definido de reglas de seguridad.

![firewall](https://erestecno.com/wp-content/uploads/2019/10/Firewall-inamsay-1468x734-1024x512.jpg)

Con Azure Firewall **puede escalar el uso verticalmente para acoger los flujos de tráfico de red cambiantes,** por lo que no es necesario elaborar un presupuesto para los picos de tráfico. El tráfico de red está sujeto a las reglas de firewall configuradas cuando se enruta al firewall, como la puerta de enlace predeterminada de la subred.

![fwall](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-basic-security-capabilities-azure/media/2-azure-firewall.png)

### Caracteristicas.

1. **Alta disponibilidad y zonas de disponibilidad integradas:** _La alta disponibilidad está integrada, por lo que no hay nada que configurar._ Además, Azure Firewall se puede configurar para abarcar varias zonas de disponibilidad y aumentar la disponibilidad.

2. **Filtrado a nivel de aplicación y de red:** Use la dirección IP, el puerto y el protocolo para admitir el filtrado de nombres de dominio completo para el tráfico HTTP(s) saliente y los controles de filtrado de red.

3. **SNAT de salida y DNAT de entrada para comunicación con recursos de Internet:** _traduce la dirección IP privada de los recursos de red a una dirección IP pública de Azure (traducción de direcciones de red de origen, SNAT) para identificar y permitir el tráfico procedente de la red virtual a destinos de Internet._ Del mismo modo, el tráfico entrante de Internet a la dirección IP pública del firewall se traduce (traducción de direcciones de red de destino o DNAT) y se filtra a las direcciones IP privadas de los recursos de la red virtual.

4. **Varias direcciones IP públicas:** Estas direcciones se pueden asociar a Azure Firewall.

5. **Inteligencia sobre amenazas:** El filtrado basado en inteligencia sobre amenazas puede habilitarse para que **el firewall alerte y deniegue el tráfico desde y hacia los dominios y las direcciones IP malintencionados conocidos.**

6. **Integración en Azure Monitor:** Se integra en Azure Monitor para habilitar la recopilación, el análisis y la acción en función de la telemetría de los registros de Azure Firewall.

---

## Web Application Firewall.

Como ya temnemos conocimiento, en la actualidad los sitios web son las que mas ciber ataques tienen malintencionados que aprovechan vulnerabilidades habitualmente conocidas. _Evitar dichos ataques en el código de la aplicación es todo un desafío. Puede requerir un mantenimiento riguroso, revisión y supervisión._El firewall de aplicaciones web (WAF) ofrece una protección centralizada de las aplicaciones web contra las vulnerabilidades de seguridad más habituales.

![azurefire](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-basic-security-capabilities-azure/media/2-web-app-firewall.png)

Un WAF centralizado ayuda a simplificar la administración de la seguridad, mejora el tiempo de respuesta ante una amenaza de seguridad y permite aplicar revisiones a una vulnerabilidad conocida en un lugar, en lugar de proteger cada aplicación web individual. Un WAF también proporciona a los administradores de la aplicación a un mejor control de la protección contra amenazas e intrusiones.

---

## Segmentacion de red.

**La segmentación consiste en dividir algo en partes más pequeñas.** Una organización, por ejemplo, suele estar formada por grupos empresariales más pequeños, como recursos humanos, ventas, atención al cliente, etc. En una oficina, es habitual que cada grupo empresarial tenga su propio espacio de oficina, mientras que los miembros del mismo grupo comparten una oficina. Esto permite que los miembros de un mismo grupo empresarial colaboren, al tiempo que se mantiene la separación de otros grupos para atender los requisitos de confidencialidad de cada empresa.

![segm](https://eontd.com/wp-content/uploads/2020/10/Segmentacion-de-Red-EON-1024x277.png)

> La segmentación de la red puede asegurar las interacciones entre los perímetros. Este enfoque puede reforzar la postura de seguridad de una organización, contener los riesgos en caso de infracción y evitar que los atacantes accedan a toda la carga de trabajo.

El mismo concepto se aplica a las redes informáticas de las empresas. Estas son las principales razones de la segmentación:

- La capacidad de agrupar recursos relacionados que forman parte de las operaciones de la carga de trabajo (o que la hacen posible).

- Aislamiento de recursos.

- Directivas de gobernanza establecidas por la organización.

> La segmentación de la red también es compatible con el modelo de Confianza cero y con un enfoque de seguridad por capas que forma parte de una estrategia de defensa en profundidad.

>**Asumir la vulneración es un principio del modelo de Confianza Cero, por lo que la capacidad de contener a un atacante es vital para proteger los sistemas de información. Cuando las cargas de trabajo (o partes de una carga de trabajo determinada) se colocan en segmentos separados, se puede controlar el tráfico desde y hacia esos segmentos para asegurar las vías de comunicación. Si un segmento se ve comprometido, podrá contener mejor el impacto y evitar que se extienda lateralmente por el resto de su red.**

### Azure Vital Network.

*Azure Virtual Network (VNet) es la pieza clave para la red privada de su organización en Azure. VNet es similar a una red tradicional que funcionaría en su propio centro de datos, pero aporta las ventajas adicionales de la infraestructura de Azure, como la escala, la disponibilidad y el aislamiento.*

Las VNets proporcionan una contención a nivel de red de los recursos sin que se permita el tráfico a través de las VNets o de entrada a la VNet, de forma predeterminada. La comunicación tiene que ser aprovisionada de forma explícita. Esto permite un mayor control sobre la forma en que los recursos de Azure en una VNet se comunican con otros recursos de Azure, Internet y las redes locales.

![vnet](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-basic-security-capabilities-azure/media/azure-virtual-networks.png)

> Azure VNet permite a las organizaciones **segmentar su red.** Las organizaciones pueden crear varias VNets por región y por suscripción, y se pueden crear varias redes más pequeñas (subredes) dentro de cada VNet.