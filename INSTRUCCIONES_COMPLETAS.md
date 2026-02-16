# INSTRUCCIONES PASO A PASO - AUDITORIA DE CONFIGURACION

## EQUIPO: 3 PERSONAS

- Persona 1: Auditor Fisico
- Persona 2: Auditor Funcional
- Persona 3: Gestor de Trazabilidad

## ESTADO ACTUAL

Ya se ha creado el commit inicial con la estructura base del proyecto.

Commit realizado:
- Hash: 87b6a9f
- Mensaje: "chore: configurar estructura base para auditoria de configuracion"
- Archivos: 12 archivos creados/modificados

---

## PASO 1: CONFIGURAR REPOSITORIO EN GITHUB

### 1.1 Crear repositorio en GitHub
1. Ir a https://github.com
2. Click en "New repository"
3. Nombre: `auditoria-configuracion`
4. Descripcion: "Proyecto de auditoria de configuracion y release controlado"
5. Publico o Privado (segun preferencia)
6. NO inicializar con README (ya existe)
7. Click "Create repository"

### 1.2 Vincular repositorio local con GitHub

```bash
git remote add origin https://github.com/TU_USUARIO/auditoria-configuracion.git
git branch -M main
git push -u origin main
```

EVIDENCIA 1: Capturar pantalla del repositorio en GitHub con el commit inicial.

---

## PASO 2: CREAR ISSUES EN GITHUB

### 2.1 Issue #1 - Auditor Fisico (Persona 1)

Ir al repositorio en GitHub > Issues > New issue

Copiar contenido de: `docs/PLANTILLAS_ISSUES.md` seccion "Issue 1"

Titulo: `Auditoria Fisica - Verificacion de Elementos de Configuracion`

Asignar a: Persona 1

Labels: `auditoria`, `documentacion`, `configuracion`

### 2.2 Issue #2 - Auditor Funcional (Persona 2)

Titulo: `Auditoria Funcional - Validacion de Requisito RF-001`

Asignar a: Persona 2

Labels: `auditoria`, `testing`, `validacion`

### 2.3 Issue #3 - Gestor de Trazabilidad (Persona 3)

Titulo: `Gestion de Trazabilidad - Configurar Convenciones y Referencias`

Asignar a: Persona 3

Labels: `auditoria`, `proceso`, `trazabilidad`

EVIDENCIA 2: Capturar pantalla de los 3 issues creados en GitHub.

ANOTAR LOS NUMEROS: Issue #1 = ___, Issue #2 = ___, Issue #3 = ___

---

## PASO 3: PERSONA 1 - AUDITORIA FISICA

### 3.1 Crear branch

```bash
git checkout main
git pull origin main
git checkout -b audit/auditoria-fisica
```

### 3.2 Commit 1: Actualizar README

Editar `README.md`: Agregar seccion "Elementos de Configuracion Verificados"

```bash
git add README.md
git commit -m "fix: agregar seccion de elementos verificados en README (#1)"
```

### 3.3 Commit 2: Completar documentacion de estructura

Editar `docs/ESTRUCTURA_PROYECTO.md`: Agregar detalles adicionales

```bash
git add docs/ESTRUCTURA_PROYECTO.md
git commit -m "fix: completar documentacion de estructura del proyecto (#1)"
```

### 3.4 Commit 3: Verificar variables de entorno

Editar `.env.example`: Agregar comentarios explicativos

```bash
git add .env.example
git commit -m "fix: agregar comentarios explicativos en .env.example (#1)"
```

### 3.5 Commit 4: Actualizar checklist

Editar `CHECKLIST_AUDITORIA.md`: Marcar items verificados

```bash
git add CHECKLIST_AUDITORIA.md
git commit -m "fix: marcar items verificados en checklist de auditoria (#1)"
```

### 3.6 Push y crear PR

```bash
git push origin audit/auditoria-fisica
```

Ir a GitHub > Pull requests > New pull request

- Base: main
- Compare: audit/auditoria-fisica
- Usar template de PR
- Vincular Issue #1 (escribir "Closes #1" en descripcion)
- Asignar revisor: Persona 3
- Crear PR

EVIDENCIA 3: Capturar pantalla del PR creado.

---

## PASO 4: PERSONA 2 - AUDITORIA FUNCIONAL

### 4.1 Crear branch

```bash
git checkout main
git pull origin main
git checkout -b audit/auditoria-funcional
```

### 4.2 Commit 1: Iniciar validacion

Editar `docs/REQUISITOS.md`: Actualizar estado de RF-001 a "En validacion"

```bash
git add docs/REQUISITOS.md
git commit -m "fix: iniciar validacion de requisito RF-001 (#2)"
```

### 4.3 Commit 2: Capturar evidencia

Ejecutar la aplicacion:

```bash
npm install
npm start
```

Abrir navegador en http://localhost:4200

Tomar screenshot de la aplicacion funcionando

Guardar en `docs/evidencias/app-funcionando.png`

