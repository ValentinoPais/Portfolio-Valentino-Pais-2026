# Preparación entrevista micro1: Backend C#/.NET

Tenés tiempo hasta el **5 de agosto 01:33 pm**, así que no hay apuro. Leé esto tranquilo, y cuando estés listo la hacés. Lo importante primero: vos hacés esto hace 5 años. La entrevista no te pide que sepas cosas nuevas, te pide que expliques lo que ya hacés. Eso es todo.

---

## 1. Qué es y qué esperar

Es una entrevista con una IA que se llama **Zara**. Habla por voz, te hace preguntas en voz alta y vos le respondés hablando al micrófono. Escucha lo que decís y te repregunta según tu respuesta, como una charla real.

Son dos partes, hasta 53 minutos en total:

1. **Charla técnica hablada** (unos 20-22 min): Zara te hace preguntas abiertas sobre C#/.NET, APIs, bases de datos, y algunas de situación ("cómo resolverías tal cosa"). No hay opción múltiple, respondés hablando.
2. **Ejercicio de código** (unos 25-30 min): resolvés un problema de programación mientras compartís pantalla. Te graban pantalla y cámara para que nadie haga trampa.

**Dos cosas clave:**

- **Es en inglés.** Zara habla y entiende inglés. Ya tenés el nivel (tu CV y portfolio están en inglés). Más abajo te dejo cómo manejarlo sin trabarte.
- **Zara va rápido y no te dice si respondiste bien.** Cambia de tema sin darte señales. Es normal, no significa que lo hiciste mal. No te pongas nervioso por eso.

---

## 2. Checklist antes de empezar

- Lugar en silencio (esperá a que terminen en tu casa).
- Internet estable, en la compu (no en el celular).
- Micrófono y cámara funcionando, dale permiso cuando te lo pida.
- Prepará el navegador para compartir pantalla.
- Tené a mano: agua, tu CV abierto por si querés mirar fechas, y un editor de código listo (VS Code o el que uses).
- Andá al baño antes. Son 50 min sin cortes cómodos.

---

## 3. Parte 1: la charla con Zara

Casi seguro arranca con preguntas de presentación y motivación, después va a lo técnico. Te dejo guiones que podés decir tal cual (adaptalos a tu voz).

### "Tell me about yourself"
Preparalo, es la primera y marca el tono. Algo así (45 segundos):

> "I'm a full-stack developer with 5 years of experience, mostly backend with C# and .NET. Right now I'm building Inteliax at Telesmart, a computer vision project using Python, YOLO and OpenCV. Before that I spent about 4 years at Xoftech building web applications end to end: backend APIs with .NET, SQL databases, and the frontend. I'm self-taught, I learn by building real things, and I'm comfortable owning a feature from the database to the API to the UI."

### "Why do you want this role / why micro1"
> "I want to work on frontier AI while using my backend strengths. I've been getting into computer vision with Inteliax, and micro1 lets me combine that interest with what I'm best at, which is C# and .NET. And it's remote, which is how I want to work."

### "Tell me about a hard problem you solved"
Elegí uno real y contalo con estructura: qué pasaba, qué hiciste, cómo terminó. Opciones tuyas: una integración complicada en Xoftech, un problema de performance en una consulta lenta, o el laburo de visión por computadora en Inteliax. Cualquiera sirve si es verdad y lo contás claro.

### Pregunta de soft skills (ejemplo: "un desacuerdo con un compañero")
Usá el molde **STAR**: Situación, Tarea, Acción, Resultado. Corto y concreto. No hace falta que sea épico, alcanza con que muestre que escuchás y resolvés.

---

## 4. Las 5 áreas técnicas

Estas son las 5 áreas que el aviso dice que van a tocar. Para cada una: qué te pueden preguntar, cómo lo respondés con lo que ya hacés, y qué conviene repasar. Todo esto ya lo sabés de laburar, es solo ponerle nombre.

### A) C# y .NET backend
**Te pueden preguntar:** cómo estructurás una app .NET, qué es inyección de dependencias, async/await, LINQ, el pipeline de middleware.

