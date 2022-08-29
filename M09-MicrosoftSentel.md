# Funcionalidad de Microsoft Sentinel.

La protección del patrimonio digital, los recursos, los activos y los datos de una organización ante las infracciones y los ataques a la seguridad es un reto continuo y creciente. En el mundo empresarial hay multitud de trabajadores remotos, lo que crea vulnerabilidades de seguridad que los cibercriminales pueden aprovechar.

Administracion de eventos e informacioón de seguridad (SEIM), nos ayuda a mitigar todo estos ataques como al igual elRespuesta automatizada de orquestación de seguridad (SOAR).

## SIEM.

Un sistema SIEM **es una herramienta que una organización utiliza para recopilar datos de todo el patrimonio, incluida la infraestructura, el software y los recursos.** 
Realiza: 

* Análisis.
* Busca correlaciones o anomalías.
* Genera alertas e incidencias.

## SOAR.

Un sistema SOAR **recibe alertas de muchos orígenes, como un sistema SIEM.** El sistema SOAR _desencadena entonces flujos de trabajo y procesos automatizados basados en acciones para ejecutar tareas de seguridad que mitiguen el problema._

A fin de proporcionar un enfoque completo para la seguridad, una organización debe usar una solución que adopte o combine las funcionalidades SIEM y SOAR.

---

## Microsoft Sentinel.

**¿Como microsoft Sentinel proporciona administración contra amenzas integrada?**

La administración efectiva del perímetro de seguridad de red de una organización requiere la combinación adecuada de herramientas y sistemas...

Es por eso que Microsoft Sentinel es una solución SIEM/SOAR escalable y nativa de la nube que ***ofrece análisis de seguridad inteligentes e inteligencia sobre amenazas en toda la empresa. Proporciona una única solución para la detección de alertas, la visibilidad de las amenazas, la búsqueda proactiva y la respuesta a las amenazas.**

#### Funcionalidad de extremo a extremo:

1. **Recopile** datos a escala de nube de todos los usuarios, dispositivos, aplicaciones y de toda la infraestructura, tanto en el entorno local como en diversas nubes.

2. **Detecte** amenazas que antes no se abarcaban y reduzca los falsos positivos mediante un análisis y una inteligencia de amenazas sin precedentes.

3. **Investigue** amenazas con inteligencia artificial (IA) y busque actividades sospechosas a gran escala, aprovechando el trabajo de ciberseguridad que ha realizado Microsoft durante décadas.

4. **Responda** a los incidentes con rapidez con la orquestación y la automatización de tareas comunes de seguridad integradas.

