# TypeScript III - Leccion II - Task 2

## Intersection Types

¿Cuál es la utilidad del operador de intersección?

- `&` nos permite unir las propiedades de dos tipos de objeto. Para hacer la similitud con las interfaces es como usar la cláusula `extends` pero en este caso se usa con **Type Aliases**. Ejemplo:

```ts
interface Colorful {
  rgb: boolean;
}
interface KeyBoard {
  mechanical: boolean;
}

// w/ Interfaces
interface GamerKeyboard extends KeyBoard, Colorful {}

// w/ Intersection Types
type GamerKeyboard = KeyBoard & Colorful;

const gamerKeyboard: GamerKeyboard = {
  rgb: true,
  mechanical: true,
};
```
