# kotlin-fundamentos

## Listas No Mutables

Para crear lista se utiliza *listOf* , este tipo listas no permite modificar

* Sintaxis
lista = listOf<TipoDato> ("valor1","valor2")
* Ejemplo
```bash
fun main() {

    val listaNombre = listOf<String>("Nombre1","Nombre2","Nombre3");
    println(listaNombre);
}
```

## Listas Mutables

Para crear una lista mutable se utiliza *mutableListOf*, este tipo de listas si permite modificar
* Con el metodo add(), se añade nuevos elementos
* Se puede obtner los valores de las listas de dos maneras
* 1. utilizando *get()*
* 2. utilizando el operado indexado *[]*
* 3. utilizando la función *first*
* 4. utilizando la función *firstOrNull* 
* 5. Remover de acuerdo a un index utilizando *removeAt*
* 6. Remover bajo una condición utilizando *removeIf*

Ejemplo
```bash
fun main() {

    val listaVacia = mutableListOf<String>();
    println(listaVacia);
  
    listaVacia.add("Nombre1");
    println(listaVacia);
  
     // 1.
    val valor1 = listaVacia.get(0);
    println(valor1);

     // 2.
    val valor2 = listaVacia[0];
    println(valor2);
    
    // 3.
    val primerValor = listaVacia.first();
    println("Retorna el primer valor de la lista:${primerValor}");
    
    // 4.
    val primerValorONull = listaVacia.firstOrNull();
    println("Retorna el primer valor de la lista en caso de ser null retorna vacio:${primerValorONull}");
    
    // 5.
    val removerAt = listaVacia.removeAt(0);
    println("removerAt:${removerAt}");
    println("listaVacia:${listaVacia}");

    // 6.
    val removerIf = listaVacia.removeIf{caracteres -> caracteres.length >3}
    println("removerAf:${removerIf}");
    println("listaVacia:${listaVacia}");
}
```