# Playbooks, SIEM y SOAR

Un Playbook o Runbook es una guía que contiene acciones predefinidas para responder de forma organizada y consistente ante un incidente de seguridad. Permite establecer qué debe hacerse, quién debe hacerlo y en qué momento, reduciendo errores y el impacto de los incidentes.

Los playbooks pueden incluir instrucciones detalladas, diagramas de flujo y tablas. También pueden estar diseñados para incidentes específicos, como ransomware, accesos sospechosos o comportamientos inusuales.

### Playbooks y SIEM

Los SIEM recopilan y analizan eventos de seguridad para detectar posibles amenazas. Cuando un SIEM genera una alerta, el analista puede utilizar un playbook para determinar los pasos que debe seguir para investigar y responder al incidente.

Ejemplo:

Un SIEM detecta un comportamiento inusual de un usuario → el analista consulta el playbook → investiga la actividad → determina las acciones de contención y respuesta.

Playbooks y SOAR

Las herramientas SOAR (Security Orchestration, Automation and Response) permiten automatizar tareas repetitivas de respuesta ante incidentes.

Por ejemplo, si se detectan múltiples intentos de inicio de sesión incorrectos, una plataforma SOAR podría bloquear automáticamente la cuenta y posteriormente el analista seguiría el playbook correspondiente para investigar el incidente.

SIEM vs SOAR
SIEM: recopila, correlaciona y analiza eventos para detectar posibles amenazas.
SOAR: automatiza y coordina acciones de respuesta ante las amenazas detectadas.
Playbook: proporciona las instrucciones que indican cómo debe responder el equipo o cómo debe ejecutarse una acción.
Concepto clave

Los Playbooks/Runbooks proporcionan procedimientos detallados para responder ante incidentes. Al utilizarlos junto con herramientas SIEM y SOAR, los equipos de seguridad pueden detectar, investigar y responder a amenazas de forma más rápida, organizada y consistente.
