# 4.2. Information Architecture

En esta sección se establecen las decisiones y sustento que dirigen la organización del contenido en las experiencias web y móvil de EcoCrop SmartCrop, incluyendo la Landing Page y las aplicaciones. Las propuestas están orientadas a que los visitantes y usuarios se adapten con facilidad a la funcionalidad de cada producto y puedan encontrar todo lo que necesiten sin esfuerzo.

---

## 4.2.1. Organization Systems

En la aplicación SmartCrop se implementarán diversos sistemas de organización para estructurar la información de forma clara, accesible y adaptada a los diferentes segmentos de usuarios (agricultores individuales, cooperativas y asociaciones agrícolas).

### Organización Visual del Contenido

#### Jerárquica (Visual Hierarchy)
Se aplicará en las pantallas principales de la aplicación y en los módulos críticos como alertas de plagas y estado del clima. La información prioritaria se estructura de mayor a menor importancia:

**Aplicaciones principales:**
- **Panel principal del agricultor**: Alertas críticas (plagas emergentes, temperatura extrema) en la parte superior con mayor tamaño e iconografía destacada
- **Dashboard de cooperativa**: Métricas consolidadas priorizadas por impacto en la producción
- **Módulo de alertas**: Notificaciones urgentes → advertencias → recomendaciones → historial
- **Información meteorológica**: Condiciones actuales → pronóstico inmediato → pronóstico extendido

**Caso de uso específico:**
```
Nivel 1 (Crítico): ALERTA: Plaga detectada en Lote A
Nivel 2 (Importante): Temperatura alta prevista (32°C)
Nivel 3 (Informativo): Reporte semanal disponible
Nivel 4 (Secundario): Nueva guía de control disponible
```

#### Secuencial (Step-by-step)
Se aplicará en procesos que requieren una guía paso a paso, especialmente beneficioso para usuarios con menor alfabetización digital:

**Procesos principales:**
- **Registro de nuevos cultivos**: Información básica → Ubicación y área → Configuración de sensores → Confirmación
- **Instalación de sensores IoT**: Selección de equipo → Ubicación física → Conexión → Calibración → Pruebas
- **Flujo de diagnóstico de plagas**: Captura de imagen → Análisis automático → Confirmación → Recomendaciones → Seguimiento
- **Configuración de alertas**: Tipo de alerta → Parámetros → Canales de notificación → Programación → Activación

**Ejemplo de flujo secuencial:**
```
Paso 1/4: Información del Cultivo
[Nombre del cultivo] [Tipo de cultivo ▼]
                    [Siguiente →]

Paso 2/4: Ubicación y Área
[Seleccionar ubicación en mapa]
[Área: ___ hectáreas]
                    [← Anterior] [Siguiente →]
```

#### Matricial
Se aplicará para mostrar información cruzada que requiere comparación simultánea entre múltiples variables:

**Aplicaciones principales:**
- **Análisis de plagas por cultivo**: Tabla cruzada mostrando tipos de plagas vs tipos de cultivos vs temporada
- **Reportes de productividad**: Comparación de fincas/lotes vs indicadores de rendimiento vs períodos
- **Dashboard de cooperativas**: Análisis comparativo entre asociados con múltiples métricas
- **Correlación clima-plagas**: Matriz que cruza condiciones climáticas con incidencia de plagas

**Ejemplo de organización matricial:**
```
                 | Tomate | Maíz | Frijol | Papa |
Pulgón          |   ⚠️    |  ✅   |   🚨   |  ⚠️  |
Mosca Blanca    |   🚨    |  ⚠️   |   ✅   |  ✅  |
Gusano Cogollero|   ✅    |  🚨   |   ⚠️   |  ⚠️  |
```

### Esquemas de Categorización del Contenido

#### Alfabético
**Aplicación:** Biblioteca de plagas y enfermedades, catálogo de cultivos
- **Caso de uso:** Módulo "Guías de Plagas" donde agricultores buscan por nombre común o científico
- **Implementación:** Lista A-Z con índice lateral para navegación rápida
- **Ejemplo:** 
  ```
  A: Áfidos, Antracnosis
  B: Babosas, Barrenador
  C: Cochinillas, Chinche
  ```

