# JavaScript

### ¿Qué es JavaScript?

Es un lenguaje de programación o de secuencias de comandos que te permite implementar f**unciones complejas en páginas web**, *más allá de información estática para que la veas,* como **actualizaciones de contenido, mapas interactivos, animación de Gráficos 2D/3D, desplazamiento de máquinas reproductoras de vídeo, etc., JavaScript suele estar involucrado.

<aside>
🖱️ JavaScript nace de la necesidad de que las páginas web sean interactivas.

</aside>

---

*En la mentoría, empezará en VSC con un archivo de **html,** creamos un **template** con **html: 5.***

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    Buenas, estrellita, la tierra te dice: Holi. Tqm.
</body>
<script>
    <!-- Asi se hacen comentarios -->
    <!-- Para imprimir en consola -->
    console.log("Primer texto impreso en consola")
    console.error("Primer error para consola")
    <!-- Otras opciones error, log, warn, info-->
</script>
</html>
```

**Peeeeero, tenemos que separar la lógica de la imagen para no tener un file tan largo.**

*Creamos un nuevo archivo para el **script** y en el de **html** hacemos un cambio*

```html
<script src="./script.js">
    <!--Cambiamos la fuente al archivo script-->
</script>
```

En resumen: 

- **html** crea plantillas
- **css** decora las plantillas
- **javascript** da funcionalidad a las plantillas

<aside>
🖱️ Para abrir el JavaScript en el navegador y que se actualicen los cambios usamos la **extensión Live Server (F1)**, ahí podemos usar la dirección IP o **[localhost:5500](http://localhost:5500)** *(en este ejemplo)* **en el navegador.**

</aside>

Así se ve el puerto del Live Server

![Captura de pantalla 2022-02-03 145740.png](JavaScript%203b3bcf832f32487b9611e352e90e8482/Captura_de_pantalla_2022-02-03_145740.png)

---

### Variables y constantes

Para declarar constantes usamos: **const.**

Para declarar variables usamos:  **let** *(let es local, var ya no se usa).*

<aside>
☢️ Es una mala práctica sólo usar **let** porque consumen más espacio de memoria.

</aside>

```jsx
/* Constantes y variables */
const nombre = 'Kokoro Bebe';

/* No puedo cambiar el nombre de Kokoro bebe, porque
yo lo declare como constante no como variable*/

/*Ahora veamos algo variable, como los meses que tiene Kokoro*/
let edad = 4;

console.log(
    "El nombre de mi mascota es: "+ nombre + "y tiene : " + edad + " meses"
);

/* Ya pasados dos meses*/
edad = 6;

console.log(
    "El nombre de mi mascota es: "+ nombre + "y tiene : " + edad + " meses"
);

/*Otro tipo de dato es es booleano: TRUE or FALSE*/

let decision = true;
```

### Operaciones lógicas

Usando operaciones lógicas y tomando las variables booleanas, podemos hacer un condicional

```jsx
if(edad > 6){
    console.log(`${nombre} es una gatita bebé`)
} else{
    console.log(`${nombre} es una gatita adulto`)
}
// Otra forma de hacer lo mismo, es usar los ternarios.
edad > 4 ? console.log('minino adulto') : console.log('minino bebe')
```

Para hacer el **and** y el **or** usamos ***&&*** y ***||*** respectivamente.

Algo interesante en cuanto a las comparaciones

```jsx
const number = 20;
console.log(number == '20')
```

Esto nos arroja un ***True*** a pesar de estar comparando un entero con un string, pero si agregamos otro **=**

```jsx
console.log(number === '20')
```

Obtendremos un ***False*** debido a que se comparará también el tipo de dato.

### Ciclos

Veamos la estructura de un ***for*** combinado con un ****if**

```jsx
for(let indice = 0; indice < 4; indice ++) {
    if(indice === 2){
        console.log('2')
    } else{
        console.log('Otra accion')
    }
}
```

Nota: en la consola, la acción que se repite más de una vez se verá así

![Captura de pantalla 2022-02-02 021822.png](JavaScript%203b3bcf832f32487b9611e352e90e8482/Captura_de_pantalla_2022-02-02_021822.png)

Ahora, para romper el ciclo usamos ***break***

```jsx
for(let indice = 0; indice < 4; indice ++) {
    if(indice === 2){
        console.log('2');
        break;
    } else{
        console.log('Otra accion');
    }
}
```

Eso terminaría el ciclo luego de encontrar el 2.

### Arreglos

La estructura de un arreglo es la siguiente

```jsx
const arreglo = ['Semi', 'Sahire','Hector','Betuel'];
console.log(arreglo)
```

Que arroja en consola, *note que se inicia contando en 0*

![Captura de pantalla 2022-02-02 022412.png](JavaScript%203b3bcf832f32487b9611e352e90e8482/Captura_de_pantalla_2022-02-02_022412.png)

Para ver elementos de arreglo

```jsx
console.log(arreglo[2]);
//Asi veriamos el nombre de Hector
```

Tenemos una variante del ***for***, el ***método forEach***

```jsx
arreglo.forEach((nombres) =>
console.log(`El nombre de la persona es ${nombres}`)
);
//Imprime lo mismo que el for, pero mas elegante
```

Estructura de un ***while*** que imprime números del 0 al 999

```jsx
let contador = 0;
while (contador < 1000){
    console.log(contador);
    contador = contador +1;
}
```

La diferencia está en que en el ***for***, ya debemos saber cuantas veces se ejecuta el ciclo o cuando se dejará de ejecutar.

### Funciones

Para crear funciones tendremos la siguiente sintaxis

```jsx
function Saludar(nombre){
    console.log(`Hola ${nombre}, ¿cómo estás?`);
}

