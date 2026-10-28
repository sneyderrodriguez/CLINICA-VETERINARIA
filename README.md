# 🐾 Clínica Veterinaria — Java POO

> Proyecto académico en **Java** para representar diferentes mascotas de una clínica veterinaria y calcular el costo de sus consultas mediante **herencia, clases abstractas, sobrescritura de métodos y polimorfismo**.

[![Java](https://img.shields.io/badge/Java-POO-orange)](https://www.java.com/)
[![GitHub](https://img.shields.io/badge/GitHub-Repositorio-black?logo=github)](https://github.com/sneyderrodriguez/CLINICA-VETERINARIA)

---

## 📌 Sobre el proyecto

Esta aplicación modela tres tipos de animales: **perros, gatos y aves**. Cada mascota comparte información básica, pero tiene datos particulares y una regla diferente para calcular el valor de su consulta.

El proyecto permite practicar cómo una clase padre define una estructura común y cómo sus clases hijas adaptan el comportamiento a cada especie. **Estado actual:** las clases del modelo están implementadas, pero `Main.java` todavía no contiene un flujo de ejecución ni una interfaz de usuario.

## ✨ Características

- Registro de atributos comunes: nombre de la mascota, edad y nombre del dueño mediante constructores.
- Datos específicos por especie: raza del perro, estado de esterilización del gato y peso del ave.
- Cálculo de costos de consulta según el tipo de animal.
- Generación de una ficha textual con la información de cada mascota y el costo calculado.
- Uso de una clase abstracta para compartir atributos y definir un método obligatorio para las subclases.

## 🧰 Tecnologías y conceptos

- **Java** (sin dependencias externas declaradas).
- Programación orientada a objetos (POO).
- Clases abstractas, herencia y encapsulación.
- Sobrescritura de métodos (`@Override`) y polimorfismo.
- IntelliJ IDEA (se incluyen archivos de configuración del proyecto).

## 🐶 Modelo de animales

| Clase | Atributo particular | Costo de consulta |
| --- | --- | --- |
| `Perro` | `raza` | `45000 + (3000 × edadAnimal)` |
| `Gato` | `esEsterilizado` | `38000` |
| `Ave` | `peso` | `28000 + (100 × peso)` |

Los importes corresponden a valores numéricos definidos en el código; no se especifica una moneda. `Animal` es una clase abstracta y no puede instanciarse directamente.

### ¿Cómo funciona el polimorfismo?

La clase `Animal` declara `calcularCostoConsulta()` sin implementar su cálculo. Cada subclase lo define a su manera. Cuando `ficha()` llama a ese método, Java utiliza la implementación correspondiente al objeto real.

## 📁 Estructura del proyecto

```text
CLINICA-VETERINARIA/
├── README.md
├── src/
│   ├── Animal.java
│   ├── Perro.java
│   ├── Gato.java
│   ├── Ave.java
│   └── Main.java
└── ClinicaVeterinaria.iml
```

*Se omiten los archivos internos de Git y de configuración del IDE para facilitar la lectura.*

## 🖥️ Ejecutar el proyecto localmente

### 1. Requisitos

Tener instalado un **JDK** y, opcionalmente, un editor como IntelliJ IDEA o Visual Studio Code.

### 2. Clonar el repositorio

```bash
git clone https://github.com/sneyderrodriguez/CLINICA-VETERINARIA.git
cd CLINICA-VETERINARIA
```

### 3. Compilar y ejecutar

Desde la raíz del proyecto:

```bash
javac -d out src/*.java
java -cp out Main
```

> **Nota:** `Main.java` contiene un método `main` vacío. Actualmente el programa compila y se ejecuta sin mostrar resultados. Para probar el modelo, es necesario crear instancias y mostrar sus fichas desde ese método.

### Ejemplo de uso opcional

Este fragmento puede añadirse dentro del método `main` de `Main.java`:

```java
Animal mascota = new Perro("Luna", 3, "Carlos", "Labrador");
System.out.println(mascota.ficha());
```

Crea un perro y muestra su ficha. Su costo de consulta será `54000.0` según la fórmula implementada.

## 🚧 Posibles mejoras

- Incorporar un menú para registrar y consultar mascotas.
- Almacenar varios animales en una colección.
- Validar edad y peso para evitar valores incorrectos.
- Añadir pruebas automatizadas para los cálculos de consulta.
- Ampliar el modelo con nuevas especies y funcionalidades.

Estas mejoras son propuestas, **no funcionalidades existentes** en la versión revisada.

## 🔗 Repositorio

[CLINICA-VETERINARIA en GitHub](https://github.com/sneyderrodriguez/CLINICA-VETERINARIA.git)

## 📄 Licencia

Este proyecto está disponible bajo la licencia **MIT**.

Puedes utilizar, modificar y distribuir el código respetando los términos establecidos en dicha licencia.
