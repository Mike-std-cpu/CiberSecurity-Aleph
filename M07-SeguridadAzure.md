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