**Cómo respondés:** contás que estructurás en capas (controllers, services, repositorios), usás inyección de dependencias del contenedor de .NET, Entity Framework para la base, y async/await para las llamadas a base de datos y APIs.

**Repasá poder explicar en palabras simples:**
- **Inyección de dependencias:** registrás los servicios y los recibís por constructor, así el código queda desacoplado y testeable.
- **async/await:** para operaciones de entrada/salida (base de datos, HTTP) para no bloquear el hilo y aguantar más carga.
- **Middleware:** la request pasa por una cadena ordenada (autenticación, logueo, manejo de errores, routing).
- **IEnumerable vs IQueryable:** IEnumerable trabaja en memoria; IQueryable se traduce a SQL y se ejecuta en la base.

### B) Diseño de APIs REST e integración
**Te pueden preguntar:** diseñá una API REST para tal cosa, principios REST, cómo versionás, cómo autenticás, cómo se comunican dos servicios.

**Cómo respondés:** URLs por recurso (sustantivos, `/api/clientes/{id}`), verbos correctos (GET, POST, PUT, PATCH, DELETE), códigos de estado (200, 201, 400, 401, 404, 500), JWT para autenticación.

**Repasá:**
- **REST:** sin estado (stateless), recursos como sustantivos, verbos estándar, códigos de estado correctos.
- **Idempotencia:** GET, PUT y DELETE son idempotentes; POST no.
- **Autenticación:** tokens JWT, `[Authorize]`, roles y claims.
- **Integración:** sincrónica (un servicio llama a otro por HTTP) vs asincrónica (cola de mensajes tipo RabbitMQ, que desacopla y aguanta caídas). Webhooks para avisar de eventos.
- **Extras que suman:** paginación en listas largas, versionado (por URL o header), manejo de errores con un formato de respuesta consistente.

### C) MySQL (diseño de esquema y optimización de consultas)
**Te pueden preguntar:** diseñá un esquema para tal cosa, cómo optimizás una consulta lenta, cuándo usás índices, qué es el problema N+1.

**Cómo respondés:** normalizás el esquema, ponés claves primarias y foráneas, e índices en las columnas por las que filtrás o hacés join. Para una consulta lenta: mirás el plan con `EXPLAIN`, agregás el índice que falta, evitás `SELECT *` y evitás el N+1.

**Repasá:**
- **Normalización:** separar datos para no repetirlos; denormalizar a veces para leer más rápido (es un trade-off).
- **Índices:** aceleran las lecturas, hacen más lentas las escrituras. Van en columnas de WHERE, JOIN y ORDER BY. Índice compuesto para varias columnas juntas.
- **EXPLAIN:** te muestra cómo la base ejecuta la consulta, para ver dónde está el problema.
- **Problema N+1:** cuando el ORM hace una consulta por cada fila en un loop. Se arregla con carga anticipada (Include en EF) o un join.
- **Transacciones y ACID:** un grupo de operaciones que pasan todas o ninguna.

### D) Performance, escalabilidad y mantenibilidad
**Te pueden preguntar:** cómo escalás un sistema, estrategias de cache, monolito vs microservicios, cómo mantenés el código sano.

**Cómo respondés:** primero medís, no adivinás. Encontrás el cuello de botella (casi siempre una consulta a la base o una llamada externa) y ahí atacás: índice, cache, o hacerlo async. Para escalar, sumás instancias detrás de un balanceador y mantenés los servicios sin estado.

**Repasá:**
- **Escalar vertical** (máquina más grande) **vs horizontal** (más máquinas + balanceador). Lo horizontal necesita servicios sin estado (stateless).
- **Cache:** en memoria (MemoryCache) o distribuida (Redis) para no pegarle a la base todo el tiempo. Lo difícil es invalidar el cache a tiempo.
- **Monolito vs microservicios (respondé honesto):** "La mayoría de lo que construí fue monolítico o modular, que es más simple de desarrollar y desplegar. Los microservicios sirven cuando necesitás escalar o desplegar partes por separado, pero suman complejidad: llamadas por red, datos distribuidos, debugging más difícil. Los usaría cuando la escala lo justifique, no antes." Esa respuesta madura vale más que tirar palabras.
- **Mantenibilidad:** código en capas, nombres claros, tests, documentación.

