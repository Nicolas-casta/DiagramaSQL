## Taller Práctico: Creación de un Diagrama MER

### Objetivos del taller

1. Identificar y modelar entidades y atributos en un escenario realista.
2. Definir relaciones y cardinalidades entre entidades.
3. Dibujar un Diagrama Entidad-Relación (MER) completo y coherente.
4. Comprender la importancia de las llaves primarias y foráneas.

------

### Descripción del escenario

Imagina que debes diseñar la base de datos para la gestión de cursos universitarios. El sistema debe almacenar información sobre los estudiantes, los cursos que ofrece la universidad y los profesores que imparten dichos cursos. Además, deberá registrar las inscripciones de los estudiantes en cada curso.

### Paso 1: Identificación de entidades y atributos

1. **Entidades propuestas** (mínimo 3):
   - **Estudiante**: almacena datos de los alumnos.
   - **Curso**: información de cada asignatura.
   - **Profesor**: datos del docente.
   - **(Opcional)** Departamento: unidad académica que organiza cursos.
2. **Atributos**: Para cada entidad, define al menos 4 atributos relevantes; por ejemplo:
   - **Estudiante**: `id` (PK), `nombre`, `apellido`, `fechaNacimiento`, `email`.
   - **Curso**: `id` (PK), `nombre`, `creditos`, `semestre`.
   - **Profesor**: `id` (PK), `nombre`, `apellido`, `departamento`.
   - **Departamento**: `id` (PK), `nombre`, `edificio`.

### Paso 2: Definición de relaciones y cardinalidades

1. **Inscripción**: relación entre Estudiante y Curso.
   - Un estudiante puede inscribirse en varios cursos.
   - Un curso puede tener muchos estudiantes.
   - Identifica atributos de la relación, por ejemplo: `FechaInscripcion`, `NotaFinal`.
2. **Imparte**: relación entre Profesor y Curso.
   - Un profesor puede impartir muchos cursos.
   - Un curso puede ser impartido por uno o varios profesores (según tu modelo).
3. **(Opcional)** Relación Departamento–Curso:
   - Un departamento ofrece varios cursos.
   - Cada curso pertenece a un único departamento.

Indica la cardinalidad de cada relación (1:1, 1:N, N:M) y, si corresponde, resuélvelas mediante entidades intermedias (en caso de N:M).

### Paso 3: Diagrama MER en MySQL Workbench

- Abre MySQL Workbench y crea un nuevo modelo EER.
- Agrega las entidades identificadas desde la paleta de herramientas.
- Añade atributos a cada tabla marcando PK y FK según corresponda.
- Establece las relaciones (líneas) arrastrando de llave foránea a primaria, definiendo cardinalidades.

### Paso 4: Entregables

1. Archivo del modelo MySQL Workbench (.mwb) con el Diagrama MER completo.
2. Exportación gráfica del diagrama (PNG, JPG o PDF).
3. Documento breve (máx. 1 página) explicando:
   - Qué entidades y relaciones definiste y por qué.
   - Justificación de las cardinalidades.

### Criterios de evaluación

| Aspecto                                 | Puntaje | Detalle                                                      |
| --------------------------------------- | ------- | ------------------------------------------------------------ |
| Identificación de entidades y atributos | 30%     | Entidades relevantes y al menos 4 atributos cada una.        |
| Relaciones y cardinalidades             | 30%     | Relaciones correctas, cardinalidades definidas en MySQL Workbench. |
| Diagrama MER en Workbench               | 30%     | Uso adecuado de herramientas, llaves indicadas y claridad visual. |
| Documentación explicativa               | 10%     | Coherencia y justificación de decisiones.                    |



¡Mucho éxito en la creación de su Diagrama MER! Cualquier duda, pregúntenme en clase o en el foro de la asignatura.