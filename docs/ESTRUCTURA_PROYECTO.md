# Estructura del Proyecto

## Descripcion General
Proyecto Angular para auditoria de configuracion de software.

## Estructura de Directorios

```
auditoria_configuracion/
├── .github/                    # Configuracion de GitHub
│   └── PULL_REQUEST_TEMPLATE.md
├── docs/                       # Documentacion del proyecto
│   ├── ESTRUCTURA_PROYECTO.md
│   └── REQUISITOS.md
├── public/                     # Archivos publicos estaticos
├── src/                        # Codigo fuente
│   ├── app/                    # Componentes de la aplicacion
│   │   ├── app.config.ts
│   │   ├── app.css
│   │   ├── app.html
│   │   ├── app.routes.ts
│   │   ├── app.spec.ts
│   │   └── app.ts
│   ├── index.html
│   ├── main.ts
│   └── styles.css
├── .env.example                # Ejemplo de variables de entorno
├── .gitignore                  # Archivos ignorados por Git
├── angular.json                # Configuracion de Angular
├── CHECKLIST_AUDITORIA.md      # Checklist de auditoria
├── LICENSE                     # Licencia del proyecto
├── package.json                # Dependencias del proyecto
├── README.md                   # Documentacion principal
├── tsconfig.app.json           # Configuracion TypeScript app
├── tsconfig.json               # Configuracion TypeScript
└── tsconfig.spec.json          # Configuracion TypeScript tests
```

## Elementos de Configuracion (Configuration Items)

### 1. Archivos de Configuracion
- `package.json`: Dependencias y scripts
- `angular.json`: Configuracion de Angular CLI
- `tsconfig.*.json`: Configuracion de TypeScript
- `.env.example`: Variables de entorno

### 2. Documentacion
- `README.md`: Documentacion principal
- `LICENSE`: Licencia MIT
- `CHECKLIST_AUDITORIA.md`: Controles de calidad
- `docs/`: Documentacion adicional

### 3. Codigo Fuente
- `src/app/`: Componentes de aplicacion
- `src/main.ts`: Punto de entrada
- `src/styles.css`: Estilos globales

### 4. Control de Version
- `.gitignore`: Exclusiones de Git
- `.github/`: Templates y workflows

## Versionado
El proyecto sigue versionado semantico (SemVer):
- MAJOR.MINOR.PATCH
- Ejemplo: v1.0.0

## Tecnologias Utilizadas
- Angular 21.0.0
- TypeScript 5.9.2
- Vitest 4.0.8
- RxJS 7.8.0

## Comandos Principales

```bash
# Instalar dependencias
npm install

# Servidor de desarrollo
npm start

# Ejecutar tests
npm test

# Build de produccion
npm run build
```

## Convenciones de Codigo
- Usar TypeScript strict mode
- Seguir guia de estilo de Angular
- Prettier configurado para formato automatico
- Tests unitarios con Vitest
