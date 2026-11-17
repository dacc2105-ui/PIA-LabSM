
# 🚁 PIA — Sistema Multiagente de Vigilancia Inteligente

## 📌 Descripción del proyecto

**Título:** Sistema Multiagente de Vigilancia Inteligente mediante Drones Cooperativos con Patrullaje y Relevos Autónomos.

El proyecto consiste en desarrollar una simulación en Python donde varios drones autónomos colaboren para vigilar una instalación industrial.

Los drones deberán patrullar diferentes sectores, compartir información, administrar su batería y realizar relevos para mantener la mayor cobertura posible.

También se evaluará el comportamiento del sistema ante fallas de drones, pérdida de mensajes y obstáculos dinámicos.

**Objetivo principal:** Maximizar la cobertura de vigilancia y reducir los puntos ciegos mediante coordinación multiagente y relevos autónomos.

### Pregunta de investigación

¿En qué medida la coordinación y los relevos autónomos entre drones permiten maximizar la cobertura de vigilancia y reducir los puntos ciegos en una instalación industrial simulada?

## Preguntas Secundarias

1. ¿Qué arquitectura de agente, reactiva o basada en modelos, permite una mejor exploración y administración de los sectores vigilados?
2. ¿Qué mecanismo de coordinación, pizarrón compartido o mensajería directa, reduce más los recorridos redundantes y los conflictos de asignación?
3. ¿Cómo influyen los niveles de batería y las estrategias de relevo en la continuidad de la vigilancia?
4. ¿Qué tan robusto es el sistema frente a fallas de drones, pérdida de mensajes y cambios en el entorno?

---

## 📁 Estructura propuesta del proyecto

```text
PIA_Drones/
│
├── main.py
├── config.py
├── requirements.txt
│
├── simulacion/
│   ├── __init__.py
│   ├── entorno.py
│   ├── cobertura.py
│   ├── agentes.py
│   ├── patrullaje.py
│   ├── coordinacion.py
│   ├── energia.py
│   ├── relevos.py
│   ├── robustez.py
│   └── motor.py
│
├── experimentos/
│   ├── ejecutar_experimentos.py
│   └── graficas.py
│
├── tests/
│   ├── test_entorno.py
│   ├── test_agentes.py
│   ├── test_coordinacion.py
│   ├── test_relevos.py
│   └── test_robustez.py
│
├── resultados/
│   ├── graficas/
│   └── animaciones/
│
└── docs/
    ├── integrante_1.md
    ├── integrante_2.md
    ├── integrante_3.md
    ├── integrante_4.md
    └── integrante_5.md
```

---

# 👥 Distribución del trabajo

## 🗺️ Integrante 1 — Entorno y cobertura

**Responsabilidad:** Construir el entorno de simulación y medir la cobertura de vigilancia.

### Actividades

- [ ] Crear el mapa industrial mediante una cuadrícula.
- [ ] Definir edificios, obstáculos y zonas transitables.
- [ ] Incorporar estaciones de recarga.
- [ ] Definir el radio de observación de los drones.
- [ ] Calcular la cobertura de vigilancia.
- [ ] Identificar puntos ciegos.
- [ ] Medir la cobertura redundante.
- [ ] Realizar pruebas y documentar resultados.

### Archivos que debe entregar

| Archivo | Contenido |
|---|---|
| `simulacion/entorno.py` | Mapa, obstáculos y sectores |
| `simulacion/cobertura.py` | Visibilidad, cobertura y puntos ciegos |
| `tests/test_entorno.py` | Pruebas del entorno |
| `docs/integrante_1.md` | Documentación y resultados |

### Experimento

Comparar la cobertura con diferentes cantidades de drones y radios de observación.

---

## 🧠 Integrante 2 — Inteligencia y patrullaje

**Práctica relacionada:** Práctica 1.

**Responsabilidad:** Implementar el comportamiento inteligente y las decisiones de movimiento de los drones.

### Actividades

- [ ] Definir los agentes autónomos.
- [ ] Implementar percepción del entorno.
- [ ] Implementar agentes reactivos.
- [ ] Implementar agentes basados en modelos.
- [ ] Incorporar memoria de sectores visitados.
- [ ] Diseñar estrategias de patrullaje.
- [ ] Seleccionar sectores por explorar o vigilar.
- [ ] Comparar ambas arquitecturas.