#### Cronológico
**Aplicación:** Historiales de cultivos, registros de incidencias, versiones de reportes
- **Caso de uso:** Historial de alertas y medidas tomadas, cronología de tratamientos aplicados
- **Implementación:** Línea de tiempo interactiva con filtros por período
- **Ejemplo:**
  ```
  15 Dic 2024: Detección de pulgón - Lote A
  16 Dic 2024: Aplicación de tratamiento orgánico
  20 Dic 2024: Seguimiento - Reducción del 80%
  22 Dic 2024: Problema resuelto
  ```

#### Por Tópicos (Temático)
**Aplicación:** Centro de ayuda, biblioteca de conocimientos, recursos de capacitación
- **Categorías principales:**
  - **Control de Plagas**: Identificación, tratamientos, prevención
  - **Gestión Climática**: Pronósticos, adaptación, riesgos
  - **Manejo de Cultivos**: Siembra, cuidado, cosecha
  - **Tecnología IoT**: Sensores, instalación, mantenimiento
  - **Cooperativismo**: Gestión grupal, reportes consolidados
  - **Análisis de Datos**: Reportes, métricas, tendencias

#### Según Audiencia (Grupos de Usuarios)
La aplicación adapta la profundidad y tipo de información según el perfil del usuario:

**Agricultores Individuales:**
- Información práctica, simple y visual
- Alertas inmediatas con pasos de acción claros
- Guías paso a paso con ilustraciones
- Métricas básicas de sus cultivos específicos

**Cooperativas y Asociaciones:**
- Reportes consolidados de múltiples productores
- Métricas de producción agregadas
- Herramientas de gestión grupal
- Análisis comparativos entre miembros
- Dashboard ejecutivo con KPIs

## 4.2.2. Labeling Systems

En SmartCrop, los datos y funcionalidades se representan con etiquetas cortas, consistentes y familiares para los agricultores y cooperativas, evitando tecnicismos innecesarios.

### Principios de Etiquetado

1. **Claridad**: Términos simples y directos que cualquier agricultor comprenda
2. **Consistencia**: Las mismas acciones mantienen la misma etiqueta en toda la aplicación
3. **Brevedad**: Limitadas a una o dos palabras por etiqueta
4. **Asociación**: Cada etiqueta se vincula intuitivamente con su contenido o acción
5. **Localización**: Términos apropiados para el contexto agrícola peruano

### Etiquetas Principales y Asociaciones

#### Navegación Principal
| Etiqueta | Asociación | Contenido |
|----------|------------|-----------|
| **Inicio** | Hogar, punto de partida | Panel principal con resumen de clima, cultivos y alertas |
| **Alertas** | Urgencia, atención inmediata | Notificaciones de plagas detectadas, cambios climáticos críticos |
| **Clima** | Tiempo, condiciones | Información meteorológica actual y pronósticos |
| **Plagas** | Problemas, amenazas | Biblioteca visual, identificación y guías de control |
| **Cultivos** | Producción, cosecha | Registro de parcelas, historial productivo |
| **Sensores** | Tecnología, monitoreo | Estado de dispositivos IoT, lecturas en tiempo real |
| **Reportes** | Análisis, resultados | Datos organizados exportables por cultivo/temporada |
| **Guías** | Aprendizaje, ayuda | Tutoriales, consejos, videos de capacitación |
| **Comunidad** | Compartir, colaborar | Espacio para intercambio entre agricultores |
| **Soporte** | Ayuda, asistencia | FAQ, contacto técnico, expertos |

#### Micro-etiquetas Contextuales
| Contexto | Etiqueta | Acción/Estado |
|----------|----------|---------------|
| **Detección de Plagas** | "Enviar Foto" | Subir imagen para análisis automático |
| **Configuración** | "Configurar Alertas" | Personalizar notificaciones |
| **Estados de Cultivo** | "Activo" | Cultivo en monitoreo |
| **Estados de Cultivo** | "Inactivo" | Fuera de temporada |
| **Estados de Sensor** | "Conectado" | Funcionando normalmente |
| **Estados de Sensor** | "Desconectado" | Requiere atención |
| **Indicadores Temporales** | "Nuevo" | Contenido recién generado |
| **Indicadores Temporales** | "Actualizado" | Información recién modificada |
| **Acciones** | "Descargar" | Obtener reporte o recurso |
| **Acciones** | "Compartir" | Enviar a comunidad o contactos |

