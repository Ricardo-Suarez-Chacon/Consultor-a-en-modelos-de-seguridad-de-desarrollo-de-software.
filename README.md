![alt text for screen readers](https://bienestarcorp.com/wp-content/uploads/2020/11/Politecnico-Grancolombiano-1.png "Text to show on mouseover")
# Primera entrega -Seguridad en el ciclo.

# Consultoría en modelos de seguridad de desarrollo de software.

**Leidy Johana Pulido Rodríguez Cod: 1911023821**

**Jorge Luis Álvarez Medina Cod: 1911023817**

**José Ricardo Suarez Chacón Cod: 1821026063**

**Robinson Daniel Clemente Córdoba Cod: 100231240**

**Carlos Andrés Minota Córdoba Cod: 100261147**

**Presentado a: Blanco Ignacio**

**SEGURIDAD EN EL CICLO DE DESARROLLO-[GRUPO B01]**

**Facultad de Ingeniería, Diseño e Innovación.**

**Ingeniería de Software.**

**Politécnico Gran Colombiano – noviembre de 2022.**

[1. Introducción. 3](about:blank#introducci%C3%B3n.)

[2. Objetivos. 4](about:blank#objetivos.)

[2.1 Objetivo General. 4](about:blank#objetivo-general.)

[2.2 Objetivos Específicos. 4](about:blank#objetivos-espec%C3%ADficos.)

[3. Estado del arte. 5](about:blank#estado-del-arte.)

[4. Modelos Existentes. 8](about:blank#modelos-existentes.)

[4.1 WASP CLASP. 8](about:blank#wasp-clasp.)

[4.2 OWASP SAMM 11](about:blank#owasp-samm)

[4.3 Nist 800-64. 23](about:blank#nist-800-64.)

[4.4 Microsoft security development lifecycle. 24](about:blank#microsoft-security-development-lifecycle.)

[6. Recomendación del modelo a implementar. 25](about:blank#recomendaci%C3%B3n-del-modelo-a-implementar.)

[7. Bibliografía. 26](about:blank#bibliograf%C3%ADa.)

# 1. Introducción.

Según la edición 2017 de Ciberamenazas y Tendencias (CCN-CERT IA-16/17)[1] Informe Anual del Centro Criptográfico Nacional del Gobierno de España y del Mando Conjunto Español del Ciberespacio, uno de los resultados fue clasificadas como pymes, se constató que aproximadamente el 82% de los ataques exitosos a la infraestructura informática que sufrió este negocio fueron fruto de actividades inocentes (es decir, causa desconocida) por parte de agentes internos (proveedores de servicios, empleados o clientes); Cuando aparece un ataque con éxito, esto indica que la vulnerabilidad fue reconocida por un comportamiento accidental o malicioso. Muchos de estos ataques están relacionados con defectos en los productos de software, en forma de errores de código fuente o errores en la lógica de la solución, que se traducen en una pérdida de confianza, operaciones dolorosas e incluso millones de euros en pérdidas para las organizaciones. [1].

El despliegue de software con defectos de diseño y/o codificación crea un gran número de vectores de ataque, dando lugar a una gran superficie de ataque para la empresa. En muchos casos, los errores en los sistemas de información pueden tener consecuencias muy graves para la fiabilidad global de la empresa, puesto que afectan a características como la tolerancia a errores, la fiabilidad, etc. Por las razones mencionadas anteriormente, es importante disponer de una metodología que proporcione un conjunto de pautas claras y específicas para desarrollar un proyecto de software de forma sistemática, didáctica y cuantificable que aporte lo necesario para garantizar la habilidad del desarrollo de productos de software. Alta calidad que satisface las necesidades del cliente y cumple con los requisitos de confidencialidad, integridad y disponibilidad.

# 2. Objetivos.

## 2.1 Objetivo General.

El objetivo de este documento es mostrar una visión general de cuatro modelos de seguridad en el ciclo de desarrollo de software y una guía que contiene lineamientos para la implementación del modelo OPENSAMM.

## 2.2 Objetivos Específicos.

- Presentar una visión general del modelo CLASP.
- Presentar una visión general del modelo OPENSAMM.
- Presentar una visión general del modelo NIST 800-64
- Presentar una visión general del modelo Microsoft security development lifecycle.

# 3. Estado del arte.

Este aspecto del presente documento trata el aspecto de los antecedentes, en donde se presentarán investigaciones de carácter internacional y nacional. Los cuales evidencian no solo la importancia de la seguridad en el ciclo de desarrollo de software (SDLC) sino también aspectos que la rodean en cuanto a su implementación.

***Internacionales:***

La tesis titulada “Seguridad de la información en el proceso de desarrollo de sistemas y del producto mediante la implementación de controles de seguridad basado en la norma ISO 27002:2015 en la empresa BITNESS CORP S.A.C.” elaborada por Alvarado y Sánchez (2020) en donde su objetivo es aumentar la seguridad en el desarrollo de sistemas y de su resultado en la organización BITNESS CORP. S.A.C. En cuanto a su metodología, esta investigación es no experimental de tipo longitudinal, ya que por una parte es experimental debido a que los datos se obtuvieron de la evaluación de la organización en su operación corriente y longitudinal debido a que la evaluación de a la organización se realizó en dos ocasiones, antes de la implementación de las medidas y después de estas. En lo concerniente a los resultados, estos se presentaron por medio de gráficas realizándose las comparaciones entre la primera evaluación y la segunda en donde se evalúa el cumplimiento de los distintos controles de seguridad definidos evidenciándose una mejora en dichos controles. Además, se presentó el aumento de la seguridad de la información de la empresa que pasó de un 48.95% a un 81.80% lo que permite concluir que la aplicación de los controles de seguridad en BITNESS CORP S.A.C permitió aumentar el nivel de seguridad tanto en el proceso de desarrollo de sistemas como en el producto resultante.

Por otro lado, el estudio cualitativo “Security in the Software Development Lifecycle” desarrollado por Assal y Chiasson (2018) el cual, a través de entrevistas a desarrolladores de software, se investigó sobre las prácticas de seguridad implementadas en la industria para cada etapa del ciclo del desarrollo del software. En donde se hallaron algunos factores que afectan la seguridad en el ciclo de desarrollo de software tales como la división de actividades, el grado de conocimiento en relación con seguridad en algunos equipos de desarrollo, la falta de la seguridad en la cultura de la organización, la disponibilidad de recursos, entre otros aspectos. Lo anterior permitió llegar a las siguientes conclusiones: que las prácticas de seguridad aplicadas en las organizaciones difieren notablemente de las mejores prácticas identificadas. Que las mejores practicas frecuentemente son ignoradas debido a que ir acorde a ellas aumentaría la carga de trabajo para el equipo de desarrollo. Que el problema no se limita al equipo de desarrollo sino también en la jerarquía de la organización y que los resultados obtenidos remarcan la necesidad de nuevas y ligeras prácticas de seguridad que se ajusten a realidad y a las presiones del desarrollo de software.

Por otra parte, Danish et al., (2020) en el artículo de investigación titulado “Importance of Secure Software Development Processes and Tools for Developers” por medio de una investigación en línea (online research) que tuvo como fuentes a IEEE, Google Scholar, Research Gate y ACM (Association for Computing Machinery) no solo para discutir sobre cuál es el método apropiado para construir software seguro, sino que también se presentaron tópicos importantes como el SDLC, las debilidades de seguridad del software, los problemas en las prácticas de código seguro al igual que sobre las prácticas de software seguro y también sobre un enfoque para resolver los problemas de seguridad. Dicho enfoque se basa en dos principales aspectos, el primero, que los desarrolladores deben capacitarse y educarse en relación con este aspecto y el segundo es que estos deben utilizar en la medida posible, herramientas de desarrollo que han demostrado ser seguras y que están disponibles. Por último, este artículo en su conclusión propone como solución el uso de herramientas para escanear la seguridad al igual que la capacitación de los interesados del proyecto de manera frecuente en conjunto con actualizaciones regulares al software implementado.

***Nacionales:***

Díaz y Castaño (2020) en el artículo nombrado “Componente de seguridad de la información en el Ciclo de Vida del Desarrollo de Software aplicado al procedimiento PR-M7-P5-033 en la Gobernación de Antioquia” con el objetivo verificar la seguridad del SDLC y considerar la implementación de seguridad en las etapas del desarrollo de software, lo anterior teniendo en cuenta el procedimiento PR-M7-P5-033 para evitar los ataques más frecuentes. En cuanto a su metodología, este artículo aplicó una investigación cualitativa con enfoque de revisión documental. Este articulo a través de su reflexión presenta algunas excusas que se suelen presentar en organizaciones en relación con la implementación de la seguridad en el SDLC, en donde la más escuchada es que “no hay tiempo para incluir la seguridad” las cuales son refutadas debidamente teniendo en cuenta la seguridad. Además de que se debe tener presente que es más provechoso y menos arriesgado prevenir o identificar un ataque en el desarrollo que aplicar la mitigación después de que una vulnerabilidad fue explotada, y es en este mismo apartado donde también se menciona los modelos de seguridad para el desarrollo de software seguro y de las ventajas de la implementación de estos. En cuanto a las conclusiones, el artículo recalca en la importancia de implementar normas y estándares en todo el ciclo de vida del desarrollo de software si se quiere asegurar el correcto funcionamiento de este. Por otra parte, Acosta (2020) en la monografía de grado titulada “El desarrollo de un software seguro la mejor opción para proteger la información” busca realizar una investigación que proporcione la importancia de la implementación de la seguridad en el desarrollo del software por medio de la metodología Security Requirements Engineering Process (SREP) y qué tanto impacta de manera positiva a la sociedad. En relación con su metodología, el estudio se identifica como una investigación descriptiva. En lo tocante a las conclusiones, texto menciona la importancia del desarrollo de software aplicando la metodología SREP la cual permite definir los requerimientos de seguridad que permitirán evaluar el ciclo de desarrollo en todas sus etapas, de tal forma que se puedan eliminar los riesgos que se relacionan con cada una de estas permitiendo que al final el cliente reciba un software con un nivel alto de seguridad.

Teniendo en cuenta los estudios presentados anteriormente, es claro que la implementación de la seguridad en el ciclo de desarrollo de software es un aspecto importante que debe ser considerado, y que los modelos de desarrollo seguro permiten alcanzar este objetivo. Es por esto por lo que las organizaciones desarrolladoras de software deben tener la disposición no solo de implementar tales modelos de tal forma que la seguridad se tenga en cuenta de manera plena en el desarrollo de sus proyectos sino también de hacer los ajustes desde la gerencia de modo que el software seguro pase a ser un aspecto del que se puede optar, a ser un aspecto completamente necesario.

# 4. Modelos Existentes.

## 4.1 WASP CLASP.

**OWASP CLASP, Comprehensive, Lightweight Application Security Process** (Proceso de seguridad de aplicaciones completo y ligero) es un conjunto de buenas prácticas, orientadas a las actividades y roles que formalizan las mejores prácticas para desarrollar software, ya sea desde cero o a partir de piezas existentes.

El proyecto CLASP está construido alrededor de 7 mejores prácticas de desarrollo y es aplicable a el ciclo completo de desarrollo, además se adapta a cualquier proceso de desarrollo para lo cual define roles a lo largo del S-SDLC Secure Software Development Life Cycle (Ciclo de vida del desarrollo de software seguro), 24 procesos basados en roles, permite un inicio pequeño e ir escalando de acuerdo con las necesidades.
<table>
  <tr>
   <td><strong>Mejores Prácticas</strong>
   </td>
   <td><strong>Actividades</strong>
   </td>
   <td><strong>Roles</strong>
   </td>
  </tr>
  <tr>
   <td>
<ol>

<li><strong> Programa de Sensibilización </strong>
</li>
</ol>
   </td>
   <td>Campañas de Sensibilización 
   </td>
   <td>
<ul>

<li>Gerente de proyecto
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td rowspan="4" >
<ol>

<li><strong>Realizar evaluaciones de las aplicaciones</strong>
</li>
</ol>
   </td>
   <td>Realización de análisis de seguridad de los requisitos y el diseño del sistema (modelado de amenazas)
   </td>
   <td>
<ul>

<li>Propietario: auditor de 
    seguridad
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Realización de una revisión de la seguridad a nivel de recursos fuente
   </td>
   <td>
<ul>

<li>Colaborador clave: ejecutor, diseñador

<li>Analista de pruebas
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>verificar los atributos de seguridad de los recursos
   </td>
   <td>
<ul>

<li>Tester
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Investigar y evaluar la postura de seguridad de las soluciones tecnológicas
   </td>
   <td>
<ul>

<li>Propietario: diseñador

<li>Colaborador clave: proveedor 
    de componentes
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td rowspan="7" >
<ol>

<li><strong>Captura de los requisitos </strong>
    <strong>de seguridad</strong>
</li>
</ol>
   </td>
   <td>Identifique la política de seguridad global
   </td>
   <td>
<ul>

<li>Redactor de requisitos
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Identificar recursos y límites 
<p>
seguros
   </td>
   <td>
<ul>

<li>Propietario: Arquitecto

<li>Colaborador clave: Redactor 
    de requisitos
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Identificar las funciones de los usuarios y las capacidades de los recursos
   </td>
   <td>
<ul>

<li>Propietario: Arquitecto

<li>Colaborador clave: Redactor de requisitos
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Especificar el entorno operativo
   </td>
   <td>
<ul>

<li>Propietario: Redactor de requisitos

<li>Colaborador clave: Arquitecto
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Detallar los casos de uso indebido
   </td>
   <td>
<ul>

<li>Propietario: Redactor de requisitos

<li>Colaborador clave: partes interesadas
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Identificación de la superficie de ataque
   </td>
   <td>
<ul>

<li>Diseñador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Documentar los requisitos de seguridad
   </td>
   <td>
<ul>

<li>Propietario: Redactor de requisitos

<li>Colaborador clave: Arquitecto
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td rowspan="6" >
<ol>

<li><strong>Implementar prácticas de desarrollo seguro.</strong>
</li>
</ol>
   </td>
   <td>Aplicar principios de seguridad 
<p>
al diseño.
   </td>
   <td>
<ul>

<li>Diseñador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Anotar los diseños de las clases
<p>
con propiedades de seguridad
   </td>
   <td>
<ul>

<li>Diseñador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Aplicar y elaborar políticas de 
<p>
recursos y tecnologías de 
<p>
seguridad
   </td>
   <td>
<ul>

<li>Desarrollador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Implementar contratos de interfaz
   </td>
   <td>
<ul>

<li>Desarrollador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Integrar el análisis de seguridad
<p>
en el proceso de gestión de 
<p>
fuentes
   </td>
   <td>
<ul>

<li>Integrador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Realizar la firma de código
   </td>
   <td>
<ul>

<li>Integrador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td rowspan="2" >
<ol>

<li><strong>Construir procedimientos de corrección de vulnerabilidades</strong>
</li>
</ol>
   </td>
   <td>Gestionar el proceso de
<p>
divulgación de problemas 
<p>
de seguridad
   </td>
   <td>
<ul>

<li>Propietario: Gerente de proyecto

<li>Colaborador clave: Diseñador
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Abordar los problemas de seguridad notificados
   </td>
   <td>
<ul>

<li>Propietario: Diseñador

<li>Reportero de fallas
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>
<ol>

<li><strong>Definir y monitorear las métricas</strong>
</li>
</ol>
   </td>
   <td>Monitorear las métricas de 
<p>
seguridad
   </td>
   <td>
<ul>

<li>Gerente de proyecto
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td rowspan="2" >
<ol>

<li><strong>Publicar directrices de seguridad operacional</strong>
</li>
</ol>
   </td>
   <td>Especificar la configuración de 
<p>
seguridad de la base de datos
   </td>
   <td>
<ul>

<li>Diseñador de la base de datos
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Construir la guía de seguridad 
<p>
operativa
   </td>
   <td>
<ul>

<li>Propietario: Integrador

<li>Colaborador clave: Diseñador, Arquitecto, Desarrollador
</li>
</ul>
   </td>
  </tr>
</table>



OWASP Open Web Application Security Project (Proyecto [abierto](https://es.wikipedia.org/wiki/C%C3%B3digo_abierto) de [seguridad](https://es.wikipedia.org/wiki/Seguridad_inform%C3%A1tica) de [aplicaciones web](https://es.wikipedia.org/wiki/Aplicaci%C3%B3n_web)) es una organización sin ánimo de lucro dedicada a determinar y combatir las causas que dan por resultado el software inseguro, para ello esta organización se encarga de crear metodologías, documentación, recomendaciones y herramientas de software libre en busca de cumplir su misión de combatir el software inseguro. Debido a esto dedicó años a crear y mantener el proyecto CLASP, sin embargo, con el paso del tiempo, emergió el proyecto OPENSAMM, el cual reemplaza a CLAMP y ya se encuentra en su versión 2.

## 4.2 [OWASP SAMM](https://owaspsamm.org/blog/2020/01/31/samm2-release/)

**[OWASP SAMM Software Assurance Maturity Model** **VERSIÓN 2](https://owaspsamm.org/blog/2020/01/31/samm2-release/),** es un marco de trabajo(Framework) que busca apoyar a las organizaciones a evaluar, formular e implementar, a través de un modelo de autoevaluación, una estrategia para la seguridad del software que se pueda integrar en su actual ciclo de vida de desarrollo de software.

*“La misión del OWASP Software Assurance Maturity Model (SAMM) es ser el principal modelo de madurez para el aseguramiento del software que proporciona una manera eficaz y medible para todo tipo de organizaciones para analizar y mejorar su postura de seguridad del software. OWASP SAMM soporta el ciclo de vida completo del software, incluyendo el desarrollo y la adquisición, y es agnóstico a la tecnología y al proceso. Está construido intencionalmente para ser evolutivo y orientado al riesgo por naturaleza.*

*El modelo original (v1.0) fue escrito por Pravir Chandra y data de 2009. Durante los últimos 10 años, ha demostrado ser un modelo ampliamente distribuido y eficaz para mejorar las prácticas de software seguro en diferentes tipos de organizaciones de todo el mundo. La comunidad ha contribuido con traducciones y herramientas de apoyo para facilitar su adopción y alineación. Con la versión 2.0, mejoramos aún más el modelo para hacer frente a algunas de sus limitaciones actuales.” SAMM resumen del modelo citado de https://owaspsamm.org/model/*

SAMM v2 aprovecha las décadas de experiencia de la organización OWASP y propone una completa guía para implementar S-SDLC Ciclo de vida del desarrollo de software seguro, y para ello pone a disposición de la comunidad los siguientes componentes:

- Visión general e introducción al modelo SAMM.
- Guía de inicio rápido con diferentes pasos para mejorar las prácticas de software seguro
- Un set de herramientas SAMM para realizar evaluaciones SAMM y crear hojas de ruta SAMM
- Herramienta para comparar su madurez y progreso con otras organizaciones y equipos similares

El modelo SAMM V2 Propone 5 ejes fundamentales para lograr sus objetivos:

- Gobernanza
- Diseño
- Implementación
- Verificación
- Operaciones

Cada uno de estos ejes fundamentales posee tres temas principales y cada tema es abordado desde dos tipos de acciones a realizar, según el tipo de actores que interactúan con los temas y el nivel de madurez del proceso en la organización.

A continuación, mostramos 15 tablas de resumen para dar un primer acercamiento al tema, estas están divididas en tres tablas para cada uno de los ejes principales.
## Gobernanza


<table>
  <tr>
   <td colspan="4" >
<ol>

<li>Gobernanza
</li>
</ol>
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    1.1 Métricas y estrategia
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Crear y promocionar
   </td>
   <td>Medir y mejorar
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Identificar los objetivos y los medios para medir la eficacia del programa de seguridad.
   </td>
   <td>Identificar los impulsores de la organización en relación con la tolerancia al riesgo de la organización.
   </td>
   <td>Definir métricas que permitan conocer la eficacia y eficiencia del Programa de Seguridad de Aplicaciones.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Establecer una hoja de ruta estratégica unificada para la seguridad del software dentro de la organización.
   </td>
   <td>Publicar una estrategia unificada para la seguridad de las aplicaciones.
   </td>
   <td>Establecer objetivos y KPI para medir la eficacia del programa.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Alinear los esfuerzos de seguridad con los indicadores organizacionales relevantes y los valores de los activos.
   </td>
   <td>Alinear el programa de seguridad de las aplicaciones para apoyar el crecimiento de la organización.
   </td>
   <td>Influir en la estrategia en función de las métricas y las necesidades de la organización.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    1. Gobernanza
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    1.2 Política y cumplimiento
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Política y normas
   </td>
   <td>Gestión del cumplimiento de las normas
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Identificar y documentar los impulsores de la gobernanza y el cumplimiento relevantes para la organización.
   </td>
   <td>Determinar una línea de base de seguridad que represente las políticas y normas de la organización.
   </td>
   <td>Identificar los impulsores y los requisitos de cumplimiento de terceros y asignarlos a las políticas y normas existentes.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Establecer una línea de base de seguridad y cumplimiento específica para la aplicación.
   </td>
   <td>Desarrollar los requisitos de seguridad aplicables a todas las aplicaciones.
   </td>
   <td>Publicar los requisitos de aplicación específicos de la conformidad y las orientaciones sobre las pruebas.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Medir el cumplimiento de políticas, normas y requisitos de terceros.
   </td>
   <td>Medir e informar sobre el estado de cumplimiento de las políticas y normas de cada aplicación.
   </td>
   <td>Medir e informar sobre el cumplimiento de la aplicación individual con los requisitos de terceros.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    1. Gobernanza
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    1.3 Educación y Orientación
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Formación y sensibilización
   </td>
   <td>Organización y cultura
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Ofrecer al personal acceso a los recursos en torno a los temas de desarrollo e implantación seguros.
   </td>
   <td>Impartir formación sobre seguridad a todo el personal que participa en el desarrollo de software
   </td>
   <td>Identificar un "Campeón de Seguridad" dentro de cada equipo de desarrollo.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Educar a todo el personal en el ciclo de vida del software con tecnología y orientación específica para cada función sobre el desarrollo seguro.
   </td>
   <td>Ofrecer orientación tecnológica y específica para cada función, incluidos los matices de seguridad de cada idioma y plataforma
   </td>
   <td>Desarrollar un centro de excelencia de software seguro que promueva el liderazgo de pensamiento entre desarrolladores y arquitectos.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Desarrollar programas de formación internos facilitados por los desarrolladores de los diferentes equipos.
   </td>
   <td>Orientación interna estandarizada en torno a las normas de desarrollo de software seguro de la organización.
   </td>
   <td>Construir una comunidad de software seguro que incluya a todas las personas de la organización implicadas en la seguridad del software.
   </td>
  </tr>
</table>





## Diseño


<table>
  <tr>
   <td colspan="4" >
<ol>

<li>Diseño
</li>
</ol>
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    2.1 Evaluación de amenazas
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Perfil de riesgo de las aplicaciones
   </td>
   <td><a href="https://owaspsamm.org/model/design/threat-assessment/stream-b">Threat Modeling</a>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Identificación de las amenazas de alto nivel para la organización y los proyectos individuales.
   </td>
   <td>Se realiza una evaluación básica del riesgo de la aplicación para comprender la probabilidad y el impacto de un ataque.
   </td>
   <td>Realice el mejor esfuerzo, el modelado de amenazas basado en el riesgo utilizando la lluvia de ideas y los diagramas existentes con listas de control de amenazas simples.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Estandarización y análisis en toda la empresa de las amenazas relacionadas con el software dentro de la organización.
   </td>
   <td>Comprender el riesgo de todas las aplicaciones de la organización centralizando el inventario de perfiles de riesgo para las partes interesadas.
   </td>
   <td>Estandarizar la formación, los procesos y las herramientas de modelado de amenazas para que se extiendan a toda la organización.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Mejora proactiva de la cobertura de amenazas en toda la organización.
   </td>
   <td>Revisar periódicamente los perfiles de riesgo de las aplicaciones a intervalos regulares para garantizar la exactitud y reflejar el estado actual.
   </td>
   <td>Optimización y automatización continua de su metodología de modelado de amenazas.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    2. Diseño
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    2.2 Requisitos de seguridad
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Requisitos de software
   </td>
   <td>Seguridad de proveedores
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Considerar la seguridad explícitamente durante el proceso de requisitos del software.
   </td>
   <td>Los objetivos de seguridad de alto nivel de la aplicación se asignan a los requisitos funcionales.
   </td>
   <td>Evaluar al proveedor en función de los requisitos de seguridad de la organización.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Aumentar la granularidad de los requisitos de seguridad derivados de la lógica empresarial y los riesgos conocidos.
   </td>
   <td>Los requisitos de seguridad estructurados están disponibles y son utilizados por los equipos de desarrolladores.
   </td>
   <td>Incorporar la seguridad en los acuerdos con los proveedores para garantizar el cumplimiento de los requisitos de la organización.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Establecer un proceso de requisitos de seguridad para todos los proyectos de software y las dependencias de terceros.
   </td>
   <td>Construir un marco de requisitos para que los equipos de productos lo utilicen.
   </td>
   <td>Garantizar una cobertura de seguridad adecuada para los proveedores externos proporcionando objetivos claros.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    2 . Diseño
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    2.3 Arquitectura de la seguridad
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>
    Diseño de la arquitectura
   </td>
   <td>Gestión de la 
<p>
tecnología
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Incorporar la consideración de la orientación proactiva de la seguridad en el proceso de diseño del software.
   </td>
   <td>Los equipos reciben formación sobre el uso de los principios básicos de seguridad durante el diseño
   </td>
   <td>Determinar las tecnologías, los frameworks y las integraciones dentro de la solución global para identificar el riesgo.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Dirigir el proceso de diseño de software hacia servicios seguros conocidos y diseños seguros por defecto.
   </td>
   <td>Establecer patrones de diseño y soluciones de seguridad comunes para su adopción.
   </td>
   <td>Estandarizar las tecnologías y los frameworks que se utilizarán en las diferentes aplicaciones
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Controlar formalmente el proceso de diseño de software y validar la utilización de componentes seguros.
   </td>
   <td>Las arquitecturas de referencia se utilizan y se evalúan continuamente para su adopción y adecuación.
   </td>
   <td>Implementar el uso de tecnologías estándar en todo el desarrollo de software.
   </td>
  </tr>
</table>





## Implementación


<table>
  <tr>
   <td colspan="4" >
<ol>

<li>Implementación
</li>
</ol>
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    3.1 Desarrollo Seguro
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Proceso de desarrollo
   </td>
   <td>Dependencias de software
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>El proceso de desarrollo es repetible y consistente.
   </td>
   <td>Crear una definición formal del proceso de desarrollo para que sea coherente y repetible.
   </td>
   <td>Cree informes con la lista de componentes de sus aplicaciones y analícelos de forma oportuna.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>El proceso de desarrollo está optimizado y totalmente integrado en el flujo de trabajo.
   </td>
   <td>Automatice su proceso de desarrollo y asegure las herramientas utilizadas. Añada comprobaciones de seguridad en el proceso de desarrollo.
   </td>
   <td>Evalúe las dependencias utilizadas y garantice una reacción oportuna ante situaciones que supongan un riesgo para sus aplicaciones.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>El proceso de desarrollo ayuda a evitar que los defectos conocidos entren en el entorno de producción.
   </td>
   <td>Defina las comprobaciones de seguridad obligatorias en el proceso de construcción y garantice que no se desarrollen productos no aptos.
   </td>
   <td>Analizar los problemas de seguridad de las dependencias utilizadas al igual que la seguridad de su propio código.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    3. Implementación
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    3.2 Despliegue Seguro
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Proceso de despliegue
   </td>
   <td>Gestión del secreto
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Los procesos de implantación están totalmente documentados.
   </td>
   <td>Formalizar el proceso de despliegue y asegurar las herramientas y procesos utilizados.
   </td>
   <td>Introduzca medidas básicas de protección para limitar el acceso a sus secretos de producción.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Los procesos de despliegue incluyen hitos de verificación de la seguridad.
   </td>
   <td>Automatice el proceso de despliegue en todas las etapas e introduzca pruebas de verificación de seguridad razonables.
   </td>
   <td>Inyectar secretos dinámicamente durante el proceso de despliegue desde depósitos protegidos y auditar todos los accesos humanos a los mismos.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>El proceso de despliegue está totalmente automatizado e incorpora la verificación automática de todos los hitos críticos.
   </td>
   <td>Verifique automáticamente la integridad de todo el software desplegado, independientemente de si está desarrollado interna o externamente.
   </td>
   <td>Mejore el ciclo de vida de los secretos de la aplicación generandolos regularmente y garantizando su uso adecuado.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    3. Implementación
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    3.3 Gestión de los defectos
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Seguimiento de defectos
   </td>
   <td>Métrica y retroalimentación
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Todos los defectos se rastrean dentro de cada proyecto.
   </td>
   <td>Introducir un seguimiento estructurado de los defectos de seguridad y tomar decisiones informadas basadas en esta información.
   </td>
   <td>Repase periódicamente los defectos de seguridad registrados anteriormente y obtenga ganancias rápidas a partir de las métricas básicas.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>El seguimiento de los defectos se utiliza para influir en el proceso de implantación.
   </td>
   <td>Califique todos los defectos de seguridad en toda la organización de forma coherente y definir acuerdos de nivel de servicio para determinadas clases de gravedad.
   </td>
   <td>Recopilar métricas estandarizadas de gestión de defectos y utilizarlas también para priorizar las iniciativas impulsadas de forma centralizada.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>El seguimiento de los defectos en múltiples componentes se utiliza para ayudar a reducir el número de nuevos defectos.
   </td>
   <td>Haga cumplir los acuerdos de nivel de servicio predefinidos e integre su sistema de gestión de defectos con otras herramientas pertinentes.
   </td>
   <td>Mejore continuamente sus métricas de gestión de defectos de seguridad y correlaciónelas con otras fuentes.
   </td>
  </tr>
</table>





## Verificación


<table>
  <tr>
   <td colspan="4" >
<ol>

<li>Verificación
</li>
</ol>
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    4.1 Evaluación de la arquitectura
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Validación de la arquitectura
   </td>
   <td>Armonización de la arquitectura
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Revisar la arquitectura para asegurarse de que existen mitigaciones de referencia para los riesgos típicos.
   </td>
   <td>Identificar los componentes de la arquitectura de la aplicación y de la infraestructura y revisarlos para la provisión de seguridad básica
   </td>
   <td>Revisión ad hoc de la arquitectura en busca de amenazas de seguridad no mitigadas.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Revisar la provisión completa de mecanismos de seguridad en la arquitectura.
   </td>
   <td>Validar los mecanismos de seguridad de la arquitectura
   </td>
   <td>Analizar la arquitectura en busca de amenazas conocidas.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Analizar la arquitectura en busca de amenazas conocidas.	Revisar la efectividad de la arquitectura y retroalimentar los resultados para mejorar la arquitectura de seguridad.
   </td>
   <td>Revisión de la eficacia de los componentes de la arquitectura
   </td>
   <td>Alimentar los resultados de la revisión de la arquitectura con la arquitectura empresarial, los principios y patrones de diseño de la organización, las soluciones de seguridad y las arquitecturas de referencia.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    4. Verificación
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    4.2 Pruebas basadas en requisitos
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Control de verificación
   </td>
   <td>Pruebas de uso indebido/abuso
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Encontrar oportunamente vulnerabilidades básicas y otros problemas de seguridad.
   </td>
   <td>Prueba de los controles de seguridad del software
   </td>
   <td>Realización de pruebas de seguridad difusas
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Realice una revisión de la implementación para descubrir los riesgos específicos de la aplicación frente a los requisitos de seguridad.
   </td>
   <td>Elaborar casos de prueba a partir de los requisitos de seguridad conocidos
   </td>
   <td>Crear y probar los casos de abuso y la prueba de defectos de la lógica empresarial
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Mantener el nivel de seguridad de la aplicación después de las correcciones de errores, los cambios o durante el mantenimiento.
   </td>
   <td>Realizar pruebas de regresión (con pruebas unitarias de seguridad)
   </td>
   <td>Pruebas de denegación de servicio y de estrés de seguridad
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    4. Verificación
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    4.3 Pruebas de seguridad
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Escalabilidad
   </td>
   <td>Entendimiento Profundo
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Realizar pruebas de seguridad (tanto manuales como basadas en herramientas) para descubrir defectos de seguridad.
   </td>
   <td>Utilizar herramientas de pruebas de seguridad automatizadas
   </td>
   <td>Realizar pruebas de seguridad manuales de los componentes de alto riesgo
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Haga que las pruebas de seguridad durante el desarrollo sean más completas y eficientes mediante la automatización complementada con pruebas de penetración de seguridad manuales regulares.
   </td>
   <td>Utilizar la automatización de las pruebas de seguridad específicas para la aplicación
   </td>
   <td>Llevar a cabo pruebas de penetración manuales
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Incorporar las pruebas de seguridad como parte de los procesos de desarrollo e implantación.
   </td>
   <td>Integrar las pruebas de seguridad automatizadas en el proceso de creación y despliegue
   </td>
   <td>Integrar las pruebas de seguridad en el proceso de desarrollo
   </td>
  </tr>
</table>





## Operaciones


<table>
  <tr>
   <td colspan="4" >
<ol>

<li>Operaciones
</li>
</ol>
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    5.1 Gestión de incidentes
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Detección de Incidentes
   </td>
   <td>Respuesta a incidentes
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Máximo esfuerzo en la detección y tratamiento de incidentes 
   </td>
   <td>Utilice y haga su mejor esfuerzo en analizar los datos de registro disponibles para realizar la detección de posibles incidentes de seguridad.
   </td>
   <td>Identificar las funciones y responsabilidades para la respuesta a incidentes.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Establecer un proceso formal de gestión de incidentes
   </td>
   <td>Seguir un proceso establecido y bien documentado para la detección de incidentes, con énfasis en la evaluación automatizada de los registros.
   </td>
   <td>Establezca un proceso formal de respuesta a incidentes y asegúrese de que el personal está debidamente formado para desempeñar sus funciones.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Gestión de incidencias 
<p>
madura
   </td>
   <td>Utilizar un proceso gestionado de forma proactiva para la detección de incidentes.
   </td>
   <td>Cuente con un equipo de respuesta a incidentes dedicado y bien formado.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    5. Operaciones
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    5.2 Gestión del entorno
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Refuerzo de la configuración
   </td>
   <td>Parches y actualizaciones
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Realizar el mejor esfuerzo en parcheo y robustez
   </td>
   <td>Realizar el mejor esfuerzo de robustecimiento de las configuraciones, basándose en la información disponible.
   </td>
   <td>Realice el mejor esfuerzo de parcheo de los componentes del sistema y de las aplicaciones.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Estructurar los procesos con las directrices establecidas
   </td>
   <td>Realice un robustecimiento coherente de las configuraciones, siguiendo las directrices y las orientaciones establecidas.
   </td>
   <td>Realizar parches regulares de los componentes del sistema y de las aplicaciones, en toda la pila. Garantizar la entrega puntual de los parches a los clientes.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Cumplimiento de la mejora continua del proceso
   </td>
   <td>Supervisar activamente las configuraciones para comprobar que se ajustan a las directrices y tratar las incidencias detectadas como defectos de seguridad.
   </td>
   <td>Supervisar activamente el estado de las actualizaciones y gestionar los parches que faltan como defectos de seguridad. Consultar de forma proactiva la información sobre vulnerabilidades y actualizaciones de los componentes.
   </td>
  </tr>
</table>





<table>
  <tr>
   <td colspan="4" >
    5. Operaciones
   </td>
  </tr>
  <tr>
   <td colspan="4" >
    5.3 Gestión operativa
   </td>
  </tr>
  <tr>
   <td>Madurez
   </td>
   <td>Objetivo
   </td>
   <td>Protección de datos
   </td>
   <td>Cierre del sistema / Gestión del legado
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>Prácticas Fundamentales
   </td>
   <td>Aplicar prácticas básicas de protección de datos
   </td>
   <td>Desactivar las aplicaciones y servicios no utilizados según se identifique. Gestionar individualmente las actualizaciones/migraciones de los clientes.
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>Procesos gestionados y con capacidad de respuesta
   </td>
   <td>Desarrollar un catálogo de datos y establecer una política de protección de datos.
   </td>
   <td>Desarrollar procesos de cierre repetibles para los sistemas/servicios no utilizados y para la migración de las dependencias heredadas. Gestionar las hojas de ruta de migración del legado para los clientes.
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>Monitoreo Activo y respuesta
   </td>
   <td>Automatizar la detección del incumplimiento de la política y auditar periódicamente su cumplimiento. Revisar y actualizar periódicamente el catálogo de datos y la política de protección de datos.
   </td>
   <td>Gestionar de forma proactiva las hojas de ruta de migración, tanto para las dependencias de fin de vida útil no soportadas, como para las versiones heredadas del software entregado.
   </td>
  </tr>
</table>

## 4.3 Nist 800-64.

Considerar la seguridad en el ciclo de vida del desarrollo del sistema es esencial para implementar e integrar una estrategia integral para administrar el riesgo para todos los activos de tecnología de la información en una organización. La publicación especial (SP) 800-64 del Instituto Nacional de Estándares y Tecnología (NIST) tiene como objetivo ayudar a las agencias del gobierno federal a integrar actividades de seguridad esenciales en sus pautas establecidas del ciclo de vida del desarrollo del sistema.

Nos ayuda a la caracterización del sistema, identificando amenazas, vulnerabilidades, control de amenazas, determinación de los riesgos, análisis de impacto, determinación de riesgo, recomendaciones de control e implementación o documentación.

Según Zambrano (s.f), las 5 fases de NIST 800-64 son:

Iniciación:

- Planear el proyecto
- Evaluación de impacto al negocio e impacto a la privacidad de los datos
- Categorización de los sistemas de información.
- Aseguramiento de los sistemas de desarrollo seguro

Desarrollo/adquisición:

- Evaluación de riesgos
- Selección y documentación de control de seguridad
- Diseño de la arquitectura de seguridad
- Diseño de ingeniería de controles de seguridad y desarrollo
- Desarrollo de documentación de seguridad
- Pruebas

Implementación/adquisición:

- Creación de un plan de certificación y acreditación
- Integrar seguridad en ambientes y sistemas
- Sistemas de control de acceso
- Sistema de autorización

Operaciones y mantenimiento:

- Realización de evaluaciones de seguridad operacional
- Revisión de configuraciones, gestión y control
- Monitoreo continuo

Disposición:

- Construir y ejecutar un plan de disposición
- Asegurar la preservación de la información
- Sonetizar medios
- Disposición de hardware y software
- Cierre del sistema

## 4.4 Microsoft security development lifecycle.

El ciclo de vida de desarrollo de seguridad (SDL) consiste en un conjunto de prácticas que respaldan los requisitos de cumplimiento y garantía de seguridad. SDL ayuda a los desarrolladores a crear software más seguro al reducir la cantidad y la gravedad de las vulnerabilidades en el software, al mismo tiempo que reduce el costo de desarrollo.

Microsoft, 2010, como se citó en Zambrano, s.f ofrece 7 fases para que se pueda cumplir  a cabalidad las buenas prácticas a desarrollar de este modelo:

Entrenamiento:

- SDL Practica #1: Capacitación de seguridad

Requerimientos:

- SDL Práctica # 2: Establecer los requisitos de seguridad y privacidad
- SDL Practica # 3: Crear puntos de calidad
- SDL Práctica # 4: Evaluaciones de riesgo de seguridad y privacidad

Diseño:

- SDL Práctica # 5: Establecer los requisitos de diseño
- SDL Práctica # 6: Análisis de la superficie de ataque
- SDL Práctica # 7: Modelamiento de Amenazas

Implementación:

- SDL Practica # 8: Utilización de herramientas aprobadas
- SDL Practica # 9: Desaprobar funciones no seguras
- SDL Practica # 10: Realizar análisis estático de código

Verificación:

- SDL Practica # 11: Realizar análisis dinámico
- SDL Práctica # 12: Pruebas Fuzz
- SDL Practica # 13: Revisión de superficie de ataque

Liberación:

- SDL Práctica # 14: Crear un Plan de Respuesta a Incidentes
- SDL Práctica # 15: Revisión de la Conducta Final de Seguridad
- SDL Practica # 16: Certificar lanzamiento y Archivo

Respuesta:

- SDL Práctica # 17: Ejecutar el Plan de Respuesta a Incidentes

# 

# Recomendación del modelo a implementar.

**Software Assurance Maturity Model**, este es un software implementado por Fortify Software que es una compañía especialista en software de seguridad, el desarrollo e implementación de este software fue a cargo del director estratégico de servicios Pravir Chandra, él trabaja con clientes para construir y optimizar software de seguridad.

Como grupo de trabajo seleccionamos este modelo de software porque ofrece un marco abierto para formular e implementar estrategias en las que encajan los diferentes riesgos que enfrenta una organización para la seguridad en el software, que le ofrece a las organizaciones:

- Evaluación de las prácticas de seguridad en software de la organización.
- Construcción de un paquete de seguridad en software balanceado en iteraciones bien definidas.
- Demostración de mejoras precisas en un programa de aseguramiento de la seguridad.
- Definición y medida de actividades relacionadas con la seguridad dentro de una organización.

Como proyecto libre, siempre permanecerá neutral al fabricante y queda disponible libremente para que todo el mundo pueda utilizarlo.

# 7. Bibliografía.

- [1] El CCN-CERT es la Respuesta a incidentes de Seguridad de la Información y el CERT Gubernamental español - CCN-CERT. (n.d.). Cni.es. Retrieved October 30, 2022, from [https://www.ccn-cert.cni.es/](https://www.ccn-cert.cni.es/)
- CLASP — Comprehensive, Lightweight Application Security Process, author owasp.org, Version Date: 31 March 2006 [https://owasp.org/www-pdf-archive/Us_owasp-clasp-v12-for-print-lulu.pdf](https://owasp.org/www-pdf-archive/Us_owasp-clasp-v12-for-print-lulu.pdf)
- Secure Software Development Life Cycle, author Victor Figueroa [Figueroa.rv@gmail.com](mailto:Figueroa.rv@gmail.com), [https://owasp.org/www-pdf-archive/OWASP-LATAMTour-Patagonia-2016-rvfigueroa.pdf](https://owasp.org/www-pdf-archive/OWASP-LATAMTour-Patagonia-2016-rvfigueroa.pdf)
- On the secure software development process: CLASP, SDL and Touchpoints compared, Authors Bart De Win *, Riccardo Scandariato, Koen Buyens, Johan Gregoire, Wouter Joosen, Available online 15 February 2008, [https://lirias.kuleuven.be/bitstream/123456789/242084/1/comparison.pdf](https://lirias.kuleuven.be/bitstream/123456789/242084/1/comparison.pdf)
- Introduction to the CLASP Process, Author(s): [Dan Graham](https://us-cert.cisa.gov/bsi/about-us/authors/dan-graham) Published: November 16, 2006 | Last revised: July 03, 2013 [https://www.cisa.gov/uscert/bsi/articles/best-practices/requirements-engineering/introduction-to-the-clasp-process](https://www.cisa.gov/uscert/bsi/articles/best-practices/requirements-engineering/introduction-to-the-clasp-process)
- SP 800-64 Rev. 2. Security Considerations in the System Development Life CycleRichard Kissel, Kevin M. Stine, Matthew A. Scholl, Hart Rossman, James Fahlsing and Jessica Gulick [https://doi.org/10.5555/2206279](https://doi.org/10.5555/2206279)
- Microsoft Corporation [https://learn.microsoft.com/en-us/windows/security/threat-protection/msft-security-dev-lifecycle](https://learn.microsoft.com/en-us/windows/security/threat-protection/msft-security-dev-lifecycle)
- Open SAMM, Pavir Chandra (2009). Tomado de: [https://www.opensamm.org/author/chandra/](https://www.opensamm.org/author/chandra/)
- SBD, MODELO DE MADUREZ DE SEGURIDAD DE SOFTWARE - OPENSAMM EN ESPAÑOL (2011). Recopilado de: [http://www.securitybydefault.com/2011/07/modelo-de-madurez-de-seguridad-de.html](http://www.securitybydefault.com/2011/07/modelo-de-madurez-de-seguridad-de.html)
- Zambrano, M. (s.f). Modelos existentes. Lectura Fundamental 2 