### Archivos que debe entregar

| Archivo | Contenido |
|---|---|
| `simulacion/agentes.py` | Agentes, percepción y memoria |
| `simulacion/patrullaje.py` | Estrategias de movimiento |
| `tests/test_agentes.py` | Pruebas de agentes |
| `docs/integrante_2.md` | Arquitecturas y resultados |

### Experimento

Comparar agentes reactivos y basados en modelos según cobertura, redundancia y eficiencia del patrullaje.

---

## 📡 Integrante 3 — Comunicación y coordinación

**Práctica relacionada:** Práctica 2.

**Responsabilidad:** Implementar la comunicación entre drones y la coordinación de sus actividades.

### Actividades

- [ ] Implementar el pizarrón compartido.
- [ ] Implementar la mensajería directa.
- [ ] Compartir información de sectores vigilados.
- [ ] Coordinar la asignación de sectores.
- [ ] Evitar asignaciones redundantes.
- [ ] Implementar solicitudes de relevo.
- [ ] Implementar confirmaciones de reemplazo.
- [ ] Evaluar retrasos de comunicación.

### Archivos que debe entregar

| Archivo | Contenido |
|---|---|
| `simulacion/coordinacion.py` | Pizarrón, mensajes y asignaciones |
| `tests/test_coordinacion.py` | Pruebas de comunicación |
| `docs/integrante_3.md` | Protocolos y resultados |

### Experimento

Comparar pizarrón compartido y mensajería directa según redundancia, retrasos y eficiencia de coordinación.

---

## 🔋 Integrante 4 — Batería y relevos inteligentes
  
**Responsabilidad:** Administrar la energía y desarrollar el algoritmo de relevos autónomos.

### Actividades

- [ ] Implementar niveles de batería.
- [ ] Simular consumo energético.
- [ ] Definir umbrales de batería baja.
- [ ] Implementar estaciones de recarga.
- [ ] Definir estados: vigilando, reserva, en relevo y cargando.
- [ ] Detectar cuándo un dron necesita ser reemplazado.
- [ ] Diseñar el algoritmo de selección del sustituto.
- [ ] Considerar batería, distancia y cobertura al seleccionar reemplazos.
- [ ] Comparar relevos fijos contra relevos inteligentes.
- [ ] Probar casos donde no exista un sustituto disponible.

### Archivos que debe entregar

| Archivo | Contenido |
|---|---|
| `simulacion/energia.py` | Consumo y recarga de batería |
| `simulacion/relevos.py` | Algoritmo de relevos autónomos |
| `tests/test_relevos.py` | Pruebas de batería y sustituciones |
| `docs/integrante_4.md` | Algoritmo, justificación y resultados |

### Experimento

Comparar turnos fijos y relevos inteligentes utilizando:

- Cobertura promedio.
- Tiempo sin vigilancia.
- Consumo energético.
- Cantidad de relevos completados.

---

## 🛡️ Integrante 5 — Robustez e integración

**Práctica relacionada:** Práctica 3.

**Responsabilidad:** Simular fallas y conectar los módulos para ejecutar el sistema completo.

### Actividades

- [ ] Implementar fallas de drones.
- [ ] Simular pérdida de mensajes.
- [ ] Incorporar obstáculos dinámicos.
- [ ] Permitir reasignación de sectores ante fallas.
- [ ] Desarrollar el ciclo principal de simulación.
- [ ] Integrar los módulos de los demás integrantes.
- [ ] Permitir configurar escenarios experimentales.
- [ ] Ejecutar pruebas de integración.
- [ ] Analizar la recuperación del sistema.

### Archivos que debe entregar

| Archivo | Contenido |
|---|---|
| `simulacion/robustez.py` | Fallas y eventos inesperados |
| `simulacion/motor.py` | Ciclo de simulación |
| `main.py` | Ejecución del proyecto |
| `tests/test_robustez.py` | Pruebas de robustez e integración |
| `docs/integrante_5.md` | Escenarios y resultados |

### Experimento

Comparar el funcionamiento normal contra escenarios con fallas, pérdida de mensajes y obstáculos dinámicos.

---

# 📊 Archivos y responsabilidades compartidas

