# Comandos para Generar Evidencias

Este documento contiene todos los comandos necesarios para generar las evidencias del proyecto para la entrega.

## 1. Historial de Commits

### Ver historial completo en formato de grafo
```bash
git log --oneline --graph --all
```

### Ver historial con detalles de cada commit
```bash
git log --graph --all --format=format:'%h - %an, %ar : %s' --abbrev-commit
```

### Ver estadísticas de commits por autor
```bash
git shortlog -sn --all
```

### Ver historial de un archivo específico
```bash
git log --follow -- RUTA_ARCHIVO
```

## 2. Información de Branches

### Listar todos los branches locales y remotos
```bash
git branch -a
```

### Ver último commit de cada branch
```bash
git branch -av
```

### Ver branches mergeados a main
```bash
git branch --merged main
```

### Ver grafo de branches
```bash
git log --graph --oneline --all --decorate
```

## 3. Información de Tags

### Listar todos los tags
```bash
git tag -l
```

### Ver información detallada del tag v1.0.0
```bash
git show v1.0.0
```

### Ver commits desde el último tag
```bash
git log v1.0.0..HEAD --oneline
```

## 4. Información de Merges

### Ver todos los merge commits
```bash
git log --merges --oneline
```

### Ver detalles de un merge específico
```bash
git show HASH_MERGE
```

### Ver branches que fueron mergeados
```bash
git log --merges --pretty=format:"%h %s"
```

## 5. Diferencias y Cambios

### Ver cambios en un commit específico
```bash
git show HASH_COMMIT
```

### Ver archivos modificados en un commit
```bash
git show --stat HASH_COMMIT
```

### Ver diferencias entre branches
```bash
git diff main..audit/auditoria-fisica
```

### Ver archivos cambiados entre commits
```bash
git diff --name-only COMMIT1 COMMIT2
```

## 6. Información de Issues y PRs (GitHub CLI)

### Listar issues
```bash
gh issue list --state all
```

### Ver detalles de un issue
```bash
gh issue view NUMERO_ISSUE
```

### Listar Pull Requests
```bash
gh pr list --state all
```

### Ver detalles de un PR
```bash
gh pr view NUMERO_PR
```

### Ver estado de PRs mergeados
```bash
gh pr list --state merged
```

## 7. Estadísticas del Proyecto

### Contar commits por tipo
```bash
git log --oneline | grep "^[a-f0-9]* fix:" | wc -l
```

### Ver contribuciones por persona (simuladas)
```bash
git log --format='%an' | sort | uniq -c
```

### Archivos más modificados
```bash
git log --pretty=format: --name-only | sort | uniq -c | sort -rg | head -10
```

### Tamaño del repositorio
```bash
git count-objects -vH
```

## 8. Evidencias para Capturas de Pantalla

### 1. Grafo de red visual (ejecutar y capturar)
```bash
git log --graph --oneline --all --decorate --color
```

### 2. Lista de commits con referencias a issues
```bash
git log --oneline --grep="#"
```

### 3. Información de los 3 merges principales
```bash
git log --merges --oneline -3
```

### 4. Estado actual del repositorio
```bash
git status
git branch -a
git tag -l
```

### 5. Commits agrupados por issue
```bash
# Issue #1
git log --oneline --grep="#1"

# Issue #2
git log --oneline --grep="#2"

# Issue #3
git log --oneline --grep="#3"
```

## 9. Verificación de Trazabilidad

### Ver commits de un branch específico
```bash
git log main..audit/auditoria-fisica --oneline
git log main..audit/auditoria-funcional --oneline
git log main..audit/gestion-trazabilidad --oneline
```

### Ver qué PRs cerraron cada issue (GitHub CLI)
```bash
gh issue view 1 --json closedAt,closingPullRequests -q '.closingPullRequests[].title'
gh issue view 2 --json closedAt,closingPullRequests -q '.closingPullRequests[].title'
gh issue view 3 --json closedAt,closingPullRequests -q '.closingPullRequests[].title'
```

### Ver información del release
```bash
gh release view v1.0.0
```

## 10. Exportar Evidencias a Archivos

### Exportar log completo a archivo de texto
```bash
git log --graph --all --format=format:'%h - %an, %ar : %s' > historial_completo.txt
```

### Exportar lista de commits a CSV
```bash
git log --pretty=format:'"%h","%an","%ad","%s"' --date=short > commits.csv
```

### Exportar estadísticas a archivo
```bash
git log --shortstat --pretty=format:'%h,%an,%ad,%s' --date=short > estadisticas.csv
```

### Exportar información de branches
```bash
git branch -av > branches.txt
```

## 11. Comandos Usados Durante el Desarrollo

### Creación de branches
```bash
git checkout -b audit/auditoria-fisica
git checkout -b audit/auditoria-funcional
git checkout -b audit/gestion-trazabilidad
```

### Commits con referencia a issues
```bash
git commit -m "fix: mensaje descriptivo (#1)"
git commit -m "fix: mensaje descriptivo (#2)"
git commit -m "fix: mensaje descriptivo (#3)"
```

### Merge de branches
```bash
# Los merges se hicieron via Pull Requests en GitHub
gh pr merge 4 --merge
gh pr merge 5 --merge
gh pr merge 6 --merge
```

### Creación de tag
```bash
git tag -a v1.0.0 -m "Release version 1.0.0 - Auditoria de Configuracion Completa"
git push origin v1.0.0
```

### Publicación de branches
```bash
git push origin audit/auditoria-fisica
git push origin audit/auditoria-funcional
git push origin audit/gestion-trazabilidad
```

## 12. Verificación Final

### Checklist de verificación (ejecutar todos)
```bash
# ✅ 12 commits tipo fix
git log --oneline --grep="fix:" --all | wc -l

# ✅ 3 issues cerrados
gh issue list --state closed

# ✅ 3 PRs mergeados
gh pr list --state merged

# ✅ 3 branches de audit
git branch --list "audit/*"

# ✅ Tag v1.0.0 creado
git tag -l "v1.0.0"

# ✅ 3 merge commits
git log --merges --oneline | head -3

# ✅ Repositorio sincronizado
git status
```

## URLs de Referencia

- **Repositorio**: https://github.com/Santy01/auditoria_configuracion
- **Issues**: https://github.com/Santy01/auditoria_configuracion/issues
- **Pull Requests**: https://github.com/Santy01/auditoria_configuracion/pulls
- **Network Graph**: https://github.com/Santy01/auditoria_configuracion/network
- **Releases**: https://github.com/Santy01/auditoria_configuracion/releases

---

**Nota**: Ejecutar estos comandos desde la raíz del repositorio local.
**Generado**: Para auditoria de configuración - Versión 1.0.0
