# 🎸 GuitarLA - React + Custom Hooks

Proyecto de tienda de guitarras desarrollado con **React**, enfocado en la arquitectura limpia mediante la extracción de lógica a **Hooks personalizados**.

> 🚀 **Demo en vivo:** [https://guitarla-nine.vercel.app](https://guitarla-nine.vercel.app)

---

## 🏗️ Arquitectura del Proyecto: Custom Hooks

La característica principal de este proyecto es la creación de un hook personalizado llamado `useCart.js`. Esta técnica permite:

- **Separación de Conceptos:** Los componentes `Header` y `Guitar` solo se encargan de la interfaz (UI), mientras que la lógica del carrito reside en un solo lugar.
- **Reutilización:** La lógica de agregar, eliminar y calcular totales puede ser utilizada por cualquier componente sin duplicar código.
- **Código Limpio:** El componente principal `App.jsx` se mantiene pequeño y fácil de leer al delegar las funciones al hook.

### 🧠 Lógica de JavaScript Implementada en `useCart`

Dentro del hook, utilicé funciones avanzadas para garantizar un rendimiento óptimo:

- **`useMemo` para Performance:** El cálculo del total del carrito (`cartTotal`) y la comprobación de si está vacío (`isEmpty`) solo se ejecutan cuando el carrito cambia.
- **Persistencia con `localStorage`:** Implementé un `useEffect` para sincronizar automáticamente el estado del carrito con el almacenamiento del navegador.
- **Manejo Inmutable del Estado:** Uso de métodos como `.map()` para actualizar cantidades y `.filter()` para eliminar productos, siguiendo las mejores prácticas de React.
- **Validaciones de Negocio:** El hook controla límites de stock (mínimo 1, máximo 5 unidades por producto).

---

## 🛠️ Stack Tecnológico

- **React.js** (Vite)
- **Custom Hooks** (Lógica de Carrito)
- **Bootstrap** (Diseño y Grilla)
- **LocalStorage** (Persistencia de datos)

---

## 📖 Aprendizajes Clave

1. **State Derivado:** En lugar de crear múltiples estados, utilicé `useMemo` para derivar valores del estado principal, manteniendo la "fuente de verdad" única.
2. **Inicialización Lazy de State:** El carrito carga los datos de `localStorage` solo una vez al iniciar la aplicación, mejorando el rendimiento.
3. **Comunicación entre Componentes:** Implementación eficiente de paso de funciones y datos mediante _props_.

---

## 🔧 Instalación

1. **Clonar repositorio:**

   ```bash
   git clone [https://github.com/TriniRs/guitarLA-useCart.git](https://github.com/TriniRs/guitarLA-useCart.git)

   ```

2. Instalar dependencias:
   npm install

3. Ejecutar en modo desarrollo:
   npm run dev
