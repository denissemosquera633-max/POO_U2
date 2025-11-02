# 🧩 Deber de POO Unidad 2

## 1. ⚙️ Metodología y Objetivos de Ingeniería

Este proyecto representa la culminación de un ejercicio de **Ingeniería de Software** orientado a la aplicación de principios de la Programación Orientada a Objetos (POO) en Java.

**Objetivo Central:** Construir un sistema altamente **cohesivo y de bajo acoplamiento** capaz de gestionar una jerarquía de contenidos de medios mediante la validación del contrato de interfaz.

### Principios de Diseño Atestados:
* **Herencia y Abstracción:** Creación de una jerarquía base a partir de una clase no instanciable.
* **Polimorfismo:** Cumplimiento de un contrato de método en múltiples clases derivadas.
* **Modularidad:** Separación de la lógica de prueba (`poo`) de las entidades (`uni1a`).
* **Relaciones Avanzadas:** Uso técnico de Agregación y Composición.

***

## 2. 🗂️ Estructura del Artefacto de Software

El código fuente del proyecto se organiza en paquetes lógicos para facilitar la separación de responsabilidades y el mantenimiento.

### 2.1. Estructura de Directorios del Repositorio

El proyecto mantiene una estructura clara para el desarrollo en IDEs basados en Maven/Gradle (o Eclipse):

Poo_unidad1/
├── .gitignore/
├── README.md/
└── src/

    ├── poo/
    │   └── PruebaAudioVisual.java (Driver de Ejecución y Validacion)
    └── uni1a/
        ├── ContenidoAudiovisual.java (Interfaz Lógica Abastracta)
        ├── Subclases de Contenido (Pelicula, Documental, SerieDeTV, Cortometraje, VideoYoutube)
        └── Clases de Soporte (Actor, Temporada, Investigador)


### 2.2. Validaciones Arquitectónicas Clave

| Clase de Contenido | Patrón de Asociación Implementado | Símbolo UML (Referencia) |
| :--- | :--- | :--- |
| **\`Pelicula\`** | Agregación con \`Actor\` (Débil) | Rombo Hueco |
| **\`SerieDeTV\`** | Agregación con \`Temporada\` (Débil) | Rombo Hueco |
| **\`Documental\`** | Composición con \`Investigador\` (Fuerte) | Rombo Sólido  |

***

## 3. 🛠️ Protocolo de Inicialización y Prueba

### Paso 1: Adquisición del Código Base (Clonación)

Ejecute el siguiente comando para replicar el repositorio localmente. Se asume que Git está configurado en el entorno de línea de comandos:

\`\`\`bash
git clone https://github.com/denissemosquera633-max/POO_U2.git
cd Poo_unidad1
\`\`\`

### Paso 2: Integración en el IDE

1.  Abra su IDE (Eclipse, IntelliJ).
2.  Utilice la opción **Importar Proyecto Existente** y seleccione la carpeta `Poo_unidad1`.
3.  El IDE resolverá automáticamente las referencias entre los paquetes **`poo`** y **`uni1a`**.

### Paso 3: Ejecución de la Prueba de Validación

1.  Abra la clase **\`PruebaAudioVisual.java\`** (`src/poo/`).
2.  Ejecute la clase. El sistema creará un **arreglo polimórfico** (`ContenidoAudiovisual[]`) y llamará al método `mostrarDetalles()` en cada elemento.
