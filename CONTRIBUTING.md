# Guía de Contribución

¡Bienvenido al proyecto Sistema de Gestión de Biblioteca! Esta guía te ayudará a hacer tu primera contribución.

## Antes de empezar

1. Asegúrate de tener instalado:
   - Java JDK 11 o superior
   - Git
   - Un IDE (IntelliJ IDEA, Eclipse, VS Code, etc.)

2. Haz un fork del repositorio haciendo clic en el botón "Fork" en la esquina superior derecha

3. Clona tu fork a tu máquina local:
```bash
git clone https://github.com/TU-USUARIO/biblioteca-java.git
cd biblioteca-java
```

## Configuración del proyecto

1. Abre el proyecto en tu IDE favorito

2. La estructura del proyecto es:
```
src/
├── com/biblioteca/
    ├── BibliotecaApp.java (clase principal)
    ├── modelo/
    │   ├── Libro.java
    │   └── Prestamo.java
    └── servicio/
        └── BibliotecaServicio.java
```

3. Compila y ejecuta el proyecto para asegurarte de que funciona:
```bash
javac -d bin src/com/biblioteca/**/*.java src/com/biblioteca/*.
java -cp bin com.biblioteca.BibliotecaApp
```

## Proceso de contribución

### Paso 1: Elige una issue

1. Ve a la pestaña "Issues" del repositorio
2. Busca una issue que te interese (recomendamos empezar con las etiquetadas como `good first issue`)
3. Comenta en la issue diciendo que la vas a trabajar
4. Espera a que el mantenedor te la asigne

### Paso 2: Crea una rama

```bash
# Actualiza tu rama main
git checkout main
git pull origin main

# Crea una nueva rama para tu contribución
git checkout -b issue-NUMERO-descripcion-corta
# Ejemplo: git checkout -b issue-5-validar-isbn
```

### Paso 3: Haz tus cambios

1. Lee cuidadosamente la descripción de la issue
2. Implementa los cambios necesarios
3. Prueba tu código para asegurarte de que funciona
4. Asegúrate de seguir el estilo de código existente

**Consejos:**
- Haz commits pequeños y frecuentes
- Escribe mensajes de commit descriptivos
- Comenta tu código cuando sea necesario

### Paso 4: Commit y push

```bash
# Agrega los archivos modificados
git add .

# Haz commit con un mensaje descriptivo
git commit -m "Fixes #NUMERO: Descripción breve de los cambios"
# Ejemplo: git commit -m "Fixes #5: Agrega validación de formato ISBN"

# Sube tus cambios a tu fork
git push origin issue-NUMERO-descripcion-corta
```

### Paso 5: Crea un Pull Request

1. Ve a tu fork en GitHub
2. Verás un botón "Compare & pull request" - haz clic en él
3. Asegúrate de que la base sea `main` del repositorio original
4. Escribe un título descriptivo: `Fixes #NUMERO: Descripción`
5. En la descripción, explica:
   - Qué cambios hiciste
   - Cómo probaste tus cambios
   - Si hay algo que el revisor deba saber

6. Haz clic en "Create pull request"

## Checklist antes de crear el PR

- [ ] El código compila sin errores
- [ ] Has probado tu implementación
- [ ] El código sigue el estilo del proyecto
- [ ] Has actualizado la documentación si es necesario
- [ ] Tu commit referencia el número de issue (Fixes #XX)

## 📝 Estilo de código

- Usa nombres descriptivos para variables y métodos
- Sigue la convención camelCase para nombres de variables y métodos
- Usa PascalCase para nombres de clases
- Indenta con 4 espacios
- Incluye comentarios para lógica compleja
- Mantén los métodos cortos y con una sola responsabilidad

## ¿Encontraste un bug?

Si encuentras un bug que no tiene issue:

1. Busca primero en las issues existentes por si ya está reportado
2. Si no existe, crea una nueva issue con:
   - Título descriptivo
   - Pasos para reproducir el bug
   - Comportamiento esperado vs. comportamiento actual
   - Capturas de pantalla si aplica

## ¿Necesitas ayuda?

- Revisa las issues existentes
- Pregunta en los comentarios de la issue
- Sé específico sobre tu problema

## Después del PR

- Responde a los comentarios del revisor
- Haz los cambios solicitados si los hay
- Una vez aprobado, tu PR será fusionado
- ¡Felicidades por tu contribución!

## Código de Conducta

- Sé respetuoso con todos los colaboradores
- Acepta críticas constructivas
- Enfócate en lo mejor para el proyecto
- Muestra empatía hacia otros miembros