#### Etiquetas de Severidad y Estados
```css
Saludable    → Todo funcionando correctamente
Atención     → Requiere vigilancia
Advertencia  → Acción recomendada pronto
Crítico      → Acción inmediata requerida
Inactivo     → Sin datos o desconectado
```

### Ejemplos de Etiquetado Contextual

#### En Dashboard Principal:
```
Clima Hoy: Soleado, 28°C
Mis Cultivos: 3 Activos, 1 Nuevo
Alertas: 2 Nuevas, 1 Crítica
Último Reporte: Hace 2 días
```

#### En Módulo de Plagas:
```
Plaga Detectada: Pulgón Verde
Detectado: Hoy 10:30 AM
Ubicación: Lote A - Tomate
Nivel: Moderado
Ver Guía de Control →
```

---

## 4.2.3. SEO Tags and Meta Tags

### Landing Page (Sitio Web de Presentación)

#### Página Principal
```html
<title>SmartCrop | Agricultura Inteligente con IoT y Detección de Plagas</title>
<meta name="description" content="SmartCrop es una solución digital para pequeños y medianos agricultores. Detecta plagas mediante IA, monitorea clima en tiempo real y ofrece guías prácticas para optimizar la producción agrícola.">
<meta name="keywords" content="agricultura inteligente, detección de plagas, IoT agrícola, SmartCrop, control climático, cultivo sostenible, cooperativas agrícolas, agro tecnología, sensores agrícolas, agricultura de precisión">
<meta name="author" content="Equipo EcoCrop - SmartCrop, Universidad Peruana de Ciencias Aplicadas (UPC)">
<meta name="robots" content="index, follow">
<meta name="language" content="Spanish">
<meta name="geo.region" content="PE">
<meta name="geo.placename" content="Peru">
```

#### Página de Características
```html
<title>Características SmartCrop | Detección de Plagas y Monitoreo IoT</title>
<meta name="description" content="Descubre las características de SmartCrop: detección automática de plagas con IA, sensores IoT para monitoreo climático, alertas en tiempo real y reportes detallados para agricultores.">
<meta name="keywords" content="características SmartCrop, detección plagas IA, sensores IoT agricultura, alertas climáticas, reportes agrícolas, monitoreo cultivos">
```

#### Página de Precios
```html
<title>Planes y Precios SmartCrop | Soluciones Agrícolas Accesibles</title>
<meta name="description" content="Conoce los planes de SmartCrop para agricultores y cooperativas. Precios accesibles para tecnología agrícola avanzada. Prueba gratuita disponible.">
<meta name="keywords" content="precios SmartCrop, planes agricultura, suscripción agrícola, precios IoT agricultura, planes cooperativas agrícolas">
```

#### Página de Contacto
```html
<title>Contacto SmartCrop | Soporte para Agricultores</title>
<meta name="description" content="Contáctanos para más información sobre SmartCrop. Soporte técnico especializado para agricultores y cooperativas. Respuesta rápida garantizada.">
<meta name="keywords" content="contacto SmartCrop, soporte agricultores, ayuda técnica agricultura, consultas agro tecnología">
```

### Web Application (Plataforma Interactiva)

#### Dashboard Principal
```html
<title>SmartCrop WebApp | Monitoreo de Cultivos y Gestión Agrícola en Tiempo Real</title>
<meta name="description" content="Plataforma web para agricultores y cooperativas que permite registrar cultivos, recibir alertas de plagas y clima, consultar reportes de producción y acceder a una comunidad colaborativa.">
<meta name="keywords" content="monitoreo agrícola, plagas en cultivos, reportes agrícolas, sensores IoT, agricultura digital, gestión cooperativa, sostenibilidad agrícola">
<meta name="author" content="Equipo EcoCrop - SmartCrop">
<meta name="robots" content="noindex, nofollow">
```

#### Módulo de Alertas
```html
<title>Alertas SmartCrop | Notificaciones de Plagas y Clima</title>
<meta name="description" content="Centro de alertas SmartCrop con notificaciones inmediatas sobre plagas detectadas, cambios climáticos y recomendaciones de acción para proteger tus cultivos.">
<meta name="keywords" content="alertas agrícolas, notificaciones plagas, alertas climáticas, avisos cultivos">
```

