# sort & toSorted

* Metodo sort
    Devuelve un array ordenado, pero tambien ordena el array original

* Metodo toSorted
    Devuelve un array ordenado, pero mantiene el orden el array original

    ```
    const nums = [4, 5, 7, 3, 8, 0, 1]
    const arraySorted = nums.sort();
    
      console.log(nums); // [0, 1, 3, 4, 5, 7, 8]
      console.log(arraySorted); // [0, 1, 3, 4, 5, 7, 8]
    
    const arrayToSorted = nums.toSorted();
      console.log(nums); // [4, 5, 7, 3, 8, 0, 1]
      console.log(arraySorted); // [0, 1, 3, 4, 5, 7, 8]
    
    ```



    
resolver el excuse generator con recursividad


# recorrido de un arbol binario

### ¿Que es un Arbol binario?

Es una estructura de datos jerárquica en la programación y ciencias de la computación. Consiste en nodos, donde cada nodo puede tener hasta dos nodos secundarios, comúnmente llamados el hijo izquierdo y el hijo derecho. Cada nodo en un árbol binario tiene un valor y, opcionalmente, puede tener un enlace a uno o dos nodos secundarios.

#### Como se crea un arbol binario
<image src="/CleanShot 2023-10-06 at 02.47.47.png" alt="Descripción de la imagen">

#### Recorrido de un arbol binario

<image src="/CleanShot 2023-10-06 at 02.32.01.png" alt="Descripción de la imagen">



### array.reduce y aplicar ordenamiento burbuja

```
const numeros = [1, 2, 3, 4, 5];

const suma = numeros.reduce((acumulador, elementoActual) => {
  return acumulador + elementoActual;
}, 0);

console.log(suma); // Resultado: 15

```

#### Ordenamiento Burbuja

```
const burbuja = (arr) => {
    let long = arr.length;
    let intercambio;

    do{
        intercambio = false;
        for(let i = 0; i < long -1; i++){
            intercambio = arr[i] > arr[i + 1] ? ([arr[i], arr[i + 1]] = [arr[i + 1], arr[i]], true) : false;
        }
    }
    while(intercambio);
    return arr;
};

// ejemplo

const num = [3, 2, 1, 5, 4, 30, 50, 8, 6, 7, 9];
console.log(burbuja(num));


```




### Instanciar un objeto
¿Que es Instanciar un objeto?
Es un paradigma de programacion orientada a objetos, aunque JS es un lenguaje de POO tiene peculiaridades que vale la pena mencionar
En JS no habia clases en el sentido tradicional hasta la llegada de ECMAScript 6, que introdujo la palabra class para definir clases, antes de ES6 se usaban funciones constructoras para crear objetos

Ejemplos

Antes de ES6
```
// Definición de una función constructora
function Coche(marca, modelo, año) {
    this.marca = marca;
    this.modelo = modelo;
    this.año = año;

    this.arrancar = function() {
        console.log(`El coche ${this.marca} ${this.modelo} arrancó.`);
    }
}

// Instanciación de un objeto
let miCoche = new Coche("Toyota", "Corolla", 2020);

```

Despues de ES6

```
// Definición de una clase
class Coche {
    constructor(marca, modelo, año) {
        this.marca = marca;
        this.modelo = modelo;
        this.año = año;
    }

    arrancar() {
        console.log(`El coche ${this.marca} ${this.modelo} arrancó.`);
    }
}

// Instanciación de un objeto
let miCoche = new Coche("Toyota", "Corolla", 2020);

```



