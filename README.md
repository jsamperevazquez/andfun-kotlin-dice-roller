# Ejercicio Dice Roll  

## Objetivos del ejercicio:

1. Realizar todos los pasos de cada rama (revisar los TODO)
2. Utilizar strings.xml según idioma
3. Cambiar strings en el layout
4. Cambiar las imágenes en drawable 
5. Cambiar la función random por algo similar 
6. Cambiar el estilo por defecto de los botones por material design

### Objetivo 1:

Cada **rama** tiene una acción a realizar con TODO y su respectiva solución
![Imagen Ramas](media/ramas.png)

Propone una serie de tareas a realizar y en la siguiente rama da la solución

### Objetivo 2:
Creo un strings a partir del existente para añadir el lenguaje inglés a la app 
![String ingles](media/eng.png)



### Objetivo 3:

Cambio los nombres a los distintos string que contiene el archivo y añado dos string nuevos para poder accerder a ellos en el código de la app
![Imagen strings](media/strings.png)

### Objetivo 4:

Sustituyo todas las imágenes que trae la aplicación por otras que han sido descargadas.
Para ello añado dichas imágenes al directorio res/drawable.
En el when de la función rollDice hago llamada a cada una de ellas en función del número random.

    diceImage = findViewById(R.id.dice_image)
    }

    private fun rollDice() {
        // cambio la función random() por shuffled.last()
        // Creada rama solución
        val randomInt = (1..6).shuffled().last()
        val drawableResource = when (randomInt) {
            1 -> R.drawable.one
            2 -> R.drawable.two
            3 -> R.drawable.three
            4 -> R.drawable.four
            5 -> R.drawable.five
            else -> R.drawable.six
        }

        diceImage.setImageResource(drawableResource)
    }


Primero cargo mi imagen por defecto en diceImage = findViewById(R.id.dice_image)

![Imagen defecto](media/imagenDefecto.png)

Después en función del número salido en el random() saldrá la imagen correspondiente

![Imagen dado](media/imagenDado.png)