#### Módulo de Reportes
```html
<title>Reportes Agrícolas SmartCrop | Análisis de Productividad</title>
<meta name="description" content="Genera reportes detallados de productividad, análisis de plagas, rendimiento de cultivos y métricas de tu producción agrícola con SmartCrop.">
<meta name="keywords" content="reportes agrícolas, análisis productividad, métricas cultivos, estadísticas agricultura">
```

### Etiquetas Open Graph y Twitter Cards

#### Para Landing Page
```html
<!-- Open Graph -->
<meta property="og:title" content="SmartCrop | Agricultura Inteligente con IoT">
<meta property="og:description" content="Tecnología avanzada para agricultores: detección de plagas, monitoreo climático y gestión inteligente de cultivos.">
<meta property="og:image" content="https://smartcrop.ecocrop.com/assets/images/og-smartcrop.jpg">
<meta property="og:url" content="https://smartcrop.ecocrop.com">
<meta property="og:type" content="website">
<meta property="og:site_name" content="SmartCrop">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="SmartCrop | Agricultura Inteligente con IoT">
<meta name="twitter:description" content="Tecnología avanzada para agricultores: detección de plagas, monitoreo climático y gestión inteligente de cultivos.">
<meta name="twitter:image" content="https://smartcrop.ecocrop.com/assets/images/twitter-smartcrop.jpg">
<meta name="twitter:creator" content="@EcoCropUPC">
```

---

## 4.2.4. Navigation Systems

El sistema de navegación de SmartCrop está diseñado para que usuarios con diferentes niveles de experiencia tecnológica puedan recorrer el contenido de manera intuitiva, rápida y consistente.

### Principios de Navegación

1. **Claridad**: Menús y botones con etiquetas directas y comprensibles
2. **Consistencia**: Ubicación uniforme de elementos de navegación en todas las páginas
3. **Accesibilidad**: Optimización para dispositivos móviles y usuarios con diversas habilidades
4. **Orientación**: Indicadores visuales claros de ubicación actual (breadcrumbs, menú activo)
5. **Eficiencia**: Minimizar clics para acceder a información prioritaria

### Landing Page - Sistema de Navegación

#### Menú Superior Principal
Menú horizontal fijo (sticky) siempre visible:
```
[Logo SmartCrop] [Inicio] [Cómo Funciona] [Características] [Precios] [Testimonios] [Contacto] [Acceder a la App]
```

**Características del menú:**
- **Posición**: Fija en la parte superior (sticky navigation)
- **Responsive**: Se colapsa en menú hamburguesa en dispositivos móviles
- **Destacado**: Botón "Acceder a la App" con color contrastante
- **Estados**: Hover effects y indicador de página activa

#### Navegación Secuencial (Scrolling)
La Landing Page utiliza navegación vertical fluida:

```
Hero Section (Inicio)
    ↓ Scroll suave
Cómo Funciona
    ↓
Características Principales
    ↓
Testimonios
    ↓
Planes y Precios
    ↓
Contacto y CTA Final
```

**Elementos de navegación secundaria:**
- **Botones CTA estratégicos**: "Prueba Gratis", "Ver Demo", "Comenzar Ahora"
- **Navegación por anclas**: Enlaces internos a secciones específicas
- **Botón "Volver Arriba"**: Aparece al hacer scroll hacia abajo

#### Footer Navigation
```
Producto          Recursos          Empresa          Contacto
├─Características ├─Guías           ├─Sobre Nosotros ├─Email
├─Precios         ├─Blog            ├─Equipo         ├─Teléfono
├─Demo            ├─Tutoriales      ├─Carreras       └─Redes Sociales
└─FAQ             └─Soporte         └─Prensa
```

### Web Application - Sistema de Navegación

#### Sidebar Principal (Desktop)
Menú lateral izquierdo persistente con iconografía:

```
Inicio
Alertas          (+ contador de nuevas)
Clima
Plagas           (+ acceso rápido a biblioteca)
Cultivos         (+ dropdown: Activos, Históricos)
Sensores         (+ indicador de estado)
Reportes         (+ dropdown: Por período, Por cultivo)
Guías
Comunidad
Soporte
```

