# U2GB-Ejercicios-Guiados-2
Ejercicios guiados para Estructura de Datos. Aquí pondré los códigos profe. Igual lo que tengo en pdf está en los archivos :)

##  Tabla de Contenidos

| Documento | Tipo | Descripción | Ver PDF |
|-----------|------|-------------|---------|
| **Lista enlazada con VisuAlgo** | `📄 PDF` | Ejercicios de listas enlazadas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Ejercicio%20de%20Lista%20Enlazada%20Simple%20con%20VisualAlgo.pdf) |
| **Curso Listas Java** | `📄 PDF` | Curso completo sobre listas en Java | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/dc4b62ab706778e21e997f26bcb808acfb092cdd/Curso%20Listas%20Java.pdf)|
| **Actividad en clase: listas, listas dobles Java** | `📄 PDF` | Actividades prácticas de listas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Actividad%20en%20clase%20listas%2C%20listas%20dobles%20Java.pdf) |
| **Lista encantada humana Java** | `📄 PDF` | Ejercicio especial de lista encantada | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/raw/main/Lista%20encantada%20humana%20Java.pdf) |

## Lista enlazada con VisuAlgo
Este es un PDF.

## Ejercicios de pila con VisuAlgo
| Imagen | Vista previa |
|--------|--------------|
| Imagen 1 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Pila.jpg?raw=true" width="300" height="400"> |


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
| Lista Encantada Humana 1 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Lista%20Encantada%20Humana1.jpg?raw=true" width="300" height="300"> |
| Lista Encantada Humana 2 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Lista%20Encantada%20Humana2.jpg?raw=true" width="300" height="300"> |
| Lista Encantada Humana 3 | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Lista%20Encantada%20Humana3.jpg?raw=true" width="300" height="300"> |


## Curso Listas Java
Este es un PDF.

## Actividad en clase: listas, listas dobles Java
Este es un PDF.
| Imagen | Vista previa |
|--------|--------------|
| Imagen: Listas simples | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Listas%20simples.jpg?raw=true" width="300" height="400"> |
| Imagen: Listas simples y dobles | <img src="https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Listas%20simples%20%20y%20dobles.jpg?raw=true" width="300" height="400"> |

### Pseudocódigo
1. Crear nuevo nodo
2. Acceder a cabeza
3. Verificar que la referencia no sea nula en ambas direcciones
4. Insertar el nuevo nodo uniendolo al anterior (doble referencia)
```
FUNCIÓN Insertar()
    temp = cabeza
    MIENTRAS (temp.derecha != nulo) 
        temp <- temp.derecha
    FIN MIENTRAS
            temp.derecha <- Nodo(datos)
            temp.derecha.izquierda = temp
FIN FUNCIÓN
```

```
FUNCIÓN Recorrer()
    temp = cabeza
    MIENTRAS (temp.derecha != nulo) 
        temp <- temp.derecha
        Imprimir temp
    FIN MIENTRAS
FIN FUNCIÓN
```
