### Tarea

*Los ejercicios se encuentran en* https://github.com/hackademymx/ejercicios-js y en este repositorio.

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
