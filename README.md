# Auditoria de Configuracion

Proyecto Angular para la practica de auditoria de configuracion y release controlado.

## Descripcion

Este proyecto implementa los principios de auditoria de configuracion, gestion de versiones y trazabilidad, aplicando controles de calidad y procesos de revision para garantizar la integridad del software.

## Estructura del Proyecto

Ver documentacion detallada en [docs/ESTRUCTURA_PROYECTO.md](docs/ESTRUCTURA_PROYECTO.md)

```
auditoria_configuracion/
├── .github/                    # Templates de GitHub
├── docs/                       # Documentacion
│   ├── ESTRUCTURA_PROYECTO.md
│   ├── REQUISITOS.md
│   └── TRAZABILIDAD.md
├── src/                        # Codigo fuente
├── CHECKLIST_AUDITORIA.md      # Controles de calidad
├── GUIA_PASO_A_PASO.md         # Guia de implementacion
├── LICENSE                     # Licencia MIT
└── README.md                   # Este archivo
```

## Servidor de Desarrollo

Para iniciar el servidor local, ejecutar:

```bash
npm install
npm start
```

Navegar a `http://localhost:4200/`. La aplicacion se recargara automaticamente al modificar archivos fuente.

## Construccion del Proyecto

Para construir el proyecto:

```bash
npm run build
```

Los artefactos se almacenaran en el directorio `dist/`. Por defecto, la construccion de produccion optimiza la aplicacion.

## Ejecucion de Tests

Para ejecutar los tests unitarios con Vitest:

```bash
npm test
```

## Proceso de Auditoria

Este proyecto implementa un proceso completo de auditoria de configuracion:

1. **Auditoria Fisica**: Verificacion de elementos de configuracion
2. **Auditoria Funcional**: Validacion de requisitos
3. **Gestion de Trazabilidad**: Control de referencias entre issues, PRs y commits
4. **Release Controlado**: Versionado semantico y notas de release

Ver [CHECKLIST_AUDITORIA.md](CHECKLIST_AUDITORIA.md) para los controles de calidad.

Ver [GUIA_PASO_A_PASO.md](GUIA_PASO_A_PASO.md) para el proceso completo.

## Convenciones

### Commits
Formato: `tipo: descripcion (#issue)`

Tipos: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

### Branches
- `feature/descripcion`: Nuevas funcionalidades
- `audit/descripcion`: Tareas de auditoria
- `docs/descripcion`: Documentacion
- `fix/descripcion`: Correcciones

### Pull Requests
- Minimo 1 revisor
- Usar template en `.github/PULL_REQUEST_TEMPLATE.md`
- Vincular issue correspondiente

## Requisitos

- Node.js 18.x o superior
- npm 11.x o superior
- Angular CLI 21.x

## Licencia

MIT - Ver [LICENSE](LICENSE)

## Equipo

- Auditor Fisico: Verificacion de configuracion
- Auditor Funcional: Validacion de requisitos
- Gestor de Trazabilidad: Control de versiones y referencias

## Documentacion Adicional

- [Estructura del Proyecto](docs/ESTRUCTURA_PROYECTO.md)
- [Requisitos del Sistema](docs/REQUISITOS.md)
- [Tabla de Trazabilidad](docs/TRAZABILIDAD.md)
- [Checklist de Auditoria](CHECKLIST_AUDITORIA.md)

## Versionado

Este proyecto sigue [Semantic Versioning](https://semver.org/):
- MAJOR.MINOR.PATCH
- Version actual: 1.0.0

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Vitest](https://vitest.dev/) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.
