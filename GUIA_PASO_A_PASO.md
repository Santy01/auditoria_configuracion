# Guia Paso a Paso - Auditoria de Configuracion

## FASE 1: CONFIGURACION INICIAL

### Paso 1.1: Commit de archivos base
Primero, vamos a guardar los archivos de configuracion creados.

```bash
cd "d:\UNIANDES\SEPTIMO\GESTION DE LA CONFIGURACIÓN DE SOFTWARE\SEMANA 6\AUDITORÍA DE CONFIGURACIÓN\auditoria_configuracion"
git add .
git commit -m "chore: agregar archivos base para auditoria"
git push origin master
```

### Paso 1.2: Verificar repositorio remoto
Asegurate de tener configurado el repositorio remoto en GitHub.

```bash
git remote -v
```

Si no existe, crear repositorio en GitHub y configurar:
```bash
git remote add origin https://github.com/TU_USUARIO/auditoria_configuracion.git
git branch -M main
git push -u origin main
```

## FASE 2: CREAR ISSUES (UNO POR PERSONA)

### Issue 1: Auditor Fisico (Persona 1)
Crear en GitHub con este contenido:

**Titulo:** Auditoria Fisica - Verificacion de Elementos de Configuracion

**Descripcion:**
```
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

## Asignado a
@persona1
```

### Issue 2: Auditor Funcional (Persona 2)
Crear en GitHub con este contenido:

**Titulo:** Auditoria Funcional - Validacion de Requisito RF-001

**Descripcion:**
```
## Objetivo
Validar que el sistema cumple el Requisito Funcional RF-001: Visualizacion de la Aplicacion.

## Requisito a Validar
RF-001: El sistema debe permitir visualizar la interfaz principal de la aplicacion Angular.

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

## Rol
Auditor Funcional

## Asignado a
@persona2
```

### Issue 3: Gestor de Trazabilidad (Persona 3)
Crear en GitHub con este contenido:

**Titulo:** Gestion de Trazabilidad - Configurar Convenciones y Referencias

**Descripcion:**
```
## Objetivo
Establecer y verificar la trazabilidad entre issues, PRs, commits y releases.

## Tareas
- [ ] Verificar que CHECKLIST_AUDITORIA.md define convenciones
- [ ] Revisar plantilla de PR en .github/PULL_REQUEST_TEMPLATE.md
- [ ] Crear tabla de trazabilidad inicial
- [ ] Documentar proceso de referencias cruzadas
- [ ] Validar que todos los commits sigan convencion

## Criterios de Aceptacion
- Convencion de commits documentada y aplicada
- Template de PR configurado
- Referencias cruzadas funcionando (issue -> PR -> commit)
- Documentacion clara del proceso

## Rol
Gestor de Trazabilidad

## Asignado a
@persona3
```

## FASE 3: CREAR BRANCHES POR ISSUE

### Persona 1: Branch para Issue #1
```bash
git checkout main
git pull origin main
git checkout -b audit/auditoria-fisica
```

### Persona 2: Branch para Issue #2
```bash
git checkout main
git pull origin main
git checkout -b audit/auditoria-funcional
```

### Persona 3: Branch para Issue #3
```bash
git checkout main
git pull origin main
git checkout -b audit/gestion-trazabilidad
```

## FASE 4: REALIZAR CAMBIOS Y COMMITS

### Persona 1: Auditoria Fisica (4 commits)
Trabajar en branch `audit/auditoria-fisica`:

**Commit 1:**
```bash
# Editar README.md agregando seccion de estructura
git add README.md
git commit -m "fix: actualizar README con estructura detallada (#1)"
```

**Commit 2:**
```bash
# Verificar o crear scripts adicionales
git add docs/ESTRUCTURA_PROYECTO.md
git commit -m "fix: completar documentacion de estructura del proyecto (#1)"
```

**Commit 3:**
```bash
# Validar .env.example
git add .env.example
git commit -m "fix: verificar variables de entorno en .env.example (#1)"
```

**Commit 4:**
```bash
# Actualizar checklist
git add CHECKLIST_AUDITORIA.md
git commit -m "fix: agregar verificacion de artefactos en checklist (#1)"
```

### Persona 2: Auditoria Funcional (4 commits)
Trabajar en branch `audit/auditoria-funcional`:

**Commit 1:**
```bash
# Ejecutar npm install y documentar
git add docs/REQUISITOS.md
git commit -m "fix: iniciar validacion de requisito RF-001 (#2)"
```

**Commit 2:**
```bash
# Ejecutar npm start y validar
# Crear captura de pantalla en docs/evidencias/
mkdir docs/evidencias
# Guardar screenshot
git add docs/evidencias/
git commit -m "fix: capturar evidencia de aplicacion en ejecucion (#2)"
```

**Commit 3:**
```bash
# Actualizar estado de requisitos
git add docs/REQUISITOS.md
git commit -m "fix: actualizar estado de validacion RF-001 (#2)"
```

**Commit 4:**
```bash
# Documentar resultados
git add docs/REQUISITOS.md
git commit -m "fix: completar documentacion de validacion funcional (#2)"
```

### Persona 3: Gestion Trazabilidad (4 commits)
Trabajar en branch `audit/gestion-trazabilidad`:

**Commit 1:**
```bash
# Revisar y ajustar CHECKLIST_AUDITORIA.md
git add CHECKLIST_AUDITORIA.md
git commit -m "fix: validar convenciones de commits en checklist (#3)"
```

**Commit 2:**
```bash
# Verificar template de PR
git add .github/PULL_REQUEST_TEMPLATE.md
git commit -m "fix: verificar template de pull request (#3)"
```

**Commit 3:**
```bash
# Crear archivo de trazabilidad
# Crear docs/TRAZABILIDAD.md
git add docs/TRAZABILIDAD.md
git commit -m "fix: crear tabla de trazabilidad inicial (#3)"
```

**Commit 4:**
```bash
# Documentar proceso completo
git add docs/TRAZABILIDAD.md
git commit -m "fix: documentar proceso de referencias cruzadas (#3)"
```

## FASE 5: PUSH Y CREAR PULL REQUESTS

### Persona 1:
```bash
git push origin audit/auditoria-fisica
```
Luego crear PR en GitHub con el template, vincular Issue #1.

### Persona 2:
```bash
git push origin audit/auditoria-funcional
```
Luego crear PR en GitHub con el template, vincular Issue #2.

### Persona 3:
```bash
git push origin audit/gestion-trazabilidad
```
Luego crear PR en GitHub con el template, vincular Issue #3.

## FASE 6: REVISION CRUZADA

- Persona 1 revisa PR de Persona 2
- Persona 2 revisa PR de Persona 3
- Persona 3 revisa PR de Persona 1

Cada revisor debe:
1. Leer los cambios
2. Verificar que cumple el checklist
3. Aprobar el PR en GitHub

## FASE 7: MERGE A MAIN

Una vez aprobados todos los PRs:
```bash
# En GitHub: Merge Pull Request
# Opcion: "Squash and merge" o "Merge commit"
```

## FASE 8: CREAR TAG Y RELEASE

```bash
git checkout main
git pull origin main
git tag -a v1.0.0 -m "Release v1.0.0 - Auditoria de Configuracion Completada"
git push origin v1.0.0
```

Luego en GitHub crear Release desde el tag v1.0.0 con release notes.

## FASE 9: GENERAR EVIDENCIAS

Capturas necesarias:
1. Lista de issues creados
2. Commits con referencias
3. PRs con revisiones
4. Release publicado
5. Tabla de trazabilidad
