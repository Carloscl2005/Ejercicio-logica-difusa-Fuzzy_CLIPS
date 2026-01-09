
**Realizado por:**
- Carlos Cerezo López 
- Enrique Moreno Alcántara

<!-- Cabe aclarar que se trabaja con FuzzyClips la sintaxis con java es por aclaración visual -->


# Grafícas visuales de los datos utilizados
<img src="graphics.png" width=80%>

<br>

## Carga de la base de conocimientos
```java
FuzzyCLIPS> (load "Ejercicio_galletas/bc.clp")
Defining deftemplate: indice_cromatico
Defining deftemplate: temperatura_horno
Defining defrule: regla_1 +j
Defining defrule: regla_2 +j
Defining defrule: regla_3 +j
TRUE
```


## Carga de la base de hechos
```java
FuzzyCLIPS> (load "Ejercicio_galletas/bh.clp")
Defining deffacts: hechos
TRUE
```

## Inicialización y ejecución del razonamiento 
Inicializamos el motor mediante ``reset`` y se ejecuta el razonamiento con ``run``.
```java
FuzzyCLIPS> (reset)
FuzzyCLIPS> (run)
```

## Comprobación
* Método Maximum

Seleccionamos el valor con el pico máximo. ``(maximun-defuzzify)`` elige el pico más alto.
```java
FuzzyCLIPS> (maximum-defuzzify 4)
230.0
```

<br>

* Método Moment (Centroide)

Calculamos el centro de gravedad del conjunto difuso de salida. ``(moment-defuzzify)`` calcula el centro de gravedad
```java
FuzzyCLIPS> (moment-defuzzify 4)
206.25
```