**Características del sidebar:**
- **Colapsible**: Se puede minimizar para maximizar área de trabajo
- **Estados visuales**: Indicadores de notificaciones y actividad
- **Accesos contextuales**: Submenús desplegables para secciones complejas
- **Responsive**: Se convierte en menú inferior en dispositivos móviles

#### Top Navigation Bar
Barra superior con información contextual y acciones del usuario:

```
[Breadcrumb] ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ [Notificaciones] [Usuario ▼]
Inicio > Cultivos > Lote A > Sensores                    (3)      Juan P. 
```

**Elementos incluidos:**
- **Breadcrumbs**: Navegación jerárquica clara
- **Centro de notificaciones**: Acceso rápido a alertas
- **Menú de usuario**: Perfil, configuración, cerrar sesión
- **Búsqueda global**: Barra de búsqueda contextual (en secciones complejas)

#### Navegación Contextual (Micro-navegación)
Dentro de cada módulo, elementos que permiten flujos de trabajo eficientes:

**Ejemplo en Módulo Cultivos:**
```
Lista de Cultivos
├─ Lote A - Tomate    [Ver Reportes] [Sensores] [Fotos]
├─ Lote B - Maíz      [Ver Reportes] [Sensores] [Plagas]
└─ Lote C - Papa      [Ver Reportes] [Sensores] [Alerta]
```

**Ejemplo en Módulo Alertas:**
```
  Alertas Críticas      [Configurar]     [ Enviar Reporte]
├─ Plaga en Lote A      [Ver Detalles]   [ Guía de Control] [Marcar Resuelta]
└─ Temperatura Alta     [Ver Pronóstico] [ Ajustar Alertas]
```

### Patrones de Navegación Específicos

#### Flujo de Navegación para Agricultor Individual
```
1. Login → Dashboard Principal
2. Revisar Alertas (si existen)
3. Consultar Clima del día
4. Revisar estado de Cultivos
5. Generar/Descargar Reportes (semanal)
```

#### Flujo de Navegación para Cooperativa
```
1. Login → Dashboard Consolidado
2. Revisar Reportes Grupales
3. Analizar Sensores de miembros
4. Compartir información en Comunidad
5. Acceder a Soporte técnico especializado
```

#### Navegación de Emergencia
```
Alerta Crítica → Notificación Push → Abrir App → Ir directo al problema → Mostrar guía de acción → Permitir marcar como resuelta
```

### Elementos de Orientación

#### Breadcrumbs
```
Inicio > Cultivos > Lote A > Sensores > Sensor Temperatura #001
```

#### Menú Activo
El elemento de navegación actual se destacará visualmente:
```css
.nav-item.active {
  background: var(--primary-green);
  color: white;
  font-weight: 600;
}
```

#### Progress Indicators
Para procesos multi-paso:
```
Configuración de Sensor: ●━━○━━○━━○  (Paso 1 de 4)
                        Conexión → Ubicación → Calibración → Confirmación
```

---

## 4.2.5. Searching Systems

Los sistemas de búsqueda en SmartCrop están diseñados para ayudar a los usuarios a encontrar información específica rápidamente, considerando las diferencias en experiencia tecnológica y necesidades específicas del sector agrícola.

### Principios de Búsqueda

1. **Simplicidad**: Interfaces de búsqueda intuitivas sin complejidad técnica
2. **Contextualidad**: Resultados relevantes según el módulo o sección actual
3. **Predictibilidad**: Sugerencias automáticas basadas en contenido común
4. **Multimodal**: Búsqueda por texto, voz e imagen
5. **Tolerancia a errores**: Corrección automática y sugerencias alternativas

### Búsqueda Global

#### Barra de Búsqueda Principal
Ubicada en la parte superior del dashboard, permite búsqueda transversal:

```
[Buscar cultivos, plagas, alertas, reportes...] 
```

**Características:**
- **Placeholder dinámico**: Cambia según contexto actual
- **Autocompletado**: Sugerencias en tiempo real mientras se escribe
- **Búsqueda por voz**: Para usuarios con limitaciones de escritura
- **Búsqueda por imagen**: Para identificación de plagas
- **Historial de búsquedas**: Accesos rápidos a búsquedas recientes

