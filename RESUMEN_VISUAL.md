# Resumen Visual del Proceso

## FLUJO COMPLETO

```
INICIO
  |
  v
[1] Configurar Repo en GitHub
  |
  v
[2] Crear 3 Issues (uno por persona)
  |
  +------------------+------------------+
  |                  |                  |
  v                  v                  v
Persona 1          Persona 2          Persona 3
Issue #1           Issue #2           Issue #3
  |                  |                  |
  v                  v                  v
[3] Crear Branch
audit/fisica     audit/funcional   audit/trazabilidad
  |                  |                  |
  v                  v                  v
[4] Hacer 4 Commits con referencia (#1, #2, #3)
  |                  |                  |
  v                  v                  v
[5] Push y Crear PR
  |                  |                  |
  +------------------+------------------+
                     |
                     v
           [6] Revision Cruzada
           - P3 revisa P1
           - P1 revisa P2
           - P2 revisa P3
                     |
                     v
             [7] Merge a Main
              (3 PRs mergeados)
                     |
                     v
          [8] Crear Tag v1.0.0
                     |
                     v
        [9] Crear Release en GitHub
                     |
                     v
       [10] Generar Informe PDF
                     |
                     v
                  ENTREGA
```

## DISTRIBUCION DE TRABAJO

### PERSONA 1: AUDITOR FISICO
- Rol: Verificar elementos de configuracion
- Issue: #1
- Branch: audit/auditoria-fisica
- Commits: 4
- Revisa: PR de Persona 2

