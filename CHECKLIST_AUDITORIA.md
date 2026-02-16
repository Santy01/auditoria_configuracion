# Checklist de Auditoria de Configuracion

## Objetivo
Este documento define los controles minimos para garantizar la integridad, trazabilidad y calidad del proyecto.

## Reglas de Control

### 1. Revision por Pull Request
- Todo cambio debe pasar por un Pull Request
- Minimo 1 revisor debe aprobar antes del merge
- El autor del PR no puede aprobar su propio PR

### 2. Referencias y Trazabilidad
- Cada issue debe tener un responsable asignado
- Cada branch debe referenciar un issue
- Cada commit debe incluir referencia al issue (#numero)
- Cada PR debe vincular el issue correspondiente

### 3. Convencion de Mensajes de Commit
Formato: `tipo: descripcion (#issue)`

Tipos permitidos:
- `feat`: Nueva funcionalidad
- `fix`: Correccion de errores
- `docs`: Cambios en documentacion
- `style`: Formato, espacios, punto y coma
- `refactor`: Refactorizacion de codigo
- `test`: Agregado de tests
- `chore`: Tareas de mantenimiento

Ejemplo: `fix: agregar estructura de directorios faltante (#1)`

#### Ejemplos de Commits Validos
```bash
fix: agregar seccion de elementos verificados en README (#1)
fix: completar documentacion de estructura del proyecto (#1)
fix: agregar comentarios explicativos en .env.example (#1)
fix: marcar items verificados en checklist de auditoria (#1)
fix: iniciar validacion de requisito RF-001 (#2)
fix: capturar evidencia de aplicacion ejecutandose (#2)
fix: actualizar criterios de aceptacion validados (#2)
fix: completar validacion funcional de RF-001 (#2)
fix: agregar ejemplos de commits en checklist (#3)
fix: mejorar checklist en template de PR (#3)
fix: actualizar tabla de trazabilidad con datos reales (#3)
fix: documentar proceso completo de trazabilidad (#3)
```

Todos los commits deben:
- Comenzar con el tipo en minusculas
- Tener descripcion clara y concisa
- Incluir referencia al issue entre parentesis
- No exceder 72 caracteres en el titulo

### 4. Convencion de Nombres de Branch
- `feature/descripcion-corta`: Para nuevas funcionalidades
- `audit/descripcion-corta`: Para tareas de auditoria
- `docs/descripcion-corta`: Para documentacion
- `fix/descripcion-corta`: Para correcciones

### 5. Checklist antes de Merge
Antes de hacer merge a main, verificar:

- [ ] El PR tiene descripcion clara del cambio
- [ ] El PR referencia el issue correspondiente
- [ ] Los commits tienen el formato correcto
- [ ] Al menos 1 revisor aprobo el PR
- [ ] No hay archivos sensibles (secrets, .env con datos reales)
- [ ] Los cambios son consistentes con el objetivo del issue
- [ ] La documentacion esta actualizada si aplica

### 6. Linea Base (Branch Main)
- Solo se hace merge a main desde PR aprobados
- Todo release se crea desde main
- No se hacen commits directos a main

### 7. Verificacion de Artefactos
- README.md actualizado
- Estructura de directorios documentada
- Archivos de configuracion (.env.example, no .env)
- Licencia presente
- Documentacion de API/componentes si aplica

### 8. Proceso de Release
- Crear tag semantico: vX.Y.Z
- Generar release notes con:
  - Que cambio
  - Issues cerrados
  - PRs mergeados
  - Como validar
  - Instrucciones de uso

## Responsables
- Auditor Fisico: Verifica estructura y configuracion
- Auditor Funcional: Valida requisitos y casos de uso
- Gestor de Trazabilidad: Asegura referencias y convenciones

## Estado de Verificacion de Artefactos

### Auditoria Fisica - Elementos Verificados
- [X] README.md actualizado y completo
- [X] LICENSE (MIT) presente
- [X] .env.example configurado
- [X] .gitignore presente
- [X] CHECKLIST_AUDITORIA.md completo
- [X] docs/ESTRUCTURA_PROYECTO.md actualizado
- [X] docs/REQUISITOS.md presente
- [X] docs/TRAZABILIDAD.md presente
- [X] .github/PULL_REQUEST_TEMPLATE.md configurado
- [X] package.json con version correcta
- [X] Archivos de configuracion TypeScript presentes
- [X] Estructura de directorios documentada

### Verificacion Completada
Fecha: 16 de febrero de 2026
Responsable: Auditor Fisico
Estado: APROBADO