```bash
mkdir docs/evidencias
# Copiar screenshot a docs/evidencias/app-funcionando.png
git add docs/evidencias/
git commit -m "fix: capturar evidencia de aplicacion ejecutandose (#2)"
```

### 4.4 Commit 3: Actualizar estado

Editar `docs/REQUISITOS.md`: Marcar criterios de aceptacion

```bash
git add docs/REQUISITOS.md
git commit -m "fix: actualizar criterios de aceptacion validados (#2)"
```

### 4.5 Commit 4: Completar documentacion

Editar `docs/REQUISITOS.md`: Marcar como "Validado"

```bash
git add docs/REQUISITOS.md
git commit -m "fix: completar validacion funcional de RF-001 (#2)"
```

### 4.6 Push y crear PR

```bash
git push origin audit/auditoria-funcional
```

Crear PR en GitHub:
- Vincular Issue #2
- Asignar revisor: Persona 1

EVIDENCIA 4: Capturar pantalla del PR y del screenshot de la app.

---

## PASO 5: PERSONA 3 - GESTION DE TRAZABILIDAD

### 5.1 Crear branch

```bash
git checkout main
git pull origin main
git checkout -b audit/gestion-trazabilidad
```

### 5.2 Commit 1: Validar convenciones

Editar `CHECKLIST_AUDITORIA.md`: Agregar ejemplos de commits validos

```bash
git add CHECKLIST_AUDITORIA.md
git commit -m "fix: agregar ejemplos de commits en checklist (#3)"
```

### 5.3 Commit 2: Verificar template PR

Editar `.github/PULL_REQUEST_TEMPLATE.md`: Mejorar checklist

```bash
git add .github/PULL_REQUEST_TEMPLATE.md
git commit -m "fix: mejorar checklist en template de PR (#3)"
```

### 5.4 Commit 3: Actualizar tabla trazabilidad

Editar `docs/TRAZABILIDAD.md`: Completar con numeros reales de issues y PRs

```bash
git add docs/TRAZABILIDAD.md
git commit -m "fix: actualizar tabla de trazabilidad con datos reales (#3)"
```

### 5.5 Commit 4: Documentar proceso

Editar `docs/TRAZABILIDAD.md`: Agregar seccion de conclusiones

```bash
git add docs/TRAZABILIDAD.md
git commit -m "fix: documentar proceso completo de trazabilidad (#3)"
```

### 5.6 Push y crear PR

```bash
git push origin audit/gestion-trazabilidad
```

Crear PR en GitHub:
- Vincular Issue #3
- Asignar revisor: Persona 2

EVIDENCIA 5: Capturar pantalla del PR.

---

## PASO 6: REVISION CRUZADA

### 6.1 Persona 3 revisa PR de Persona 1
1. Ir al PR de audit/auditoria-fisica
2. Revisar archivos cambiados
3. Verificar checklist
4. Aprobar PR (boton "Approve")

### 6.2 Persona 1 revisa PR de Persona 2
1. Ir al PR de audit/auditoria-funcional
2. Revisar archivos cambiados
3. Verificar screenshot de evidencia
4. Aprobar PR

### 6.3 Persona 2 revisa PR de Persona 3
1. Ir al PR de audit/gestion-trazabilidad
2. Revisar tabla de trazabilidad
3. Aprobar PR

EVIDENCIA 6: Capturar pantalla de cada PR con la aprobacion.

---

## PASO 7: MERGE A MAIN

Una vez que cada PR tenga al menos 1 aprobacion:

### 7.1 Merge PR #(Persona 1)
1. Ir al PR en GitHub
2. Click "Merge pull request"
3. Confirmar merge
4. Borrar branch si ofrece la opcion

### 7.2 Merge PR #(Persona 2)
Repetir proceso

### 7.3 Merge PR #(Persona 3)
Repetir proceso

EVIDENCIA 7: Capturar pantalla de commits en main con los 3 PRs mergeados.

---

## PASO 8: CREAR TAG Y RELEASE

### 8.1 Actualizar repositorio local

```bash
git checkout main
git pull origin main
```

### 8.2 Crear tag

```bash
git tag -a v1.0.0 -m "Release v1.0.0 - Auditoria de Configuracion Completada"
git push origin v1.0.0
```

### 8.3 Crear Release en GitHub

1. Ir a repositorio > Releases > Create a new release
2. Tag: v1.0.0
3. Title: `Release v1.0.0 - Auditoria de Configuracion Completada`
4. Descripcion (Release Notes):

