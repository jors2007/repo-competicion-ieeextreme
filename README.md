# 🚀 IEEEXtreme - Manual de Supervivencia del Equipo

Este repositorio contiene las soluciones, plantillas y herramientas del equipo para la competencia **IEEEXtreme**. Al estar compitiendo en **remoto**, la coordinación y el orden son vitales para maximizar nuestros puntos.

---

## ⏱️ 60 Minutos Antes: El Checklist de Preparación

Cada integrante debe asegurar este entorno en su casa antes del pitazo inicial:

- [ ] **Conectividad:** Reinicia el router de internet y prioriza conexión por cable (Ethernet) si es posible.
- [ ] **Entorno de Voz:** Conéctate al canal de Discord. Configura el micrófono en *Push-to-Talk* o supresión de ruido (Krisp) para evitar ruidos molestos de fondo.
- [ ] **Espacio de Trabajo:** Ten a mano agua, café/energizantes, snacks ligeros (frutos secos, frutas) y comida lista para calentar. ¡No pierdas tiempo cocinando durante el torneo!
- [ ] **Sincronización de Git:** Ejecuta un `git checkout main` seguido de un `git pull origin main` para asegurarte de tener la última versión de las plantillas.
- [ ] **Logueo en la plataforma:** Inicia sesión en el portal oficial de IEEEXtreme y verifica que tu usuario y equipo aparezcan correctamente.

---

## ⚔️ Estrategia Durante las 24 Horas

### 1. El Flujo de Trabajo en Git (Sin Tallarines)
Para evitar conflictos de código (*Merge Conflicts*), **nunca trabajes sobre la rama `main`** y **maneja un archivo por problema** (Ej: `ProblemaA.java`).

Cuando vayas a resolver un problema:
1. Crea tu rama desde la terminal: `git checkout -b problema-A`
2. Programa tu solución en su propio archivo (`ProblemaA.java`).
3. Sube tus avances si necesitas ayuda: `git push origin problema-A`
4. **Una vez que la plataforma te dé "ACCEPTED" (100 puntos):**
   ```bash
   git checkout main
   git pull origin main
   git merge problema-A
   git push origin main
   ```
5. Avisa al equipo por Discord: *"¡Problema A subido a main!"*. Los demás harán un `git fetch` para estar al día.

### 2. Uso de IA Generativa (Regla Oficial)
Está permitido usar IA para generar código o destrabar lógica, pero **es obligatorio declarar su uso**. Si usas código generado por IA, añade este comentario al inicio de tu archivo antes de subirlo a la plataforma:
```java
// Este código utiliza asistencia de IA para [explicar brevemente: optimizar lectura / estructura de grafos]
```

### 3. Logística y Relevos de Sueño
- **Lectura en Radar:** Cuando se liberen nuevos problemas, dividámonos la lectura (ej. Uno lee el 1 y 2, otro el 3 y 4). Resuman el problema en voz alta por Discord para clasificar si es Fácil, Medio o Difícil.
- **Bloqueos de 30 min:** Si pasas más de 30 minutos estancado en un problema sin avanzar, **pide ayuda por Discord o rota de problema**. No gastes energía de forma ineficiente.
- **Turnos de Descanso:** Respetemos los turnos de sueño acordados. Quien esté libre *debe* ir a descansar. Si alguien no aparece a su turno, su pareja de relevo lo llamará al celular.

---

## 🛠️ Comandos Rápidos de Consola (Java)

Para compilar y ejecutar tus archivos sueltos desde la terminal de tu editor sin usar proyectos pesados:

### Compilar el archivo:
```bash
javac ProblemaA.java
```

### Ejecutar pasándole datos por consola a mano:
```bash
java ProblemaA
```

### 💡 Truco de Productividad: Probar con un archivo de texto
Crea un archivo llamado `input.txt` con el ejemplo del enunciado y ejecútalo así para no tener que escribir los datos cada vez que pruebes:
```bash
java ProblemaA < input.txt
```

---

## 📝 Plantilla Base (Lectura Rápida)

Usa siempre esta estructura para tus códigos de Java. Evita usar `Scanner` ya que puede provocar errores de **Time Limit Exceeded (TLE)** debido a su lentitud con grandes volúmenes de datos.

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = null;

        String linea = br.readLine();
        if (linea == null) return;
        
        st = new StringTokenizer(linea);
        // Ejemplo de lectura de enteros:
        // int n = Integer.parseInt(st.nextToken());
        
        // --- TU LÓGICA AQUÍ ---
        
    }
}
```

¡Mucho éxito equipo! Mantengamos la calma, la comunicación abierta y a sumar puntos. 🎯
