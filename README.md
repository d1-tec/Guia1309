# Guía Lunes 13/09

1. Repaso TDD
2. [Continuación Grafo TDD](https://github.com/d1-tec/Clase0609-polimorfismo-tdd)
3. [Continuación Teórico 1 TDD](https://docs.google.com/presentation/d/1pQ1DpALOuOQTld3mHTcY6T2Pb1vI_2nkq2IKpW0ASEY/edit#slide=id.p)
4. [Teórico 2 TDD](https://docs.google.com/presentation/d/1aRlj_URtnkjLSgZjfYPWfuLwUQhn2SR7qSxBW2GWqi8/edit#slide=id.p)
5. Ejercicio Caché TDD
6. [Ejercicio pendiente de Polimorfismo](https://docs.google.com/presentation/d/1OwemJyp3y8UoPSennA7xagsG0z4CqsMRmsiqCkrkUn4/edit#slide=id.gc938043450_0_189)


## Grafo TDD

- [X] Inicialmente un grafo está vacío
- [X] Si agregamos un nodo a un grafo el mismo ya no está vacío
- [X] Un nodo no puede estar repetido en un grafo
- [X] El grafo es dirigido, por lo que si agregamos arista de A hacia B, no implica que se pueda ir de B hacia A
- [X] Si hay una arista entre dos nodos ambos son adyacentes
- [ ] Si hay un camino entre dos nodos ambos son adyacentes
- [ ] Si pregunto por un nodo adyacente y el mismo no existe se debería lanzar una excepción

## Caché TDD

Construir un POC de una caché, tipo Redis o Memcached, que implemente los siguientes comandos.
Para simplificar el problema asumiremos que la caché solamente guarda strings.

- [ ] `DBSIZE` devuelve el número de claves guardadas. Inicialmente es cero.
- [ ] `SET clave string` almacena el string en el caché, asociándolo con una clave.
- [ ] `SET clave string` lanza una excepción si la clave ya existe.
- [ ] `SET clave string fecha` almacena el string hasta que pase la fecha de expiración. Por defecto de no haber fecha se almacena por 24hrs.
- [ ] `HARDSET clave string fecha` es un set normal pero que sobreescribe el dato anterior, sin lanzar una excepción.
- [ ] `DEL clave` elimina el dato asociado a la clave de la caché.
- [ ] `GET clave` retorna el dato asociado a la clave. Debe contemplarse la expiración de las claves según la fecha que fue pasada.
- [ ] `FLUSHALL` limpia la caché, borrando todos sus datos.
- [ ] `GET SET clave string` actualiza el valor asociado a la clave, pero devuelve el valor previo.
