# Direccion de Gobierno Digital DevOps Desafío

## Prólogo

Este desafío está destinado a ver cómo abordaría un problema y no a ver
qué tan bien entrega una solución que creemos que es correcta. No debes concentrarte en
obteniendo _la respuesta_ "correcta".

- Las **Instrucciones** a continuación son pasos generales para comenzar.

- La sección **Desafío** tiene más problemas abiertos para que los resuelvas en de la forma que creas conveniente.

  Para cada desafío enumerado a continuación, puede proponer su enfoque, siempre es una ventaja si puede ejecutar su propuesta. Algunos desafíos se publican como abiertos. preguntas y puedes responderlas en línea.

  Se estima que los desafíos toman entre **2 - 8 horas** dependiendo de qué tan familiarizado usted está con la tecnología de contenerización. El tiempo de investigación también se contabiliza en la duración estimada.

## Instrucciones

1. Descargue este repositorio y, usándolo como base, cree un nuevo repositorio **privado**.
2. Proporcione sus respuestas en su repositorio generado.
3. Una vez que su repositorio esté listo para su revisión, puede agregar al usuario `` como colaborador
   para su repositorio.
4. Espera nuestra respuesta.

## Estructura del repositorio

El Stack de la aplicaciones de ejemplo es un sitio de blogs sociales (es decir, un clon de Medium.com) llamado "Conduit". Utiliza una API personalizada para todas las solicitudes, incluida la autenticación.

**En este repositorio, usted encontrará:**

- [./api](./api):

  - Especificación de API y algunas utilidades para probar el backend.

- [./src/frontend](./src/frontend):

  - Código fuente para la aplicación de interfaz de usuario de interfaz de usuario usando React.js. Puedes leer más al respecto en [./src/frontend/README.md](./src/frontend/README.md).
  - Localmente, la aplicación se ejecuta en http://localhost:4100

- [./src/backend.v1](./src/backend.v1):

  - Código fuente para el código del servidor backend heredado. Esto está escrito en Golang, y puedes leer más al respecto en [./src/backend.v1/readme.md](./src/backend.v1/readme.md).
  - Localmente, la aplicación se ejecuta en http://localhost:8080

- [./src/backend.v2](./src/backend.v2):

  - Código fuente para el nuevo código del servidor backend que aún estamos desarrollando. Esto está escrito en .NET Core, y puede leer más al respecto en [./src/backend.v2/readme.md](./src/backend.v2/readme.md).
  - Localmente, la aplicación se ejecuta en http://localhost:5000

## Desafío

Los siguientes desafíos están relacionados con el repositorio. Para dar su opinión sobre el
desafíos, recuerde enviar sus respuestas a su repositorio.

### 1. ¿Podemos contenerizar estos servicios?

Hemos escuchado cosas buenas docker y pensamos qué pasaría si traemos a nuestra stack de aplicaciones.
¿Puedes ayudar a Dockerizar `frontend`, `backend.v1` y `backend.v2`?

Hemos proporcionado un `Dockerfile` básico en la carpeta de cada servicio para ayudarlo a comenzar.

### 2. ¿Podemos automatizar la construcción del contenedor?

Actualmente, nuestros desarrolladores tienen que ejecutar manualmente `docker build` después de realizar cambios. ¿Puedes escribir un Docker Composer para automatizar el proceso de compilación y comenzar un nuevo contenedor con la imagen actualizada?

### 3. ¿Has oído hablar de Kubernetes?

[Kubernetes](https://kubernetes.io/) parece una gran herramienta para ayudarnos con la implementación, el escalado y la administración de estos servicios en contenedores.

¿Puede crear un archivo `yaml` para cada servicio con los recursos necesarios de Kubernetes que nos permitirá escalarlos en el futuro?

### 4. ¿Has oído hablar de Infraestructura como código?

La infraestructura como código (IaC) es muy popular.

[Terraform](https://www.terraform.io/) es una infraestructura de código abierto como herramienta de código desarrollada por HashiCorp.

¿Puede crear un archivo `tf` para realizar el despliegue del cluster de kubernetes creado en el paso anterios?

**Es bueno tener:** Sería una demostración genial para nuestras partes interesadas si pudiéramos poner las aplicaciones en línea y pudieran acceder a ellas desde su computadora.
Está bien si es solo una dirección IP o un nombre de dominio aleatorio.
