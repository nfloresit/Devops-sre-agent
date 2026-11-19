# Agente DevOps SRE: guía y MVP de agente de 

Guía de implementación y agente demostrativo para tratamient de alertas en un entorno de **prueba**. Acompaña el Trabajo Final de Grado *"Transformación de roles y competencias en equipos DevOps/SRE: incorporación de agentes autónomos de IA"* (UEAN, Licenciatura en Tecnología Informática).

> **Aviso.** Este proyecto es una demostración académica. No está pensado para producción, no tiene credenciales de sistemas reales y no debe exponerse a internet sin autenticación y control de acceso.

## Contenido

- `checklist/implementacion.md`: checklist de diez pasos con condiciones verificables.
- `agente/AGENTS.md`: rol, acciones permitidas, acciones que requieren confirmación y acciones prohibidas.
- `agente/memories/LIMITS.md`: qué puede y qué no puede guardar el agente en memoria.
- `agente/skills/incidentes/SKILL.md`: procedimiento de evaluacion, con criterio de incidentes.
- `docs/SECURITY.md`: decisiones de seguridad y estado de la infraestructura.

## Checklist de implementación (resumen)

| # | Paso | Condición verificable |
|---|---|---|
| 1 | Definir el nivel de autonomía | Figura por escrito en `AGENTS.md` el nivel elegido, con las acciones que incluye. |
| 2 | Escribir las instrucciones del agente | Existe `AGENTS.md` con rol, límites y escalamiento. |
| 3 | Definir la política de memoria | Existe `LIMITS.md` que excluye credenciales, datos personales y datos de producción. |
| 4 | Documentar los procedimientos como skills | Cada skill tiene `SKILL.md` con cuándo aplica, pasos y criterio de parada. |
| 5 | Aplicar permisos mínimos | Ninguna credencial en el repositorio; las herramientas están limitadas a lectura salvo confirmación. |
| 6 | Registrar trazas de cada decisión | Cada acción queda en un registro con fecha, herramienta, entrada, salida y motivo. |
| 7 | Probar el rollback | Existe un procedimiento de reversión que se ejecutó en el entorno de prueba. |
| 8 | Ejecutar una batería de pruebas antes de cada cambio | Hay al menos un caso de alerta conocida con resultado esperado documentado. |
| 9 | Asignar responsable y escalamiento | `AGENTS.md` nombra a la persona o equipo responsable y los criterios para escalar. |
| 10 | Revisar periódicamente | Hay una fecha de revisión y un registro de cambios de las instrucciones y de la memoria. |

## Estructura del agente

El agente se configura con archivos separados por función:

- **Identidad:** `SOUL.md` define la personalidad y el tono.
- **Instrucciones del proyecto:** `AGENTS.md` define el rol, los límites y el escalamiento.
- **Memoria:** `memories/` guarda hechos durables del entorno de prueba, sin secretos.
- **Procedimientos:** `skills/` contiene una carpeta por procedimiento, con su `SKILL.md`.
- **Secretos:** `.env`, fuera del repositorio.

## Infraestructura de la demostración

- Máquina virtual en Google Cloud, con Ubuntu 24.04 LTS.
- Docker y Docker Compose, con el agente y su interfaz web en contenedores.
- Modelo de lenguaje consumido mediante API.

## Seguridad

Ver `docs/seguridad.md`. Resumen:

- Acceso SSH solo con llave RSA.
- Firewall con reglas de origen restringido.
- Interfaz web con contraseña y sin exposición directa a internet.
- El contenedor está aislado del sistema anfitrión.
- Ninguna clave ni contraseña está en este repositorio.

## Limitaciones

El agente opera sobre alertas de prueba. Su comportamiento depende de un modelo probabilístico, por lo que las pruebas describen tendencias y no garantías.

