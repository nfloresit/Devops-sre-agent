
# Política de memoria del agente

## Objetivo

Establecer criterios para la persistencia,
actualización y revisión de información utilizada
por el agente.

## Información permitida

- Características del entorno de pruebas.
- Convenciones técnicas del proyecto.
- Preferencias operativas no sensibles.
- Conocimientos técnicos previamente verificados.
- Aprendizajes aprobados por el responsable humano.

## Información prohibida

- Contraseñas.
- Tokens de acceso.
- API keys.
- Certificados y claves privadas.
- Datos personales.
- Información confidencial.
- Datos de sistemas productivos.
- Logs que contengan información sensible.
- Hipótesis no verificadas presentadas como hechos.

## Reglas de actualización

- Persistir únicamente información relevante.
- Evitar duplicaciones.
- Eliminar información obsoleta.
- Revisar los cambios antes de su aprobación.
- No utilizar la memoria para ampliar permisos.

## Control durante la validación

Durante las pruebas formales se utilizará una
memoria inicial equivalente para cada ejecución.

No se permitirán modificaciones persistentes entre
ejecuciones que alteren las condiciones iniciales.

## Revisión y gobernanza

El operador humano será responsable de revisar
el contenido de la memoria y autorizar los cambios.

La política considera los principios de finalidad,
pertinencia, seguridad y confidencialidad de
la información contemplados en la Ley 25.326.

## Limitaciones

Este documento define una política de uso.

Su cumplimiento requiere controles técnicos
adicionales sobre almacenamiento, permisos,
configuracion y acceso a la información.