| Archivo / Actividad | Responsable |
|---|---|
| `config.py` | Definición entre todos; mantenimiento del integrante 5 |
| `requirements.txt` | Integrante 5, con aportaciones de todos |
| `experimentos/ejecutar_experimentos.py` | Integrante 5 crea la estructura; todos aportan experimentos |
| `experimentos/graficas.py` | Integrante 1 coordina; todos validan sus resultados |
| `resultados/` | Cada integrante entrega sus evidencias |
| Reporte en Overleaf | Los cinco |
| Conclusiones individuales | Cada integrante |
| Pruebas finales | Los cinco |
| Defensa del proyecto | Los cinco |

---

# 🔄 Orden de desarrollo

## Fase 1 — Diseño general

**Responsables: Todos**

- [ ] Definir el tamaño del mapa.
- [ ] Definir cantidad inicial de drones.
- [ ] Definir cómo se representan posiciones y sectores.
- [ ] Definir estados de los drones.
- [ ] Acordar los datos que intercambiarán los módulos.
- [ ] Definir las métricas y parámetros experimentales.

## Fase 2 — Desarrollo de módulos

**Responsables: Cada integrante**

- [ ] Integrante 1: entorno y cobertura.
- [ ] Integrante 2: agentes y patrullaje.
- [ ] Integrante 3: comunicación y coordinación.
- [ ] Integrante 4: batería y relevos.
- [ ] Integrante 5: robustez y motor de simulación.

## Fase 3 — Integración

**Responsables: Todos**

- [ ] Conectar los módulos.
- [ ] Verificar compatibilidad de funciones.
- [ ] Ejecutar la simulación completa.
- [ ] Corregir errores en cada módulo.
- [ ] Verificar la medición de cobertura.
- [ ] Verificar los relevos y la recuperación ante fallas.

## Fase 4 — Experimentación

**Responsables: Todos**

- [ ] Comparar arquitecturas de agentes.
- [ ] Comparar mecanismos de coordinación.
- [ ] Comparar relevos fijos e inteligentes.
- [ ] Evaluar cobertura y puntos ciegos.
- [ ] Evaluar consumo energético.
- [ ] Evaluar fallas y recuperación.
- [ ] Generar tablas y gráficas.

## Fase 5 — Documentación y entrega

**Responsables: Todos**

- [ ] Documentar el funcionamiento de cada módulo.
- [ ] Explicar las decisiones de diseño.
- [ ] Incorporar diagramas de arquitectura.
- [ ] Presentar resultados experimentales.
- [ ] Elaborar el reporte en Overleaf.
- [ ] Incluir referencias bibliográficas.
- [ ] Redactar conclusiones individuales.
- [ ] Preparar la defensa.

---

# 📦 Entregables mínimos por integrante

Cada integrante deberá entregar:

1. Sus archivos `.py` funcionales.
2. Su archivo de pruebas `test_*.py`.
3. Su documentación en `docs/integrante_X.md`.
4. Evidencia de ejecución y resultados.
5. Explicación de las decisiones de diseño.
6. Aportación al reporte final.
7. Conclusión individual.

**Importante:** Cada integrante es responsable de corregir los errores de su módulo. La integración no significa que una sola persona deba reparar el trabajo de los demás.

---

# 🎯 Criterios de éxito del proyecto

El sistema deberá demostrar que:

- [ ] Los drones patrullan autónomamente.
- [ ] Se puede calcular la cobertura de vigilancia.
- [ ] Se identifican puntos ciegos.
- [ ] Los drones intercambian información.
- [ ] Los drones administran su batería.
- [ ] Se ejecutan relevos autónomos.
- [ ] El sistema responde a fallas.
- [ ] Se pueden comparar diferentes estrategias.
- [ ] Los resultados se presentan mediante métricas y gráficas.

**Nota:** El objetivo es maximizar la cobertura, no garantizar vigilancia perfecta ni ausencia absoluta de puntos ciegos.

---

# ⚠️ Acuerdos importantes

- Si modifican, comenten y agreguen el porque
- Acordar las interfaces de los módulos antes de programar.
- Utilizar los mismos parámetros y semillas aleatorias en comparaciones equivalentes.
- Documentar los cambios realizados.
- Subir código funcional y probado.
- No dejar la integración para el último día.

---

## 🚀 Objetivo final

Desarrollar una simulación multiagente en Python que permita estudiar cómo la cooperación, el patrullaje autónomo y los relevos inteligentes influyen en la cobertura de vigilancia, la eficiencia energética y la robustez de una instalación industrial simulada.
