# CV — Sistema de 4 pasos (diagnosticar → identificar → reescribir → practicar)

Aplicado sobre tu CV actual (Valentino Pais · Full Stack Developer).

---

## PASO 1 — ATS simulado: qué te está bajando puntos

**Puntaje estimado: ~62/100.** Un ATS lo parsea, pero perdés puntos por estructura y por falta de
keywords. Esto es lo concreto que te resta, con la línea exacta:

| Problema | Dónde | Por qué baja puntos |
|---|---|---|
| **Experiencia duplicada** | "XOFTECH … 2022–Actualidad" **y** "SIMAX – Desarrollador de Aplicaciones Web … 2022–2026 (proyecto principal en Xoftech)" | Simax es el producto que hiciste *en* Xoftech, pero figura como un empleo aparte y solapado. El ATS lee dos jobs pisados y el reclutador lee relleno. **Hay que fusionarlo.** |
| **Título inconsistente** | Encabezado dice "Full Stack Developer"; la entrada de Simax dice "Desarrollador de Aplicaciones Web" | El ATS puntúa la coincidencia de *job title* con la vacante. Elegí UN título objetivo y repetilo. |
| **Sin sección Educación** | No existe | Muchos ATS tienen un campo "Education" obligatorio; si no lo encuentran, marcan el perfil como incompleto y bajan el score. Aunque sea autodidacta/cursos, tiene que haber una sección. |
| **Fechas en formatos distintos** | "2022 – Actualidad" vs "2022 – 2026" vs "2023" / "2021" | Normalizá todo a `MM/AAAA – Presente`. Ayuda al parser a calcular antigüedad. |
| **Teléfono sin formato** | "1124580224" | Poné `+54 9 11 2458-0224`. Sin código de país perdés en búsquedas internacionales. |
| **Inglés inconsistente** | CV: "Intermedio-Avanzado" · Portfolio: "Avanzado" · Audio: "fully comfortable" | Definí UNO. Para internacional, "Advanced (C1)" o "Professional working proficiency". |
| **Bullets anidados (● con ○)** | Toda la sección Experiencia | Los sub-bullets de 2 niveles algunos ATS los aplanan o rompen. Usá **un solo nivel** de viñeta. |
| **Faltan keywords de alta frecuencia** | Sección Habilidades | Ver Paso 2. El ATS matchea términos exactos; te faltan varios que casi seguro usás. |

**Lo que SÍ está bien (no lo toques):** una sola columna, PDF de texto (no imagen), contacto completo
arriba, secciones con títulos estándar, skills listadas. Eso parsea bien.

---

## PASO 2 — Recruiter: qué te falta vs cientos de vacantes parecidas

Comparado con avisos típicos de **.NET Full-Stack / Software interno** (LATAM + internacional), estos
términos aparecen una y otra vez y en tu CV **no figuran**. Divididos en dos grupos:

**A) Casi seguro lo usás pero NO lo decís → agregalo ya (gratis):**
- **Git / control de versiones** (aparece en ~90% de las vacantes y no está)
- **ASP.NET / ASP.NET Core** (escribís ".NET MVC" suelto; el término que matchea es "ASP.NET MVC" / "ASP.NET Core")
- **Entity Framework** (u ORM) — si tocaste SQL desde .NET, casi seguro lo usaste
- **API REST** (lo tenés ✓, pero sumá "diseño de APIs", "Swagger/OpenAPI" si corresponde)
- **Metodologías ágiles / Scrum**
- **Trabajo en equipo / code review / comunicación con cliente** (soft skills que el ATS y el humano buscan)

**B) Gaps reales a cubrir o aclarar (si no los tenés, son tu hoja de ruta de aprendizaje):**
- **Testing** (unit tests, xUnit/NUnit) — muy pedido, rara vez en CVs junior/semi
- **Cloud** (Azure es el natural para .NET; o AWS) — gran diferenciador
- **CI/CD** (pipelines, GitHub Actions/Azure DevOps)
- **Docker / contenedores**
- **Framework front moderno** — hoy usás jQuery, que señala "legacy". Si sabés algo de React/Angular/Blazor, ponelo; si no, es lo próximo a aprender para no quedar etiquetado solo en stack viejo.
- **Certificación** — una Microsoft (ej. AZ-204) te sube muchísimo el match en roles .NET.

> Prioridad: el grupo A es puntaje gratis (agregás términos verdaderos hoy). El grupo B es tu plan
> de estudio para los próximos meses — y cada uno que sumes, lo metés al CV.

---

## PASO 3 — Reescritor: cada línea con la fórmula XYZ de Google

Fórmula: **"Logré [X, resultado medible] medido por [Y, la métrica] haciendo [Z, lo que hiciste]."**
Dejé los números entre `[corchetes]` para que los completes con datos reales o estimaciones honestas
(no inventes; una estimación razonable está bien: "~", "+", "miles de").

### Perfil profesional (reescrito)
```
Desarrollador Full-Stack con +5 años construyendo y modernizando software interno de gestión e
integraciones para empresas. Especializado en ASP.NET MVC / C# y SQL, con sistemas en producción
usados por organizaciones reales —incluida una plataforma de firma digital de escala nacional—.
Foco en UI/UX y en resolver integraciones que la mayoría evita (firma digital, hardware, puentes
nativo↔web). Sumando capas de IA (LLMs/RAG) sobre datos internos.
```

