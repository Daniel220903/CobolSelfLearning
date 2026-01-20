## 🔐 Credenciales Vista TN3270

- **Usuario:** `herc01`
- **Contraseña:** `cul8tr`

---

## 📘 Comandos dentro del JCL

- https://platzi.com/cursos/cobol/comandos-del-entorno-mvs-a-detalle/

---

## 📂 Commands / Datasets que deben existir

- `SYS2.PROCLIB(COBOL)` → `PROC_COMPI.txt`
- `HERC01.PLATZI.JCL(JCLCOMPI)` → `COMPI_HOLA.txt`
- `HERC01.PLATZI.JCL(JCLHOEX)` → `JCHOLA.txt`

---

## 🧩 Sintaxis de variables en COBOL

Dentro del **Working-Storage**:

- Prefijo: `WS` (Working Storage)
- Tipos:
  - `V` → Variables
  - `C` → Constantes
  - `S` → Switches

### Formato general

```text
WS(V | C | S)-NOMBRE
```

### Ejemplos

```text
WSC-PRECIO
WSV-EDAD
```

---

## 🔄 Flujo de trabajo completo

### 1️⃣ Código fuente COBOL

- **Dataset:** `HERC01.PLATZI.SRC(HOLA)`
- **Contiene:** Programa COBOL sin compilar

---

### 2️⃣ JCL de compilación

- **Dataset:** `HERC01.PLATZI.JCL(JCLCOMPI)`
- **Función:** Compila el código fuente y genera el ejecutable

---

### 3️⃣ JCL de ejecución

- **Dataset:** `HERC01.PLATZI.JCL(JCLRUN)` (o similar)
- **Función:** Ejecuta el programa ya compilado

---

### 4️⃣ Biblioteca de carga (Load Library)

- **Dataset:** `HERC01.PLATZI.LOAD`
- **Contiene:** Programa compilado (ejecutable)

---

## 📊 Tipos de datos en variables COBOL

### Comparación rápida

| Característica  | PIC 9        | PIC Z              | PIC X                     |
|-----------------|--------------|--------------------|---------------------------|
| Tipo de dato    | Numérico     | Numérico editado   | Alfanumérico              |
| Contenido       | Dígitos 0–9  | Dígitos + espacios | Letras, números, símbolos |
| Uso en cálculos | Sí           | No                 | No                        |
| Suprime ceros   | No           | Sí                 | N/A                       |
| Uso principal   | Cálculos     | Reportes / Display | Texto, nombres, códigos   |

## ENTRAR A SPOOL
=3.8
