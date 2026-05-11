# Actividad Práctica – AEE

## Desafío de Consultoría "Gobernanza Digital"

* **Unidad:** UD7. Sistemas de Gestión Empresarial  
* **Contexto:** RA7 (CE: a, c, f, i)  
* **Investigación**. Se puede utilizar TODO en INTERNET, **menos agentes IA**. Se deben referenciar todas las fuentes utilizadas.

# 1\. El Escenario (El "Por qué")

La empresa sevillana **"Aceites del Aljarafe S.L."** opera actualmente con el "Efecto Silo": usan hojas de cálculo para el inventario, una base de datos Access antigua para clientes y facturan a mano. Han contratado a vuestro equipo de consultoría para migrar a un sistema profesional.

# 2\. Misión del Equipo (Grupos de 3 personas)

Vuestra tarea es entregar una **Propuesta Técnica de Implantación** que cubra los siguientes tres bloques fundamentales:

## Bloque A: Análisis de Mercado y Selección (CE a, c)

Debéis elegir entre **Odoo (SaaS o Community)**, **SAP S/4HANA** o **Zoho One**.

1. Justifica la elección basándote en el perfil de la empresa (25 empleados, presupuesto ajustado, necesidad de personalización en el etiquetado).  
2. **Cálculo de TCO:** Realiza una estimación a 3 años. No olvidéis incluir:  
   * Coste de licencias/suscripción.  
   * Coste de implantación (vuestras horas de desarrollo: estima 100h a 40€/h).  
   * Coste operativo (Hosting en Google Cloud, AWS, Huawei Cloud o similar).

## Bloque B: Diseño de Seguridad RBAC (CE f)

Diseña la matriz de permisos para los siguientes roles, asegurando el **Principio de Mínimo Privilegio**:

* **Administrador:** Acceso total.  
* **Comercial:** Solo ve sus clientes y presupuestos (Record Rules).  
* **Operario de Almacén:** Solo ve stock y albaranes de entrada/salida.  
* **Contable:** Puede mirar facturas pero no puede modificar el stock.

## Bloque C: Documentación de Explotación (CE i)

Siguiendo la norma **ISO/IEC 26514**, redacta un breve **Manual de Despliegue** para que el responsable de IT de la empresa pueda levantar el sistema en caso de caída. Debe incluir:

1. El fragmento de *docker-compose.yml* necesario.  
2. El comando para realizar un backup de la base de datos PostgreSQL.

# 3\. Entregable y Evaluación

Subirás un README a un repositorio Github específico con la propuesta técnica. Lo importante aquí es la **precisión técnica**:

* ¿Es coherente el TCO con la realidad de una PYME?  
* ¿La matriz RBAC evita que el comercial vea los costes de producción?  
* ¿El comando de backup es sintácticamente correcto?

# 4\. Cronograma de la Actividad

* **08:30 \- 08:50 min:** Explicación del caso y formación de grupos (Willman).  
* **08:50 \- 09:40 min:** Trabajo de investigación y redacción (Uso de Odoo y búsqueda de TCO).  
* **09:40 \- 10:25 min:** "*Elevator Pitch*": Cada grupo defiende su elección de ERP frente al "Cliente" (Willman).

# 5\. Rúbrica de Evaluación

| Criterio de Evaluación | Sobresaliente (10-9) | Notable(8-7) | Aprobado(6-5) | Insuficiente(4-0) | Peso |
| ----- | ----- | ----- | ----- | ----- | :---: |
| **Análisis y Selección de ERP (CE a, c)** | Selecciona el sistema ideal justificando con precisión técnica y estratégica según las necesidades de la PYME. | Selecciona el sistema adecuado con una justificación clara pero con pocos detalles técnicos. | La selección es aceptable pero la justificación es genérica o poco adaptada al caso. | No justifica la selección o elige un sistema claramente inadecuado para el escenario. | 18% |
| **Cálculo de TCO (CE c)** | Realiza un cálculo quirúrgico a 3 años incluyendo licencias, horas de desarrollo y hosting con datos reales. | Calcula el TCO incluyendo los bloques principales, aunque con pequeñas imprecisiones en los costes operativos. | El cálculo es muy básico y omite costes indirectos importantes (mantenimiento o backups). | No realiza el cálculo de TCO o los datos son totalmente incoherentes con el mercado. | 18% |
| **Diseño RBAC y Seguridad (CE f)** | Define una matriz de permisos perfecta que cumple estrictamente el principio de mínimo privilegio y usa Record Rules. | Define la matriz correctamente para todos los roles, aunque la restricción del comercial es mejorable. | La matriz es funcional pero asigna permisos excesivos a roles que no los requieren. | No define roles o la matriz permite acceso total a personal no autorizado (riesgo de seguridad). | 18% |
| **Doc. de Explotación e ISO 26514 (CE i)** | Documentación profesional con *docker-compose.yml* y comandos de backup 100% funcionales y sintácticamente correctos. | Documentación clara siguiendo la norma ISO, con comandos funcionales pero con errores leves de formato. | Incluye la documentación mínima pero los comandos requieren ajustes para ser funcionales. | Documentación inexistente, desorganizada o con comandos que generan errores críticos. | 18% |
| **Organización del repositorio Github** **(Competencia Transversal)** | Organización profesional, README con imágenes y bien “estilizado” | Organización profesional, README con imágenes | Organización profesional y README | Sin organización aunque tenga README | 14% |
| **Presentación y Pitch** **(Competencia Transversal)** | Defiende la propuesta con seguridad, lenguaje técnico preciso y convence al "cliente" de la viabilidad. | Presentación clara y profesional, respondiendo bien a la mayoría de las dudas técnicas. | Exposición correcta pero con dificultades para defender los puntos financieros (TCO). | No es capaz de explicar la propuesta o utiliza un lenguaje poco profesional. | 14% |
| **Uso de agentes IA** | Incluyendo Google, Bing, etc. “Modo IA” |  |  |  | **\-100%** |

### **Observaciones:**

* **CE a y c:** Se ha valorado especialmente que no solo elijas Odoo por ser el que usamos en clase, sino que demuestres conocer las alternativas.  
* **CE f:** Lo importante aquí es que el comercial no pueda "asomarse" a la contabilidad.  
* **CE i:** Un comando de backup mal escrito es un suspenso directo en este bloque, fíjate que la integridad del dato no admite errores de sintaxis.  
* **Evaluación de competencias**. Una vez hayas leído toda la actividad y sepas qué vas a hacer, levántate y desde tu puesto dile al profesor que has comprendido la actividad, los nombres de los integrantes del grupo y el profesor te dará el “Ok“ para comenzar. Si no lo haces, el profesor evaluará qué has hecho y si comienzas de nuevo o continúas.

