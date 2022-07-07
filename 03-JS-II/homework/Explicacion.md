1. En un archivo de texto separado que debes crear, escribe explicaciones de los siguientes conceptos como si se lo estuvieras explicando a un niño de 12 años. Hacer esto te ayudará a descubrir rápidamente cualquier agujero en tu comprensión.

* `for`
    El bucle for es una sentencia (un grupo d instrucciones) de repetición, este se repetirá mientra no se 
    no se cumpla la condición que se haciné en su argumento, el for es una forma de repetir una tarea muchas 
    veces sin tener que escribir tantas veces el mismo código.

* `&&`, `||`, `!`
    Los operadores lógicos son comparadores, con ellos podemos saber si las expresiones son verdaderas o falsas.
        && (Y) (AND) este operador solo devolverá verdadero si las condiciones son verdaderas, si una es falsa o ambas son falsas devolverá falso.
        
        || (O) (OR) este operador solo devolverá verdadero si las condiciones si una de sus condiciones es verdadera, solo devolverá falso si ambas son  falsas.

        ! (NO) (NOT) este es un operador de negación devuelve el valor opuesto a la condición, si es verdadero devuelve falso y si es falso devuelve verdadero


nota me tira error el ejercicio este y no encuentro que es lo que pasas.
tira error cuando verifica si alnuno de los num son 0.

function operadoresLogicos(num1, num2, num3) {
  //La función recibe tres números distintos. 
  //Si num1 es mayor a num2 y a num3 y además es positivo, retornar ---> "Número 1 es mayor y positivo"
  //Si alguno de los tres números es negativo, retornar ---> "Hay negativos"
  //Si num3 es más grande que num1 y num2, aumentar su valor en 1 y retornar el nuevo valor.
  //0 no es ni positivo ni negativo. Si alguno de los argumentos es 0, retornar "Error".
  //Si no se cumplen ninguna de las condiciones anteriores, retornar false. 
  if (num1 < 0 || num2 < 0 || num3 < 0) {
    return 'Hay negativos';
  }if (num1 > num2 && num1 > num3 && num1 > 0) {
    return 'Número 1 es mayor y positivo';
  }if (num3 > num1 && num3 > num2 && num3 > 0) {
    return num3 + 1;
  }if (num1 === 0 || num2 === 0 || num3 === 0) {
    return "Error";
  } else {
    return false;
  }
}



Fallos:

 ● operadoresLogicos(num1, num2, num3) › should return 'Error' if any of the arguments are equal 0

    expect(received).toBe(expected) // Object.is equality

    Expected: "Error"
    Received: 11

      148 |   });
      149 |   it('should return \'Error\' if any of the arguments are equal 0', function() {
    > 150 |     expect(operadoresLogicos(1, 0, 10)).toBe('Error');
          |                                         ^
      151 |   });
      152 |   it('should return false if none of the conditions are met', function() {
      153 |     expect(operadoresLogicos(10, 30, 6)).toBe(false);

      at Object.<anonymous> (03-JS-II/homework/tests/JSII.test.js:150:41)

  ● tablaDelSeis() › should return multiplication table of 6

    expect(received).toEqual(expected) // deep equality

    - Expected  - 13
    + Received  +  1

    - Array [
    -   0,
    -   6,
    -   12,
    -   18,
    -   24,
    -   30,
    -   36,
    -   42,
    -   48,
    -   54,
    -   60,
    - ]
    + Array []

      182 | describe ('tablaDelSeis()', function() {
      183 |   it('should return multiplication table of 6', function() {
    > 184 |     expect(tablaDelSeis()).toEqual([0 , 6, 12, 18, 24, 30, 36, 42, 48, 54, 60]);
          |                            ^
      185 |   });
      186 | });
      187 |

      at Object.<anonymous> (03-JS-II/homework/tests/JSII.test.js:184:28)
