# Proyecto-Concurso-de-peso-de-pescados
# 🎣 Sistema de Registro de Pesos para Concurso de Pesca  
**Proyecto NEXO – ITIID – Cuatrimestre 3**

Sistema no-code basado en Google Forms + Google Sheets, diseñado para registrar participantes de un concurso de pesca y determinar automáticamente el TOP 3 de peces más pesados.  
Incluye representación visual del podio en un cuarto de cuarzo dentro de Minecraft.

---

## 📌 Descripción del Proyecto  

Este proyecto implementa una solución sencilla pero funcional para gestionar un concurso de pesca en el que cada participante registra:

- Su **ID**
- Su **nombre**
- El **peso del pez más grande que logró atrapar**

La información se captura mediante **Google Forms**, se almacena y procesa en **Google Sheets**, y el **Top 3** de pescadores se representa visualmente en un **mundo virtual de Minecraft** mediante un podio de tres bloques:

- 🥇 Diamante → 1er lugar  
- 🥈 Esmeralda → 2do lugar  
- 🥉 Oro → 3er lugar  

La meta del proyecto es demostrar una solución realista, rápida de implementar y totalmente documentada, incluso con recursos limitados o sin conocimientos avanzados de programación.

---

## 🛠 Tecnologías Utilizadas

- **Google Forms** – Captura de datos de participantes  
- **Google Sheets** – Procesamiento, ordenamiento y ranking  
- **Minecraft Java Edition** – Visualización del podio  
- **No-Code Workflow** – Enfoque sin programación tradicional  
- **Google Drive** – Manejo de recursos y evidencias  

---

## 🧰 Instalación / Setup (Paso a Paso)

### 🔹 1. Crear el Google Form  
Campos requeridos:

1. **ID del participante**  
2. **Nombre completo**  
3. **Peso del pez más pesado (kg)**  

Esto permitirá estructurar la base de datos correctamente.

---

### 🔹 2. Conectar Forms → Sheets  
En Google Forms:  
> Respuestas → Crear hoja de cálculo

Esto generará automáticamente una hoja llamada **Respuestas**.

---

### 🔹 3. Crear la hoja “Top3”  
En Google Sheets:  
> Crear nueva hoja → renombrar a **Top3**

Insertar la fórmula:

**Ordenamiento completo:**
=SORT(A2:C, C2:C, FALSE)

**Top 3:**
=ARRAY_CONSTRAIN(SORT(A2:C, C2:C, FALSE), 3, 3)

Esto devuelve automáticamente los 3 mejores pescadores basándose en el peso registrado.

4. Preparar el Mundo Virtual en Minecraft

Construir un cuarto de presentación con:

Paredes de bloque de cuarzo

Iluminación con antorchas

Podio central con:

Diamante (1er lugar)

Esmeralda (2do lugar)

Oro (3er lugar)

Letreros sobre cada bloque indicando:

Lugar

Nombre del participante

Peso registrado

El presentador del concurso solo debe actualizar manualmente los nombres y pesos del Top 3 sacados de Sheets.

🚀 Uso / Ejemplos
✔ Ejemplo de Registro (Google Form)
ID	Nombre	Peso (kg)
103	Ana Rivera	5.1
142	Carlos Martínez	4.6
219	Luis Jiménez	4.2
✔ Resultado Automático en Google Sheets

En la hoja Top3 aparecerá:

1. Ana Rivera — 5.1 kg  
2. Carlos Martínez — 4.6 kg  
3. Luis Jiménez — 4.2 kg

Actualiza manualmente estos datos en los letreros del podio de Minecraft.

🖼 Capturas de Pantalla



🧾 Créditos / Referencias

Google Forms Official Documentation

Google Sheets Function Reference

Minecraft Wiki – Blocks & Building

Proyecto NEXO – UPSRJ Guía Oficial de Documentación

Metodología No-Code Workflow

📬 Contacto

Autor/es: Ricardo García Alvarez , Jesus Villeda Ramirez 
UPSRJ
Año: 2025
