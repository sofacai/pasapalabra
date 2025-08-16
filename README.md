# Pasapalabra - Juego Interactivo

## Nuevas Funcionalidades Agregadas

### 1. **Campo de Respuesta en el Dashboard**
- Se agregó una sección de respuesta correcta en el control de juego
- Incluye un botón para **mostrar/ocultar PREGUNTA Y RESPUESTA**
- **Tanto pregunta como respuesta se ocultan con asteriscos (***) en el control**
- **El display nunca muestra las respuestas, solo el control**
- Ideal para cuando se pasa el control de una persona a otra sin revelar nada

### 2. **Estructura JSON Mejorada**
- Los archivos JSON ahora incluyen las respuestas correctas
- Formato: `"A_respuesta": "Respuesta correcta"`
- **Se agregó la letra Ñ después de la N (27 letras en total)**
- Compatible con la estructura anterior

### 3. **Carga de Múltiples JSONs**
- Soporte para cargar varios archivos JSON en paralelo
- Cada participante puede subir su propio archivo sin ver el de otros
- Los archivos se combinan automáticamente en el juego

### 4. **Timer Individual por Participante**
- **Cada participante tiene su propio timer independiente**
- El tiempo se pausa automáticamente al cambiar de participante
- Cada uno mantiene su tiempo restante por separado
- La configuración de tiempo se aplica al participante actual

### 5. **Navegación Inteligente entre Participantes**
- **Lógica inteligente de navegación con prioridades:**
  1. **Primero**: Si tiene letras amarillas (pasapalabra), va a la primera amarilla
  2. **Segundo**: Si no tiene amarillas, busca su primera letra gris (sin jugar)  
  3. **Tercero**: Si todos completaron la vuelta, va a la primera letra gris global
- **Cada participante mantiene su progreso individual**
- **Prioriza completar la vuelta antes de empezar nuevas letras**

## Estructura de Archivos JSON

```json
{
  "1": {
    "participante": "Nombre del Participante",
    "imagen": "fotos/foto.jpg",
    "A": "Con la A. Pregunta para la letra A",
    "A_respuesta": "Respuesta correcta",
    "B": "Con la B. Pregunta para la letra B",
    "B_respuesta": "Respuesta correcta",
    "N": "Con la N. Pregunta para la letra N",
    "N_respuesta": "Respuesta correcta",
    "Ñ": "Con la Ñ. Pregunta para la letra Ñ",
    "Ñ_respuesta": "Respuesta correcta",
    // ... continúa para todas las 27 letras
  }
}
```

## Archivos Incluidos

- `control.html` - Dashboard de control con las nuevas funcionalidades
- `display.html` - Pantalla de visualización (actualizada con Ñ)
- `preguntas_ejemplo.json` - Archivo ejemplo con respuestas y letra Ñ
- `participante_sofia.json` - Archivo individual para Sofía
- `participante_martin.json` - Archivo individual para Martín

## Cómo Usar las Nuevas Funcionalidades

### Mostrar/Ocultar Pregunta y Respuesta
1. En el dashboard de control, busca la sección "Pregunta y Respuesta"
2. **Por defecto tanto pregunta como respuesta aparecen como asteriscos (***)**
3. Haz clic en "🔍 MOSTRAR PREGUNTA Y RESPUESTA" para ver ambas
4. Haz clic en "👁️ OCULTAR PREGUNTA Y RESPUESTA" para volver a mostrar asteriscos
5. **El display nunca muestra las respuestas, solo las ve quien controla el juego**

### Cargar Múltiples Archivos
1. En la sección "Cargar Preguntas", selecciona múltiples archivos JSON
2. Los archivos se cargarán automáticamente y se combinarán
3. Navega entre participantes usando las flechas ← →

## Beneficios

- **Privacidad Total**: Cada participante puede preparar sus preguntas sin que otros las vean
- **Flexibilidad**: Control total sobre cuándo mostrar/ocultar respuestas con asteriscos
- **Separación de Roles**: El display solo muestra el juego, las respuestas solo las ve el controlador
- **Organización**: Archivos separados para mejor gestión del juego
- **Completitud**: Ahora incluye la letra Ñ para un juego más completo en español
- **Justicia**: Timer individual asegura que cada participante tenga el mismo tiempo disponible
- **Fluidez**: Navegación inteligente mantiene el ritmo del juego sin interrupciones
- **Estrategia**: Prioriza completar vueltas antes de empezar letras nuevas

## Archivos de Ejemplo

Incluye dos archivos JSON listos para usar:
- `participante_sofia.json` - Preguntas para Sofía con todas las 27 letras
- `participante_martin.json` - Preguntas para Martín con todas las 27 letras

Los nombres de los archivos JSON no importan, pueden ser cualquiera.