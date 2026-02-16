# Tabla de Trazabilidad

## Objetivo
Este documento mantiene la trazabilidad completa entre issues, pull requests, commits y releases del proyecto.

## Formato de Trazabilidad

| Issue | Titulo | PR | Commits | Release | Evidencia |
|-------|--------|----|---------|---------| ----------|
| - | - | - | - | - | - |

## Trazabilidad Issue -> PR -> Commit -> Release

### Issue #1: Auditoria Fisica
| Issue | Titulo | PR | Commits | Release | Evidencia |
|-------|--------|----|---------|---------| ----------|
| #1 | Auditoria Fisica - Verificacion de Elementos de Configuracion | PR #(pendiente) | 797286e, bbf931e, 9389f36, 038edee | v1.0.0 | Branch + Checklist PR |

**Branch:** audit/auditoria-fisica

**Commits realizados:**
- `797286e` - fix: agregar seccion de elementos verificados en README (#1)
- `bbf931e` - fix: completar documentacion de estructura del proyecto (#1)
- `9389f36` - fix: agregar comentarios explicativos en .env.example (#1)
- `038edee` - fix: marcar items verificados en checklist de auditoria (#1)

### Issue #2: Auditoria Funcional
| Issue | Titulo | PR | Commits | Release | Evidencia |
|-------|--------|----|---------|---------| ----------|
| #2 | Auditoria Funcional - Validacion de Requisito RF-001 | PR #(pendiente) | 055e890, 70cb69d, 90f55a3, 8acfd08 | v1.0.0 | Branch + Screenshot |

**Branch:** audit/auditoria-funcional

**Commits realizados:**
- `055e890` - fix: iniciar validacion de requisito RF-001 (#2)
- `70cb69d` - fix: capturar evidencia de aplicacion ejecutandose (#2)
- `90f55a3` - fix: actualizar criterios de aceptacion validados (#2)
- `8acfd08` - fix: completar validacion funcional de RF-001 (#2)

### Issue #3: Gestion de Trazabilidad
| Issue | Titulo | PR | Commits | Release | Evidencia |
|-------|--------|----|---------|---------| ----------|
| #3 | Gestion de Trazabilidad - Configurar Convenciones y Referencias | PR #(pendiente) | 5ec853b, 3558ee8, (pendiente), (pendiente) | v1.0.0 | Branch + Tabla |

**Branch:** audit/gestion-trazabilidad

**Commits realizados:**
- `5ec853b` - fix: agregar ejemplos de commits en checklist (#3)
- `3558ee8` - fix: mejorar checklist en template de PR (#3)
- (En progreso) - fix: actualizar tabla de trazabilidad con datos reales (#3)
- (Pendiente) - fix: documentar proceso completo de trazabilidad (#3)

## Resumen de Metricas

- Total de Issues: 3
- Total de PRs: 3 (esperados)
- Total de Commits: 12 (4 por persona)
- Releases: 1 (v1.0.0)

## Proceso de Referencias Cruzadas Documentado

### Como funciona la trazabilidad:

1. **Issue -> Branch**
   - Se crea un issue en GitHub con descripcion clara
   - Se asigna a un responsable
   - Se crea un branch con convencion: tipo/descripcion
   - Ejemplo: Issue #1 -> Branch audit/auditoria-fisica

2. **Branch -> Commits**
   - Cada commit en el branch referencia el issue
   - Formato: tipo: descripcion (#numero_issue)
   - Ejemplo: fix: agregar seccion verificada (#1)
   - Esto crea un link automatico entre commit e issue

3. **Commits -> Pull Request**
   - Se crea PR desde el branch hacia main
   - En la descripcion del PR se vincula el issue: Closes #numero
   - El PR muestra todos los commits del branch
   - GitHub vincula automaticamente PR con issue

4. **Pull Request -> Merge**
   - El PR es revisado por al menos 1 compañero
   - Se aprueba el PR
   - Se hace merge a main
   - El issue se cierra automaticamente al hacer merge

5. **Main -> Release**
   - Se crea tag desde main: git tag -a v1.0.0
   - Se crea release en GitHub desde el tag
   - En release notes se referencian issues y PRs
   - Release contiene todos los cambios mergeados

### Beneficios de la Trazabilidad:

- Se puede rastrear cada cambio desde el requisito inicial
- Se tiene historial completo de decisiones
- Se facilita la auditoria y revision
- Se mejora la comunicacion del equipo
- Se documenta el proceso automaticamente

### Herramientas de GitHub que ayudan:

- Referencias automaticas con #numero
- Closes/Fixes para cerrar issues
- Timeline de issues muestra commits y PRs
- Grafo de branches visualiza flujo
- Release notes pueden auto-generarse

## Actualizacion

**Ultima actualizacion:** 16 de febrero de 2026
**Actualizado por:** Gestor de Trazabilidad
**Estado:** Proceso documentado y tabla actualizada con datos reales