Commits:
1. fix: agregar seccion de elementos verificados en README (#1)
2. fix: completar documentacion de estructura del proyecto (#1)
3. fix: agregar comentarios explicativos en .env.example (#1)
4. fix: marcar items verificados en checklist de auditoria (#1)

### PERSONA 2: AUDITOR FUNCIONAL
- Rol: Validar requisitos
- Issue: #2
- Branch: audit/auditoria-funcional
- Commits: 4
- Revisa: PR de Persona 3

Commits:
1. fix: iniciar validacion de requisito RF-001 (#2)
2. fix: capturar evidencia de aplicacion ejecutandose (#2)
3. fix: actualizar criterios de aceptacion validados (#2)
4. fix: completar validacion funcional de RF-001 (#2)

### PERSONA 3: GESTOR DE TRAZABILIDAD
- Rol: Controlar referencias y convenciones
- Issue: #3
- Branch: audit/gestion-trazabilidad
- Commits: 4
- Revisa: PR de Persona 1

Commits:
1. fix: agregar ejemplos de commits en checklist (#3)
2. fix: mejorar checklist en template de PR (#3)
3. fix: actualizar tabla de trazabilidad con datos reales (#3)
4. fix: documentar proceso completo de trazabilidad (#3)

## TOTAL DE COMMITS

```
Commit inicial (chore): 1 commit
Persona 1 (fix): 4 commits
Persona 2 (fix): 4 commits
Persona 3 (fix): 4 commits
-----------------------------
TOTAL: 13 commits
(12 commits tipo "fix" + 1 commit inicial)
```

## TRAZABILIDAD

```
Issue #1 ──┬──> Branch: audit/auditoria-fisica
           ├──> 4 Commits con (#1)
           ├──> PR #X
           ├──> Aprobado por Persona 3
           ├──> Mergeado a main
           └──> Incluido en Release v1.0.0

Issue #2 ──┬──> Branch: audit/auditoria-funcional
           ├──> 4 Commits con (#2)
           ├──> PR #Y
           ├──> Aprobado por Persona 1
           ├──> Mergeado a main
           └──> Incluido en Release v1.0.0

Issue #3 ──┬──> Branch: audit/gestion-trazabilidad
           ├──> 4 Commits con (#3)
           ├──> PR #Z
           ├──> Aprobado por Persona 2
           ├──> Mergeado a main
           └──> Incluido en Release v1.0.0
```

## TIMELINE SUGERIDO

```
DIA 1:
- Configurar repositorio en GitHub
- Crear 3 issues
- Cada persona crea su branch

DIA 2:
- Cada persona hace sus 4 commits
- Push de branches
- Crear PRs

DIA 3:
- Revision cruzada
- Aprobar PRs
- Merge a main

DIA 4:
- Crear tag v1.0.0
- Crear release
- Generar informe PDF
```

## ARCHIVOS CLAVES DEL PROYECTO

```
auditoria_configuracion/
│
├── INSTRUCCIONES_COMPLETAS.md    ← GUIA PRINCIPAL (LEER PRIMERO)
├── RESUMEN_VISUAL.md              ← Este archivo
├── CHECKLIST_AUDITORIA.md         ← Controles de calidad
├── GUIA_PASO_A_PASO.md            ← Detalles del proceso
│
├── docs/
│   ├── PLANTILLAS_ISSUES.md      ← Copiar/pegar para crear issues
│   ├── FORMATO_INFORME.md        ← Estructura del PDF
│   ├── TRAZABILIDAD.md            ← Tabla a completar
│   ├── REQUISITOS.md              ← Requisitos a validar
│   └── ESTRUCTURA_PROYECTO.md    ← Documentacion tecnica
│
└── .github/
    └── PULL_REQUEST_TEMPLATE.md  ← Template automatico de PR
```

## CONVENCIONES IMPORTANTES

### Formato de Commits
```
tipo: descripcion breve (#numero_issue)
```

Ejemplos validos:
- `fix: actualizar README con estructura detallada (#1)`
- `fix: capturar evidencia de aplicacion (#2)`
- `fix: agregar ejemplos en checklist (#3)`

### Formato de Branches
```
tipo/descripcion-breve
```

Ejemplos:
- `audit/auditoria-fisica`
- `audit/auditoria-funcional`
- `audit/gestion-trazabilidad`

### Formato de Tags
```
vMAJOR.MINOR.PATCH
```

Para este proyecto:
- `v1.0.0`

## CHECKLIST RAPIDO

Antes de comenzar:
- [ ] Leer INSTRUCCIONES_COMPLETAS.md
- [ ] Tener cuenta de GitHub
- [ ] Tener Git instalado
- [ ] Asignar roles a cada persona

Durante el proceso:
- [ ] Crear repositorio en GitHub
- [ ] Crear 3 issues
- [ ] Cada persona crear branch
- [ ] Hacer 4 commits por persona (12 total)
- [ ] Crear 3 PRs
- [ ] Revision cruzada
- [ ] Merge a main
- [ ] Tag v1.0.0
- [ ] Release con notas

Para la entrega:
- [ ] Capturar 9+ evidencias
- [ ] Completar tabla de trazabilidad
- [ ] Generar PDF del informe
- [ ] Subir a plataforma del curso

## LINKS IMPORTANTES

Una vez creado el repositorio, actualizar:
- Repositorio: https://github.com/USUARIO/auditoria-configuracion
- Issues: https://github.com/USUARIO/auditoria-configuracion/issues
- PRs: https://github.com/USUARIO/auditoria-configuracion/pulls
- Releases: https://github.com/USUARIO/auditoria-configuracion/releases

## CONSEJOS

1. Comunicarse constantemente entre el equipo
2. Seguir las convenciones al pie de la letra
3. Revisar bien antes de aprobar PRs
4. Tomar capturas de cada paso importante
5. Completar la tabla de trazabilidad en tiempo real
6. Revisar checklist antes de cada merge
7. Redactar release notes con cuidado

## ERRORES COMUNES A EVITAR

- NO hacer commits sin referencia al issue
- NO aprobar tu propio PR
- NO saltarse la revision
- NO hacer commits directos a main
- NO olvidar capturar evidencias
- NO usar formato incorrecto en commits
- NO crear release sin tag
- NO olvidar vincular issues en PRs

## SOPORTE TECNICO

Si surge algun problema:
1. Revisar la documentacion en docs/
2. Verificar que los comandos se ejecutaron correctamente
3. Revisar el log de git: `git log --oneline`
4. Verificar branches: `git branch -a`
5. Verificar remotes: `git remote -v`
