# Tópicos de Programación - Primer Semestre 2023 (Salón 409, 8:00 AM)

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-2.19+-0175C2?logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Firestore-orange?logo=firebase&logoColor=white)
![Hive](https://img.shields.io/badge/Hive-Local%20Storage-FF9900)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**Proyecto académico: Aplicación de Punto de Venta e Inventario desarrollada en Flutter para la materia de Tópicos de Programación.**

</div>

---

## 📚 Contexto Académico

Este repositorio contiene el desarrollo de una aplicación móvil realizada como parte de la materia **"Tópicos de Programación"** durante el primer semestre de 2023 (grupo del salón 409, 8:00 AM). El objetivo del proyecto es aplicar conceptos modernos de desarrollo móvil, persistencia de datos y arquitectura de software en un caso práctico real: un **sistema de punto de venta para una tienda de abarrotes**.

---

## 🚀 Funcionalidades

La aplicación incluye los siguientes módulos:

- **📦 Gestión de Inventario**
  - Registro, edición y eliminación de productos
  - Clasificación de productos por categorías
  - Visualización del catálogo de productos en almacén

- **🏷️ Gestión de Categorías**
  - Creación y edición de categorías de productos
  - Asociación de productos a categorías existentes

- **🛒 Punto de Venta (Ventas)**
  - Registro de ventas en tiempo real
  - Cálculo automático de totales
  - Historial de transacciones

- **📷 Escáner de Códigos de Barras**
  - Lectura de códigos de barras mediante la cámara del dispositivo (`flutter_barcode_scanner`)
  - Búsqueda rápida de productos escaneados

- **🗄️ Persistencia Dual**
  - Almacenamiento local con **Hive** para operaciones offline rápidas
  - Sincronización con **Cloud Firestore** para respaldo en la nube

- **👥 Gestión de Usuarios**
  - Vista de usuarios registrados en el sistema

---

## 🛠️ Stack Tecnológico

| Tecnología | Uso |
|------------|-----|
| **Flutter** | Framework de UI multiplataforma |
| **Dart** | Lenguaje de programación |
| **Hive** | Base de datos local NoSQL (almacenamiento rápido en disco) |
| **Firebase Core + Cloud Firestore** | Backend en la nube y base de datos remota |
| **flutter_barcode_scanner** | Escaneo de códigos de barras por cámara |
| **google_fonts** | Tipografías personalizadas |
| **eva_icons_flutter** | Conjunto de iconos modernos |
| **path_provider** | Acceso a rutas del sistema de archivos |
| **faker** | Generación de datos de prueba |

---

## 📁 Estructura del Proyecto

```
lib/
├── main.dart                          # Punto de entrada, inicializa Hive y Firebase
├── firebase_options.dart              # Configuración de Firebase por plataforma
├── modelos/                           # Modelos de datos
│   ├── categoria_model.dart
│   └── producto_model.dart
├── controladores/                     # Lógica de negocio (Controllers)
│   ├── agregar_producto_controller.dart
│   ├── categorias_controller.dart
│   ├── editar_categoria_controller.dart
│   ├── ventas_controller.dart
│   └── ver_productos_controller.dart
├── vistas/                            # Interfaces de usuario (Views)
│   ├── menu_vista.dart                # Menú principal de navegación
│   ├── almacen_vista.dart
│   ├── categorias_vista.dart
│   ├── crear_categoria_vista.dart
│   ├── editar_categoria_vista.dart
│   ├── agregar_producto_vista.dart
│   ├── ver_productos_vista.dart
│   ├── ventas_vista.dart
│   ├── ver_users.dart
│   ├── ver_imagen.dart
│   └── vista_prueba.dart
└── widgets/                           # Componentes reutilizables
    └── custom_button_navigation.dart
```

> **Nota educativa:** El proyecto sigue un patrón de separación de responsabilidades inspirado en MVC, donde los `controladores` gestionan el estado y la lógica, y las `vistas` se encargan únicamente de la presentación.

---

## 📦 Instalación y Ejecución

### Requisitos Previos

- Flutter SDK `>=2.19.0 <3.0.0`
- Dart SDK compatible
- Android Studio / VS Code con plugins de Flutter
- Una cuenta de Firebase (para configurar `google-services.json` y `firebase_options.dart`)

### Pasos

```bash
# 1. Clonar el repositorio
git clone https://github.com/ebravo-dev/topicosprimersem2023am.git
cd topicosprimersem2023am

# 2. Instalar dependencias
flutter pub get

# 3. Configurar Firebase
# Asegúrate de que tu proyecto Firebase esté vinculado y que los archivos
# google-services.json (Android) y/o GoogleService-Info.plist (iOS) estén en su lugar.
# El archivo firebase_options.dart ya está configurado para las plataformas habilitadas.

# 4. Ejecutar la aplicación
flutter run
```

---

## 🎯 Objetivos de Aprendizaje

Durante el desarrollo de este proyecto se pusieron en práctica los siguientes conceptos:

- ✅ Programación orientada a objetos en Dart
- ✅ Gestión de estado en Flutter (StatefulWidget + controllers)
- ✅ Persistencia local con Hive (cajas, adaptadores, operaciones CRUD)
- ✅ Integración con Firebase (inicialización, Firestore)
- ✅ Arquitectura por capas (Modelo - Vista - Controlador)
- ✅ Navegación y rutas en Flutter
- ✅ Consumo de plugins nativos (escáner de códigos de barras)
- ✅ Manejo de assets (imágenes, fuentes)
- ✅ Diseño de interfaces responsivas con Material Design

---

## 👥 Autores

**Eder J. Bravo** - [@ebravo-dev](https://github.com/ebravo-dev) - Estudiante / Docente

> Este proyecto fue desarrollado en el contexto de la materia **Tópicos de Programación**, primer semestre 2023, salón 409, turno matutino (8:00 AM).

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Consulta el archivo [`LICENSE`](LICENSE) para más detalles.

---

<div align="center">

**⭐ Proyecto académico - Uso libre para fines educativos ⭐**

</div>