#### Algoritmo de Búsqueda Global
```
Prioridad de resultados:
1. Alertas críticas activas relacionadas
2. Cultivos del usuario que coincidan
3. Plagas identificadas previamente
4. Guías y recursos relevantes
5. Contenido de comunidad
6. Historial personal
```

### Sistemas de Búsqueda por Módulo

#### Módulo Plagas - Búsqueda Especializada

**Búsqueda por Texto:**
```
Buscar plaga: [nombre común, científico, síntomas...]
Filtros: [Mi región] [Tipo de cultivo] [Temporada] [Severidad]
```

**Opciones de filtrado:**
- **Por cultivo afectado**: Tomate, Maíz, Papa, Frijol, etc.
- **Por tipo de plaga**: Insectos, Hongos, Bacterias, Virus
- **Por severidad**: Baja, Moderada, Alta, Crítica  
- **Por región**: Filtro geográfico automático basado en ubicación
- **Por temporada**: Actual, Próxima, Histórica

#### Módulo Cultivos - Búsqueda y Filtrado

**Barra de búsqueda:**
```
[Buscar por nombre, lote, fecha de siembra...]
```

**Filtros avanzados:**
```
Filtrar por:
├─ Fecha de siembra: [Último mes ▼]
├─ Tipo de cultivo: [Todos ▼]
├─ Ubicación: [Todos los lotes ▼]
├─ Estado: [☑️ Activos ☑️ Cosechados ☐ Inactivos]
└─ Rendimiento: [Alto ▼]
```

**Vista de resultados:**
```
Se encontraron 12 cultivos:

Lote A - Tomate Cherry          Sembrado: 15 Nov    Activo
Parcela Norte - Maíz Amarillo   Sembrado: 1 Oct     Creciendo  
Campo Sur - Papa Blanca         Sembrado: 20 Sep    Atención

[Exportar resultados] [Compartir lista]
```

#### Módulo Reportes - Búsqueda Temporal y Analítica

**Búsqueda temporal:**
```
Período: [Último mes ▼]      Desde: [01/12/24] Hasta: [31/12/24]
Cultivo: [Todos ▼]
Tipo: [☑️ Productividad ☑️ Plagas ☑️ Clima ☐ Sensores]
```

**Filtros analíticos:**
```
Mostrar solo:
├─ Reportes con alertas
├─ Tendencias significativas  
├─ Objetivos no cumplidos
└─ Mejores rendimientos
```

### Presentación de Resultados de Búsqueda

#### Layout de Resultados Estándar
```
Resultados para "pulgón tomate" (1.2 segundos - 24 resultados)

Resultados prioritarios:
ALERTA ACTIVA: Pulgón detectado en Lote A - hace 2 horas
Guía: Control de Pulgón en Tomate - 95% relevancia
Comunidad: "Eliminé pulgones con jabón potásico" - 47 

Todos los resultados:
PLAGAS (8 resultados)
├─ Pulgón Verde del Tomate ⭐⭐⭐⭐⭐
├─ Pulgón Amarillo ⭐⭐⭐⭐
└─ Áfido del Tomate ⭐⭐⭐

GUÍAS (12 resultados)  
├─ Control Biológico de Pulgones [ Video - 5 min]
├─ Preparación de Insecticida Casero [PDF - 2 páginas]
└─ Calendario de Tratamientos [Excel descargable]

COMUNIDAD (4 resultados)
├─ "¿Funciona el ajo para pulgones?" - 23 respuestas
└─ "Mi experiencia con neem en tomates" - 15 
```

### Manejo de "Sin Resultados" y Errores

#### Cuando no hay resultados exactos:
```
No se encontraron resultados para "guzano cogollero"

Sugerencias:
├─ ¿Quisiste decir "gusano cogollero"? [Buscar]
├─ Guías relacionadas con "control de gusanos"
├─ Preguntar a la comunidad sobre tu problema
└─ Contactar a un experto agrícola

Términos relacionados que podrían ayudarte:
├─ "spodoptera frugiperda" (nombre científico)
├─ "barrenador del maíz"
├─ "oruga del cogollo"
└─ "gusano soldado"
```