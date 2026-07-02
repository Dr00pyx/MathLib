# MathLib 🧮

`MathLib` es una librería estática ligera desarrollada en C++17 diseñada para el almacenamiento, manipulación y ejecución de operaciones algebraicas con matrices bidimensionales. El sistema cuenta con un control estricto de excepciones para garantizar la integridad de la memoria durante las operaciones matemáticas.

## 🚀 Funcionalidades

La librería proporciona una abstracción robusta para el álgebra lineal mediante las siguientes características:

* **Gestión Dinámica de Memoria:** Inicialización segura de matrices parametrizadas por filas y columnas utilizando contenedores estándar (`std::vector`).
* **Suma Matricial ($A + B$):** Operación elemento a elemento con validación estricta de dimensiones idénticas. Lanza una excepción `std::invalid_argument` en caso de discrepancias.
* **Multiplicación Matricial ($A \times B$):** Implementación del algoritmo de producto clásico con validación interna de compatibilidad de dimensiones (las columnas de la primera matriz deben coincidir con las filas de la segunda).
* **Control de Desbordamiento:** Acceso seguro a los elementos mediante métodos que lanzan `std::out_of_range` si se intenta acceder a índices fuera de los límites de la matriz.

---

## 📁 Estructura del Proyecto

El repositorio sigue una arquitectura de desarrollo modular estándar para C++:

```text
MathLib/
├── include/
│   └── Matrix.h         # Interfaz y declaración de la clase Matrix
├── src/
│   └── Matrix.cpp       # Implementación de los métodos algebraicos
├── test/
│   └── test_matrix.cpp  # Pruebas unitarias y demostración de consola
└── README.md            # Documentación general del proyecto