![MicrosoftSent](https://docs.microsoft.com/es-es/learn/wwl-sci/describe-security-capabilities-of-azure-sentinel/media/3-four-aspects-azure-sentinel.png)

### Sentinel y los datos.

> Para incorporar Microsoft Sentinel, primero debe conectarse a los orígenes de seguridad. Microsoft Sentinel incluye varios conectores para soluciones de Microsoft, que están disponibles inmediatamente y proporcionan integración en tiempo real. 

#### Workbooks.

Después de conectar los orígenes de datos a Microsoft Sentinel, **puede supervisar los datos mediante la integración de Microsoft Sentinel con los libros de Azure Monitor.** Verá un lienzo para el análisis de datos y la creación de informes visuales completos en Azure Portal. Mediante esta integración, Microsoft Sentinel **le permite crear libros personalizados de todos los datos.** También incluye plantillas de libro integradas que permiten obtener información rápidamente en los datos en cuanto se conecta con un origen de datos.

#### Analisis.

Microsoft Sentinel usa el análisis para poner en correlación las alertas con los incidentes. Los incidentes son grupos de alertas relacionadas que, juntas, crean una posible amenaza procesable que se puede investigar y resolver. Con el análisis en Microsoft Sentinel, puede utilizar las reglas de correlación integradas tal y como están, o bien usarlas como punto de partida para crear otras propias.

> También proporciona reglas de aprendizaje automático para asignar el comportamiento de red y buscar luego anomalías en los recursos.

![analisis](https://docs.microsoft.com/es-es/azure/sentinel/media/investigate-cases/incident-severity.png#lightbox)

#### Administracion de incidentes en MSentinel.

- La administración de incidentes permite administrar el ciclo de vida del incidente.
- Vea todas las alertas relacionadas que se agregan a un incidente.
- Puede evaluar las prioridades e investigar.
- Revise todas las entidades relacionadas del incidente y la información contextual adicional significativa para el proceso de evaluación de prioridades.
- Investigue las alertas y las entidades relacionadas para comprender el ámbito de la infracción.

#### Atomatización y orquestación de seguridad.

_Puede usar Microsoft Sentinel para automatizar algunas de las operaciones de seguridad y hacer que el centro de operaciones de seguridad (SOC) sea más productivo._ 

Microsoft Sentinel se integra con Azure Logic Apps, lo que permite crear flujos de trabajo automatizados, o cuadernos de estrategias, en respuesta a eventos. 

> _Un **cuaderno de estrategias** de seguridad es una colección de procedimientos que pueden ayudar a los ingenieros y analistas de SOC de todos los niveles a automatizar y simplificar las tareas y organizar una respuesta._

![admon](https://docs.microsoft.com/es-es/azure/sentinel/media/tutorial-respond-threats-playbook/logic-app.png)

#### Investigación.

Las herramientas de investigación profunda de Microsoft Sentinel están actualmente en versión preliminar y le ayudan a conocer el ámbito de una posible amenaza de seguridad y a encontrar la causa principa.

![inve](https://docs.microsoft.com/es-es/azure/sentinel/media/investigate-cases/map-timeline.png)

#### Busqueda.

Use las eficaces herramientas de búsqueda y consulta de Microsoft Sentinel, basadas en el marco MITRE (una base de datos global de tácticas y técnicas de adversarios), para buscar de forma proactiva amenazas de seguridad en todos los orígenes de datos de la organización, antes de que se desencadene una alerta. Una vez que ha descubierto qué consulta de búsqueda proporciona las conclusiones más valiosas sobre posibles ataques, también puede crear reglas de detección personalizadas basadas en la consulta y exponer esas conclusiones como alertas para los respondedores a los incidentes de seguridad.

#### Cuaderno.

Microsoft Sentinel admite cuadernos de Jupyter. Jupyter Notebook es una aplicación web de código abierto que le permite crear y compartir documentos que contienen código, ecuaciones, visualizaciones y texto narrativo dinámicos. Puede usar cuadernos de Jupyter en Microsoft Sentinel para ampliar el ámbito de lo que puede hacer con los datos de Microsoft Sentinel.

> Por ejemplo, realizar análisis que no están integrados en Microsoft Azure Sentinel, como algunas características de aprendizaje automático de Python, crear visualizaciones de datos que no están integradas en Microsoft Azure Sentinel, como escalas de tiempo personalizadas y árboles de proceso, o integrar orígenes de datos fuera de Microsoft Azure Sentinel, como un conjunto de datos local.

![notebooks](https://docs.microsoft.com/es-es/azure/sentinel/media/notebooks/sentinel-notebooks-on-machine-learning.png)

#### Comunidad.

La comunidad Microsoft Azure Sentinel es un recurso muy eficaz para la detección y la automatización de amenazas. Los analistas de seguridad de Microsoft crean y agregan constantemente nuevos libros, cuadernos de estrategias, consultas de búsqueda, etc., y los publican en la comunidad para que los pueda usar en el entorno.

---

## Costos.

* **Reservas de capacidad:** con las reservas de capacidad, se le factura una tarifa fija en función del nivel seleccionado, lo que permite un costo total predecible para Microsoft Sentinel.

*** Pago por uso:** con los precios de pago por uso, se le factura por gigabyte (GB) el volumen de datos ingeridos para el análisis en Microsoft Sentinel y almacenados en el área de trabajo de Log Analytics de Azure Monitor.
