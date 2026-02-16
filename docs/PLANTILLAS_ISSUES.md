# Plantillas de Issues para GitHub

## Issue 1: Auditor Fisico

**Titulo:**
```
Auditoria Fisica - Verificacion de Elementos de Configuracion
```

**Labels:** `auditoria`, `documentacion`, `configuracion`

**Asignado a:** Persona 1

**Descripcion:**
```markdown
## Objetivo
Verificar que todos los elementos de configuracion existan y esten correctamente versionados.

## Tareas
- [ ] Verificar estructura de directorios completa
- [ ] Validar archivos de configuracion (.env.example, tsconfig, angular.json)
- [ ] Revisar documentacion (README, LICENSE, ESTRUCTURA_PROYECTO.md)
- [ ] Agregar scripts de utilidad si faltan
- [ ] Actualizar documentacion de estructura

## Criterios de Aceptacion
- Todos los archivos de configuracion estan presentes
- La documentacion refleja la estructura real
- Los archivos sensibles estan en .gitignore
- Existe .env.example pero no .env con datos reales

## Rol
Auditor Fisico

## Evidencia Esperada
- 1 Pull Request con ajustes de estructura y documentacion
- 4 commits con referencias a este issue
- Checklist de verificacion completado
```

---

## Issue 2: Auditor Funcional

**Titulo:**
```
Auditoria Funcional - Validacion de Requisito RF-001
```

**Labels:** `auditoria`, `testing`, `validacion`

**Asignado a:** Persona 2

**Descripcion:**
```markdown
## Objetivo
Validar que el sistema cumple el Requisito Funcional RF-001: Visualizacion de la Aplicacion.

## Requisito a Validar
**RF-001:** El sistema debe permitir visualizar la interfaz principal de la aplicacion Angular.

## Criterios de Aceptacion
1. La aplicacion inicia correctamente con npm start
2. La interfaz es accesible en http://localhost:4200
3. Los estilos CSS se aplican correctamente

## Pasos de Validacion
- [ ] Ejecutar npm install
- [ ] Ejecutar npm start
- [ ] Verificar acceso en navegador
- [ ] Capturar evidencia (screenshot)
- [ ] Documentar resultados en docs/REQUISITOS.md
- [ ] Actualizar estado de validacion

## Rol
Auditor Funcional

## Evidencia Esperada
- 1 Pull Request con validacion y evidencias
- 4 commits con referencias a este issue
- Screenshots de la aplicacion ejecutandose
- Documentacion de pasos de validacion completada
```

---

## Issue 3: Gestor de Trazabilidad

**Titulo:**
```
Gestion de Trazabilidad - Configurar Convenciones y Referencias
```

**Labels:** `auditoria`, `proceso`, `trazabilidad`

**Asignado a:** Persona 3

**Descripcion:**
```markdown
## Objetivo
Establecer y verificar la trazabilidad entre issues, PRs, commits y releases.

## Tareas
- [ ] Verificar que CHECKLIST_AUDITORIA.md define convenciones
- [ ] Revisar plantilla de PR en .github/PULL_REQUEST_TEMPLATE.md
- [ ] Actualizar tabla de trazabilidad en docs/TRAZABILIDAD.md
- [ ] Documentar proceso de referencias cruzadas
- [ ] Validar que todos los commits sigan convencion
- [ ] Preparar documentacion para release notes

## Criterios de Aceptacion
- Convencion de commits documentada y aplicada
- Template de PR configurado y funcionando
- Referencias cruzadas funcionando (issue -> PR -> commit)
- Tabla de trazabilidad completada
- Documentacion clara del proceso

## Rol
Gestor de Trazabilidad

## Evidencia Esperada
- 1 Pull Request con mejoras de trazabilidad
- 4 commits con referencias a este issue
- Tabla de trazabilidad completa
- Documentacion de convenciones
```

---

## Instrucciones para Crear Issues en GitHub

1. Ir al repositorio en GitHub
2. Click en "Issues" -> "New issue"
3. Copiar y pegar el contenido correspondiente
4. Asignar a la persona responsable
5. Agregar los labels sugeridos
6. Crear el issue

## Orden de Creacion

1. Crear los 3 issues
2. Anotar los numeros asignados (ej: #1, #2, #3)
3. Estos numeros se usaran en los commits y PRs