Saludar(nombre);
```

*Nota: si la variable de entrada no está definida, obtendremos un dato **undefined.***

### ¿Qué son los objetos en JavaScript?

Un ***objeto*** es un entidad independiente con propiedades y tipos. *Como los diccionarios de Python.*

Sintaxis de un objeto

```jsx
const gato1 = {
    nombre: 'Kokoro',
    apellido: 'Bebe',
    edad: 4,
};
```

### Ejercicios de tarea

*Los ejercicios se encuentran en* https://github.com/hackademymx/ejercicios-js.

(*Vamos a resolver en el archivo script.js)*

1. **Dado un arreglo de números enteros, Imprimir solamente aquellos que son denominados números primos, (usar arreglo denominado como "ejercicio1").** 

```jsx
const ejercicio1 = [
  3, 100, 85, 64, 46, 39, 40, 30, 20, 24, 25, 6, 10, 54, 82, 71, 67, 77, 17, 29,
  19, 88, 456, 13, 23, 24,
];

// R E S O L U C I Ó N 1

const EsPrimo = numero => {
  if (numero == 0 || numero == 1) return false;
  for (let n=2;n<numero;n++){
    if (numero % n ==0) return false;
  }
  return true;
}
console.log(ejercicio1)
console.log(EsPrimo(2))

for (let i = 0; i< ejercicio1.length; i++) {
  if (EsPrimo(ejercicio1[i])) console.log(ejercicio1[i]);
}
```

1. **Ramón quiere hacer una fiesta privada en donde solo entre un número exclusivo de personas, ayúdale al portero a solo dejar pasar a aquellas personas mayores de edad que sean familiares de Ramón. (Con imprimir los usuarios que se admitirán basta, usar el arreglo denominado como "ejercicio2").** 

```jsx
const ejercicio2 = [
  {
    nombre: "Gabriel",
    edad: 22,
    esFamiliar: false,
  },
  {
    nombre: "Jaime",
    edad: 15,
    esFamiliar: true,
  },
  {
    nombre: "María",
    edad: 18,
    esFamiliar: true,
  },
  {
    nombre: "Angel",
    edad: 19,
    esFamiliar: true,
  },
  {
    nombre: "Fer",
    edad: 18,
    esFamiliar: true,
  },
  {
    nombre: "Rachel",
    edad: 30,
    esFamiliar: true,
  },
];

// R E S O L U C I Ó N 2
// Solo van a pasar >=18 y familiares de Ramón

const Filtro = (persona) => {
  if (persona.edad >= 18 && persona.esFamiliar){
    console.log(persona.nombre)
  }
}
ejercicio2.forEach((persona) => {Filtro(persona)});
```

1. **Con ayuda de ciclos imprime los primeros 50 números de la sucesión de Fibonacci, (1,1,2,3,5,8,13,21).**

```jsx
// R E S O L U C I Ó N 3

function Fibo(n){
  let l = [];
  let a = 1;
  let b = 1;
  l.push(a,b);
  for (let k=1; k<n-1; k++){
    c = a+b;
    l.push(c)
    a = b;
    b = c;
  };
  return l
}

console.log(Fibo(50))
```