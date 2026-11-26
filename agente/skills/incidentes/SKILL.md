
---
name: analisis-incidentes
description: Analiza alertas operativas simuladas y genera
  diagnosticos preliminares para equipos DevOps/SRE.
---

# Análisis de incidentes operativos

## Cuándo utilizar esta skill

Cuando el operador proporcione una alerta,
un incidente, logs o métricas para diagnóstico.

## Entradas esperadas

- Identificador de alerta.
- Servicio afectado.
- Descripción del problema.
- Métricas disponibles.
- Logs disponibles.
- Contexto operativo.

## Procedimiento

### Paso 1. Interpretación

Identificar el servicio afectado y el síntoma
principal del incidente.

### Paso 2. Clasificación

Determinar la categoría del incidente:

- Infraestructura.
- Aplicación.
- Red.
- Rendimiento.
- Disponibilidad.
- Seguridad.
- Información insuficiente.

### Paso 3. Criticidad

Clasificar el incidente según su impacto conocido:

- Baja.
- Media.
- Alta.
- Crítica.

Si el impacto no puede determinarse, indicarlo
explícitamente.

### Paso 4. Análisis de evidencia

Identificar los logs, métricas y datos relevantes.

Diferenciar la información observada de las
interpretaciones realizadas.

### Paso 5. Diagnóstico

Formular hipótesis sobre las posibles causas.

Indicar qué evidencia respalda cada hipótesis
y qué información falta para confirmarla.

### Paso 6. Recomendaciones

Proponer acciones de diagnóstico y resolución,
ordenadas por prioridad y riesgo.

No ejecutar las recomendaciones.

### Paso 7. Escalamiento

Determinar si resulta necesaria la intervención
del operador humano.

### Paso 8. Informe

Generar la respuesta con el siguiente formato:

## Resultado del análisis

- ID de alerta:
- Servicio afectado:
- Categoría:
- Criticidad:
- Resumen:
- Evidencias identificadas:
- Hipótesis principal:
- Hipótesis alternativas:
- Información faltante:
- Acciones recomendadas:
- Escalamiento requerido: Sí / No
- Motivo del escalamiento:
- Herramientas utilizadas:
- Acciones ejecutadas:

## Criterios de parada

Finalizar el análisis cuando:

- Se haya generado el informe.
- No exista información suficiente para continuar.
- Se requieran permisos fuera del alcance.
- Se detecte una situación que deba escalarse.

No inventar métricas, logs ni resultados.
No modificar infraestructura.
```

