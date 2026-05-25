# DistribucionContinua

Repositorio ejemplar para la actividad de distribución continua en DevOps

## Estructura de un Workflow

El archivo .yml es el corazón de la automatización en GitHub Actions. Consiste en 
un archivo de texto con una sintaxis específica que le dice a GitHub qué, cuándo 
y cómo ejecutar tareas de forma automática.

### Componentes principales

- **name**: El nombre identificable del workflow.
- **on**: El desencadenante. Define qué evento en GitHub pone en marcha el 
  workflow. Puede ser un push a una rama, la creación de un pull_request, un 
  horario programado (schedule) o incluso una ejecución manual.
- **jobs**: La sección que agrupa el trabajo o acciones a realizar. Un workflow 
  puede tener uno o varios trabajos. Por defecto, se ejecutan en paralelo para 
  ser más eficientes.
- **runs-on**: Especifica el entorno de ejecución, el sistema operativo del 
  servidor virtual donde correrá el trabajo.
- **steps**: Consiste en una serie de tareas individuales que se ejecutan de 
  forma secuencial dentro de un mismo job. Si un paso falla, los siguientes se 
  detienen (a menos que se indique lo contrario).
- **uses**: Permite reutilizar acciones predefinidas de la comunidad o de GitHub.
- **run**: Ejecuta directamente comandos de la terminal (shell) del runner.
- **with**: Se utiliza junto a uses para pasar parámetros de configuración a 
  una acción.