### E) Debugging en producción, troubleshooting y documentación
**Te pueden preguntar:** cómo debuggeás un problema intermitente en producción (esta es casi segura, es la pregunta estrella de ellos), cómo documentás.

**Cómo respondés, con este orden:** observo (logs y métricas), aíslo (qué servicio, qué endpoint, la base?), formo una hipótesis, la pruebo, arreglo, y dejo monitoreo para que salte antes la próxima vez.

**Repasá:**
- **Logueo estructurado** y un ID de correlación para seguir una request entre servicios.
- **Causas típicas de problemas intermitentes:** picos de carga, condiciones de carrera, se agota el pool de conexiones, una dependencia externa lenta, o una fuga de memoria.
- **Documentación:** Swagger/OpenAPI para las APIs, un README para levantar el proyecto, y comentarios que expliquen el "por qué", no el "qué".

---

## 5. Parte 2: el ejercicio de código

Después de la charla pasás a programar. Compartís pantalla, te graban. Suele ser un problema práctico, no un acertijo raro. Un ejemplo real que dieron: **construir un editor de texto** con insertar, borrar, deshacer y rehacer. O sea, diseñar una clase con métodos, que es justo lo que hacés todos los días.

**Cómo encararlo (esto importa más que resolverlo perfecto):**

1. **Leé el problema y repetilo con tus palabras** en voz alta, para confirmar que entendiste.
2. **Aclará supuestos hablando:** "I'll assume the input is..." Preguntá lo que no esté claro.
3. **Empezá simple:** una solución que funcione, aunque no sea la óptima. Después mejorás.
4. **Pensá en voz alta todo el tiempo.** Zara evalúa cómo pensás, no solo el resultado. No te quedes callado.
5. **Probá con un ejemplo** al final y revisá los casos borde (lista vacía, valor nulo, etc.).
6. **Podés usar C#.** Repasá que te salga fluido lo básico: listas, diccionarios, loops, manejo de strings.

Si no llegás a terminar, no es el fin del mundo. Un razonamiento claro cuenta muchísimo.

---

## 6. Frases útiles en inglés

Para no trabarte cuando hablás. Es normal pausar y pensar, no pasa nada.

- Para ganar tiempo: *"That's a good question, let me think for a second."*
- Para estructurar: *"There are a few things to consider. First... and second..."*
- Si no entendiste: *"Could you repeat that?"* o *"Just to make sure I understand, are you asking about...?"*
- Para ser honesto sin quedar mal: *"I haven't used that directly, but here's how I'd approach it..."*
- En el código: *"I'll start with a simple version and then improve it."*

Hablá lento y claro. No trates de sonar rebuscado, tratá de que se entienda.

---

## 7. Mentalidad (leé esto antes de arrancar)

- **No inventes.** Zara repregunta. Si tirás una palabra que no sabés sostener, se nota. Si no usaste algo, decilo y contá cómo lo encararías o qué usaste parecido. La honestidad con razonamiento gana siempre.
- **Este puesto es tu fuerte.** Es backend C#/.NET, 5 años haciendo exactamente esto. Si toca frontend, sé honesto: tu fuerte es el backend, hiciste front con JavaScript, y estás sumando TypeScript y frameworks. Pero el foco va a estar en lo tuyo.
- **Está bien no salir perfecto.** Es tu primera entrevista así. Aunque no quede, ya la próxima la hacés con menos nervios. Es práctica real.
- **Lo peor que puede pasar es que salga mal, y eso no te saca nada que no tengas ahora.** Salí a jugarla tranquilo.

Cualquier cosa antes de arrancar, me escribís. Suerte, la tenés más controlada de lo que pensás.
