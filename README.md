# U2GB-Ejercicios-Guiados-2
Ejercicios guiados para Estructura de Datos. Aquí pondré los códigos profe. Igual lo que tengo en pdf está en los archivos :)

##  Tabla de Contenidos

| Documento | Tipo | Descripción | Ver PDF |
|-----------|------|-------------|---------|
| **Lista enlazada con VisuAlgo** | `📄 PDF` | Ejercicios de listas enlazadas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Ejercicio%20de%20Lista%20Enlazada%20Simple%20con%20VisualAlgo.pdf) |
| **Pila con VisuAlgo** | `📄 PDF` | Ejercicios de pilas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Ejercicios%20de%20Pila%20con%20VisuAlgo.pdf) |
| **Curso Listas Java** | `📄 PDF` | Curso completo sobre listas en Java | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/dc4b62ab706778e21e997f26bcb808acfb092cdd/Curso%20Listas%20Java.pdf)|
| **Curso Colas** | `📄 PDF` | Curso Colas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Curso%20Colas.pdf) |
| **Curso Listas y Pilas** | `📄 PDF` | Curso Listas y Pilas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Curso%20Listas%20y%20Pilas.pdf) |
| **Actividad en clase: listas, listas dobles Java** | `📄 PDF` | Actividades prácticas de listas | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Actividad%20en%20clase%20listas%2C%20listas%20dobles%20Java.pdf) |
| **Lista encantada humana Java** | `📄 PDF` | Ejercicio especial de lista encantada | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Lista%20Encantada%20Humana%20en%20Java.pdf) |
| **Actividad en clase: Ordenamiento Burbuja** | `📄 PDF` | Ordenamiento Burbuja | [Ver PDF](https://github.com/diabegarciamtz-coder/U2GB-Ejercicios-Guiados-2/blob/main/Ordenamiento%20Burbuja%20.pdf) |






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
## Actividad en clase: colas
```
package colas;

import java.util.HashSet;

/**
 *
 * @author Diana Mabel Garcia Martinez
 *          1224100672
 *          diabegarciamtz@gmail.com    24/10/25
 */
public class Cola <T> {
    private Nodo<T> cabeza; //este va enfrente, donde insertamos
    private Nodo<T> cola;   //este va atras, donde eliminamos
    private int tamano;     //para ver el tamano

    public Cola() {           //todo en 0's
        this.cabeza = null;  //no tenemos cabeza
        this.cola = null;   //no tenemos cola
        this.tamano = 0;   //iniicaliza el tamano en vacio
    }

    public void setCabeza(Nodo<T> cabeza) {
        this.cabeza = cabeza;
    }

    public void setCola(Nodo<T> cola) {
        this.cola = cola;
    }

    public void setTamano(int tamano) {
        this.tamano = tamano;
    }

    public Nodo<T> getCabeza() {
        return cabeza;
    }

    public Nodo<T> getCola() {
        return cola;
    }

    public int getTamano() {
        return tamano;
    }
    
    public boolean colaVacia(){ //revisa si esta vacia
        return cabeza == null;
    }
    
    public void insertar(T elemento){   //encola
        Nodo <T> nuevoNodo = new Nodo<>(elemento);
        
        if (colaVacia()){   //le habla al metodo para ver si esta vacia
            cabeza = nuevoNodo;
            cola = nuevoNodo;
        }
        else{   //si no esta vacia
            this.cola.setSiguiente(nuevoNodo);  //el nodo que era final ahora apunta al nuevo
            this.cola = nuevoNodo;  //ahora es el nuevo nodo
        }
        tamano++;   //crecemos el tamano
        System.out.println("-> Insertado: "+elemento); //referimos lo que se inserto
    }
    
    public T quitar(){
        if(colaVacia()){    //verificamos si esta vacia
            System.out.println("Error: la cola está vacia.");
        }
        
        T datoQuitado = this.cabeza.getDato(); //en esta variable guardamos el dato a devolver
        
        this.cabeza = this.cabeza.getSiguiente(); //el nodo de atras ahora es cabeza
        
        if(this.cabeza == null){ //actualiza en caso de que no haya elementos
            this.cola = null;
        }
        
        tamano--; //disminuimos el tamano de la cola
        return datoQuitado; 
    }
    
    //Devuelve el elemento que tenemos al frente sin eliminarlo
    public T frente(){
        if(colaVacia()){
            System.out.println("Error: la cola esta vacia");
        }
        return this.cabeza.getDato();
    }
}

```

```

package colas;

/**
 *
 * @author Diana Mabel Garcia Martinez
 *          1224100672
 *          diabegarciamtz@gmail.com    24/10/25
 */
public class Nodo <T> {
    private T dato;
    private Nodo siguiente;
    
    public Nodo (T data){
        dato = data;
        siguiente = null;
    }

    public T getDato() {
        return dato;
    }

    public Nodo getSiguiente() {
        return siguiente;
    }

    public void setDato(T dato) {
        this.dato = dato;
    }

    public void setSiguiente(Nodo siguiente) {
        this.siguiente = siguiente;
    }

    @Override
    public String toString() {
        return "Nodo{" + "dato=" + dato + ", siguiente=" + siguiente + '}';
    }
    
}

```

```
package colas;

import java.util.Scanner;

/**
 *
 * @author Diana Mabel Garcia Martinez
 *          1224100672
 *          diabegarciamtz@gmail.com    24/10/25
 */
public class MainCola {
    public static void main(String[] args) {

        Cola<String> colaTareas = new Cola<>();
        Scanner scanner = new Scanner(System.in);
        int opcion;

        do {
            System.out.println("\n--- MENÚ DE OPERACIONES ---");
            System.out.println("1. Insertar tarea");
            System.out.println("2. Consultar frente");
            System.out.println("3. Quitar tarea");
            System.out.println("4. Mostrar estado de la cola");
            System.out.println("5. Mostrar tamaño");
            System.out.println("0. Salir");
            System.out.print("Seleccione una opción: ");
            opcion = scanner.nextInt();
            scanner.nextLine(); // Limpiar buffer

            switch (opcion) {
                case 1:
                    System.out.print("Ingrese la tarea a insertar: ");
                    String tarea = scanner.nextLine();
                    colaTareas.insertar(tarea);
                    scanner.nextLine();
                    break;

                case 2:
                    if (!colaTareas.colaVacia()) {
                        System.out.println("Tarea al frente: " + colaTareas.frente());
                    } else {
                        System.out.println("La cola está vacía.");
                    }
                    scanner.nextLine();
                    break;

                case 3:
                    if (!colaTareas.colaVacia()) {
                        String quitada = colaTareas.quitar();
                        System.out.println("Tarea quitada: " + quitada);
                    } else {
                        System.out.println("No se puede quitar, la cola está vacía.");
                    }
                    scanner.nextLine();
                    break;

                case 4:
                    if (!colaTareas.colaVacia()) {
                        System.out.println("Estado actual de la cola:");
                        Nodo<String> actual = colaTareas.getCabeza();
                        while (actual != null) {
                            System.out.println("- " + actual.getDato());
                            actual = actual.getSiguiente();
                        }
                    } else {
                        System.out.println("La cola está vacía.");
                    }
                    scanner.nextLine();
                    break;

                case 5:
                    System.out.println("Tamaño actual de la cola: " + colaTareas.getTamano());
                    scanner.nextLine();
                    break;

                case 0:
                    System.out.println("Saliendo del programa...");
                    //scanner.nextLine();
                    break;

                default:
                    System.out.println("Opción inválida. Intente de nuevo.");
            }
        } while (opcion != 0);

        scanner.close();
    }
}

```
