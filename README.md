# REPORTE DE LABORATORIO 04
**Curso:** Control de Versiones para Desarrollo Full Stack  
**Docente:** Ing. Luis Flores  

---

### 1. Identificación del Equipo Ágil
* **Grupo de Trabajo N°:** Skibidi-01
* **Integrantes de Ingeniería:**
* **[DESARROLLADOR 1] (Líder):** Ricardo Antonio Álvarez Montenegro | GitHub: @Pepi3660
* **[DESARROLLADOR 2] (Colaborador):** Walter Alexei Amador Jiron | GitHub: @WalterJiron

---

### 2. Hito 1: Implementación de Seguridad Perimetral (.gitignore)
1. **Estructura del archivo `.gitignore` consolidada:**
```text
# Secretos locales de ApexPay
.env
.env.local
# Temporales de compilacion y dependencias generadas por el script
node_modules/
dist/
*.log
```

2. **Prueba de Inmunidad de Credenciales:**
```text
git status 
En la rama main
Tu rama y 'origin/main' han divergido,
y tienen 1 y 10 commits diferentes cada una respectivamente.
  (use "git pull" if you want to integrate the remote branch with yours)

nada para hacer commit, el árbol de trabajo está limpio
```

---

### 3. Hito 2: Resolución de la Colisión de Interfaces (Merge Conflict)
1. **Discrepancia Técnica Inicial:**  
_Respuesta:_ El push del Desarrollador 2 fue rechazado porque ambos trabajaron sobre la misma sección del archivo. Git inyectó los siguientes marcadores bloqueando la integración automática en el archivo original:
```markdown
<<<<<<< HEAD
Tema del proyecto: Claro
=======
Tema del proyecto: Oscuro
>>>>>>> cf40291... feat: configurar tema oscuro
```

2. **Resultado Consolidado de Consenso:**  
```markdown
Tema del proyecto: Configuración híbrida (Soporte dinámico para Claro y Oscuro)
```

---

### 4. Hito 3: Mitigación de Exposición de Infraestructura (git revert)
1. **Histórico del Historial Clínico de Producción (Git Log):**  
```text
git log --oneline
8ce60fc (HEAD -> main) Revert "feat: modulo de pruebas de red expuestas"
7640dab feat: modulo de pruebas de red expuestas
8bc5a1d pa que revises :u
9f45c02 resuelto :u
48b8265 Merge branch 'main' of https://github.com
dd58eb5 feat: configurar tema claro
cf40291 feat: configurar tema oscuro
d9a9073 chore: inicializador codigo base de ApexPay y configurar gitignore
2b3d0a7 Initial commit
```

2. **Análisis de Resiliencia Organizacional:**  
_Respuesta:_  
>[!note]
>`git reset --hard` es considerado de alto peligro en ramas centrales compartidas porque **reescribe el historial público**, eliminando commits existentes y obligando a usar `git push --force`, lo que desincroniza a todos los colaboradores que ya tenían esos commits en sus repositorios locales, rompe pipelines de CI/CD, corrompe Pull Requests activos y compromete la trazabilidad del proyecto. En cambio, `git revert` crea un **nuevo commit que invierte los cambios** sin tocar el historial previo, permitiendo un `push` normal, manteniendo a todo el equipo sincronizado y dejando un registro auditable de qué se deshizo, cuándo y por qué, lo que lo convierte en la práctica segura y recomendada para entornos corporativos.

---

### 5. Hito 4: Enlaces de Gobernanza y Solicitudes de Integración
* **Pull Request de Menú (`feat/menu-principal`):** `https://github.com/Pepi3660/apexpay-dashboard/pull/2`
* **Pull Request de Footer (`feat/footer`):** `https://github.com/Pepi3660/apexpay-dashboard/pull/1`