```markdown
## Release v1.0.0 - Auditoria de Configuracion Completada

Fecha: [FECHA ACTUAL]

### Que cambio
- Auditoria fisica completa de elementos de configuracion
- Validacion funcional del requisito RF-001
- Implementacion de trazabilidad completa
- Documentacion actualizada y completa

### Issues Cerrados
- #1 Auditoria Fisica - Verificacion de Elementos de Configuracion
- #2 Auditoria Funcional - Validacion de Requisito RF-001
- #3 Gestion de Trazabilidad - Configurar Convenciones y Referencias

### Pull Requests Mergeados
- #[X] Auditoria fisica por @persona1
- #[Y] Auditoria funcional por @persona2
- #[Z] Gestion trazabilidad por @persona3

### Como Validar
1. Clonar el repositorio
2. Ejecutar `npm install`
3. Ejecutar `npm start`
4. Verificar aplicacion en http://localhost:4200
5. Revisar documentacion en carpeta docs/

### Archivos de Configuracion Verificados
- README.md
- LICENSE (MIT)
- .env.example
- CHECKLIST_AUDITORIA.md
- docs/ESTRUCTURA_PROYECTO.md
- docs/REQUISITOS.md
- docs/TRAZABILIDAD.md

### Criterios de Entrega Cumplidos
- Todos los elementos de configuracion presentes y versionados
- Requisito RF-001 validado con evidencia
- Trazabilidad completa documentada (issue -> PR -> commit -> release)
- Revision cruzada completada (minimo 1 revisor por PR)
- Release notes completas con referencias

### Metricas
- Total Issues: 3
- Total PRs: 3
- Total Commits: 12 (4 por persona)
- Revisores: 3 (revision cruzada)
```

5. Click "Publish release"

EVIDENCIA 8: Capturar pantalla del release publicado.

---

## PASO 9: VERIFICAR TRAZABILIDAD COMPLETA

### 9.1 Actualizar tabla en docs/TRAZABILIDAD.md

Editar localmente con los datos reales:

```bash
git checkout main
git pull origin main
# Editar docs/TRAZABILIDAD.md con numeros reales
git add docs/TRAZABILIDAD.md
git commit -m "docs: actualizar tabla de trazabilidad final"
git push origin main
```

### 9.2 Verificar referencias cruzadas

En GitHub, verificar que:
- Cada issue muestra los commits que lo referencian
- Cada PR muestra el issue vinculado
- El release muestra issues y PRs

EVIDENCIA 9: Capturar pantalla de un issue mostrando commits vinculados.

---

## PASO 10: GENERAR INFORME PDF

### 10.1 Usar plantilla

Abrir `docs/FORMATO_INFORME.md`

### 10.2 Completar datos

- Nombres de integrantes
- Links reales de repositorio, issues, PRs, releases
- Numeros de commits (hashes)
- Fechas

### 10.3 Insertar capturas

Agregar todas las evidencias capturadas (9 imagenes minimo)

### 10.4 Exportar a PDF

Usar Word, Google Docs o Markdown to PDF

Verificar: 2-4 paginas, tablas visibles, imagenes claras

---

## RESUMEN DE EVIDENCIAS NECESARIAS

1. Repositorio en GitHub con commit inicial
2. 3 issues creados y asignados
3. PR de Persona 1 (auditoria fisica)
4. PR de Persona 2 (auditoria funcional + screenshot app)
5. PR de Persona 3 (gestion trazabilidad)
6. PRs con aprobaciones de revisores
7. Commits en main tras merge
8. Release v1.0.0 publicado
9. Issue mostrando commits vinculados

Total: Minimo 9 capturas de pantalla

---

## COMANDOS RAPIDOS DE REFERENCIA

### Ver log de commits
```bash
git log --oneline --graph
```

### Ver detalles de un commit
```bash
git show HASH_DEL_COMMIT
```

### Ver estado actual
```bash
git status
```

### Ver branches
```bash
git branch -a
```

### Ver tags
```bash
git tag
```

---

## CHECKLIST FINAL

Antes de entregar, verificar:

- [ ] Repositorio en GitHub accesible
- [ ] 3 issues creados y cerrados
- [ ] 3 PRs creados, revisados y mergeados
- [ ] 12 commits totales (4 por persona) con referencias (#issue)
- [ ] Todos los commits siguen convencion: "tipo: descripcion (#issue)"
- [ ] Revision cruzada documentada (approvals en PRs)
- [ ] Tag v1.0.0 creado
- [ ] Release v1.0.0 publicado con release notes
- [ ] Tabla de trazabilidad completa
- [ ] Informe PDF con 2-4 paginas
- [ ] 9+ capturas de pantalla incluidas
- [ ] Links del repo funcionando

---

## ENTREGA FINAL

Subir a la plataforma del curso:

1. Link del repositorio GitHub
2. Link del release v1.0.0
3. Archivo PDF del informe

Fecha limite: [Segun calendario del curso]

---

## SOPORTE

Documentos de referencia en el proyecto:
- GUIA_PASO_A_PASO.md (detallado)
- docs/PLANTILLAS_ISSUES.md (contenido de issues)
- docs/FORMATO_INFORME.md (estructura del PDF)
- CHECKLIST_AUDITORIA.md (controles de calidad)
- docs/TRAZABILIDAD.md (tabla a completar)
