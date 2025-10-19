# U2GB-Ejercicios-Guiados-2
Ejercicios guiados para Estructura de Datos. Aquí pondré los códigos profe. Igual lo que tengo en pdf está en los archivos :)


## Lista enlazada con VisuAlgo
Este es un PDF.

## Ejercicios de pila con VisuAlgo
| Imagen | Vista previa |
|--------|--------------|
| Imagen 1 | <img src="[[https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Imagen%20de%20WhatsApp%202025-10-03%20a%20las%2016.05.06_898dd399.jpg?raw=true](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Pila.jpg?raw=true)](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Pila.jpg?raw=true)" width="200" height="200"> |


## Especificaciones de pila
```
package pilas;

/**
 *
 * @author Diana Mabel Garcia Martinez
 *          1224100672
 *          diabegarciamtz@gmail.com    16/10/25
 */
public class StackArray<E> implements IStack<E> {
    private E[] elements;
    private int top = -1;

    /*Creacion de pila al tamaño de 30, 
    se usa el casteo al usar un parentesis y 
    dentro el arreglo generico y despues el object*/
    public StackArray() {
        elements = (E[])new Object[30];
    }
    
    //Creacion del arreglo de la pila al tamaño que sea
    public StackArray(int size) {
        elements = (E[])new Object[size];
    }

    @Override
    public void push(E element) {
        if (top < elements.length - 1) {
            top++;
            elements[top] = element;
        } else {
        // Indicar que está Llena
        System.out.println("La pila está llena.");
        }
    }


    @Override
    public E pop() throws PilaVaciaException {
        if (isEmpty()) {
            System.out.println("La pila está vacía.");
            return null;
        }
            return elements[top--];
    }

    @Override
    public E top() throws PilaVaciaException {
        if (isEmpty()) {
        throw new PilaVaciaException("La pila está vacía.");
        }
        return elements[top];
    }

    @Override
    public E peek() {
        if (isEmpty()) {
            System.out.println("Pila Vacía");
            return null;
        }
            System.out.println("Conociendo el último de la pila");
            return (E) elements[top];
    }


    @Override
    public boolean isEmpty() {
        return top == -1;
    }
    
}
```

```
import pilas.StackArray;


/**
 *
 * @author Diana Mabel Garcia Martinez
 *          1224100672
 *          diabegarciamtz@gmail.com    17/10/25
 */
public class MainStack {
    public static void main(String[] args) {
        StackArray<String> nombres = new  StackArray<String> ();
        
        nombres.push ("vale");
        nombres.push ("susi");
        nombres.push ("pau");
        /*nombres.push ("owen");
        nombres.push ("abel");*/
        
         // Mostramos el último elemento sin eliminarlo
        System.out.println("Elemento en la cima (peek): " + nombres.peek()); // pau

        // Eliminamos el último elemento
        if (!nombres.isEmpty()) {
            System.out.println("Elemento eliminado (pop): " + nombres.pop()); // pau
        }

        // Vista previa del nuevo último elemento
        System.out.println("Nuevo elemento en la cima (peek): " + nombres.peek()); // susi

        // Verificamos si la pila está vacía
        System.out.println("¿La pila está vacía?: " + nombres.isEmpty()); // falsoo

        // Eliminamos todos los elementos restantes
        if (!nombres.isEmpty()) System.out.println("Elemento eliminado: " + nombres.pop()); // susi
        if (!nombres.isEmpty()) System.out.println("Elemento eliminado: " + nombres.pop()); // vale

        // Intentamos eliminar uno más (no hay elementos)
        if (!nombres.isEmpty()) {
            System.out.println("Elemento eliminado: " + nombres.pop());
        } else {
            System.out.println("No se puede eliminar, la pila está vacía.");
        }

        // Verificamos nuevamente si está vacía
        System.out.println("¿La pila está vacía ahora?: " + nombres.isEmpty()); // veda
    }

}


```

## Lista encantada humana Java
Este es un PDF.
| Imagen | Vista previa |
|--------|--------------|
| Imagen 1 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Imagen%20de%20WhatsApp%202025-10-03%20a%20las%2016.05.06_898dd399.jpg?raw=true" width="300" height="300"> |
| Imagen 2 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Imagen%20de%20WhatsApp%202025-10-03%20a%20las%2016.05.03_caa70b7c.jpg?raw=true" width="300" height="300"> |
| Imagen 3 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Imagen%20de%20WhatsApp%202025-10-03%20a%20las%2016.04.56_1ca07a06.jpg?raw=true" width="300" height="300"> |
| Imagen 4 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Imagen%20de%20WhatsApp%202025-10-03%20a%20las%2016.04.26_0a921f8f.jpg?raw=true" width="300" height="300"> |

## Curso Listas Java
Este es un PDF.

## Actividad en clase: listas, listas dobles Java
Este es un PDF.