### Experiencia — Xoftech · Desarrollador Full-Stack · 05/2022 – Presente
*(acá se fusiona la entrada duplicada de "SIMAX")*
```
• Desarrollé Simax, plataforma de mesa de ayuda usada por [N] empresas/[N] agentes, reduciendo el
  tiempo de gestión de incidentes en [X%] mediante ticketing, seguimiento de SLA, escalamientos y
  gestión de clientes en ASP.NET MVC + SQL Server/MySQL.
• Entregué SIACC, sistema de firma digital en producción para un organismo de escala nacional,
  habilitando la firma de [N] documentos/mes mediante una API REST, una extensión de Chrome propia
  conectada a un ejecutable nativo en C# e integración con hardware ePass para validar certificados.
• Reduje [tiempo de carga / errores] en [X%] optimizando rendimiento y seguridad del front y back end.
• Mejoré la experiencia de usuario de las herramientas internas rediseñando [pantallas clave],
  bajando [consultas a soporte / clicks por tarea] en [X%].
```

### Experiencia — Telesmart S.A. · Desarrollador Full-Stack · 2023
```
• Construí un display de monitoreo en tiempo real para operaciones de fibra óptica, dándole al equipo
  de operaciones visibilidad de [N] procesos/enlaces en una sola pantalla.
• Automaticé [proceso interno], ahorrando ~[X horas/semana] de trabajo manual al área.
```

### Experiencia — KanuSur · Desarrollador de Software y Apps · 2021
```
• Lancé un sistema de licencias que habilitó la venta de contenido audiovisual protegido, soportando
  [N] licencias/usuarios mediante una web de venta y una app Android de canje y reproducción.
```

### Educación (AGREGAR — sección que hoy falta)
```
[Título / Tecnicatura / Carrera en curso] — [Institución], [año o "en curso"]
Cursos relevantes: [.NET, etc.]   ·   (Opcional) Certificación: [Microsoft AZ-204 — en progreso]
```

### Habilidades (reescritas con los keywords del Paso 2)
```
Lenguajes: C#, JavaScript, SQL, HTML, CSS
Back-end: ASP.NET MVC, ASP.NET Core, APIs REST, Entity Framework, arquitectura cliente-servidor
Front-end: JavaScript, jQuery, UI/UX  [+ React/Angular/Blazor si aplica]
Datos: SQL Server, MySQL
DevOps/Tools: Git, [CI/CD, Docker, Azure — a medida que los sumes]
Integraciones: Firma digital, Chrome Extensions, hardware ePass, puentes nativo↔web
IA: LLMs, RAG, agentes (en desarrollo) · GitHub Copilot, Claude
Metodologías: Scrum / Ágil
Idiomas: Español (nativo), Inglés (Avanzado / C1)
```

> Lo mismo aplicá al **portfolio**: unificá el nivel de inglés a "Avanzado", y en los tiles de proyectos
> cambiá la descripción de tarea por resultado (mismo criterio XYZ).

---

## PASO 4 — Hiring manager: entrevista técnica (respondé y te califico 1-10)

Te dejo 7 preguntas duras de tu área. **Respondé las que quieras (de a una o varias)** y en el próximo
mensaje te pongo nota 1-10 a cada una con feedback de qué faltó para llegar a 10. Después iteramos.

**Rúbrica:** 1-3 vago/incorrecto · 4-6 correcto pero superficial · 7-8 sólido con ejemplo concreto ·
9-10 profundo, con trade-offs y experiencia real.

1. **C# / EF:** ¿Diferencia entre `IEnumerable` e `IQueryable` y por qué importa al consultar la base con Entity Framework?
2. **ASP.NET MVC:** Contame el ciclo de vida de un request y cómo funciona el model binding. ¿ViewBag vs ViewData vs modelo fuertemente tipado?
3. **SQL:** Tenés una consulta lenta en producción. ¿Cómo la diagnosticás y qué hacés? (índices, plan de ejecución, N+1).
4. **Seguridad (tu caso real):** En SIACC, la extensión de Chrome habla con un ejecutable nativo para firmar con ePass. ¿Cómo evitás que una página maliciosa dispare una firma? ¿Qué validás?
5. **Firma digital:** ¿Por qué se firma el *hash* del documento y no el documento entero? ¿Qué garantiza eso?
6. **Concurrencia:** Dos agentes editan el mismo incidente a la vez en Simax. ¿Cómo evitás que uno pise los cambios del otro? (concurrencia optimista, rowversion).
7. **Capa de IA:** Querés un asistente que responda sobre los tickets internos sin alucinar. ¿Cómo lo armás? (RAG, embeddings, grounding, citar fuentes).

---

### El loop
Diagnosticar (Paso 1) → identificar lo que falta (Paso 2) → reescribir como resultado (Paso 3) →
practicar la defensa (Paso 4). Cada vuelta, tu CV y tus respuestas quedan más afiladas.
