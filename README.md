# CifradoCesar_Atbash

Progama simple para cifrar y descifrar usando los métodos Cesar y Atbash.

Documentación del código:
Fig. 1
• Atajo para selección de ids del DOM.
• Función para la limpieza de caracteres repetidos dentro del cuadro de texto designado para indicar los caracteres a usar. Recorre el texto y guarda los caracteres ya vistos para construir una versión sin repetidos.
Fig. 2
• Valida el conjunto de caracteres usados como alfabeto para asegurarnos de que tiene al menos dos caracteres y que no tenga caracteres repetidos. Esto con el fin de evitar Cadena ambiguas o sin sentido por la posición de caracteres repetidos.
Fig. 3
• Función para realizar el cifrado César: Recibe el texto, el conjunto de caracteres permitido (alfabeto) y el desplazamiento indicado por el usuario. Busca cada carácter dentro del alfabeto y lo mueve cierto número de posiciones usando aritmética modular para no salir del rango. Si el carácter no pertenece al alfabeto, se deja sin cambios.
Fig. 4
• Función para realizar el cifrado Atbash: Recorre el texto y sustituye cada carácter por su opuesto dentro del alfabeto definido, tomando la posición inversa respecto al final del conjunto. En caso de que el carácter no exista en el alfabeto, se conserva igual. Este método es autoinverso, por lo que cifrar y descifrar es el mismo proceso.
Fig. 5
• Función para calcular la plausibilidad del texto: Evalúa qué tan “legible” parece una cadena contando letras, espacios y símbolos comunes, asignando un puntaje positivo a caracteres esperados y negativo a caracteres poco comunes. Se utiliza para comparar resultados y estimar el tipo de cifrado aplicado.
Fig. 6
• Función para estimar el desplazamiento del cifrado César: Prueba todos los desplazamientos posibles dentro del alfabeto y calcula el puntaje de plausibilidad de cada resultado. Se selecciona el desplazamiento que produce el texto más coherente, devolviendo el shift estimado y el texto más probable.
Fig. 7
• Función para detectar el tipo de cifrado utilizado: Aplica el método Atbash y también prueba el cifrado César con distintos desplazamientos. Compara los puntajes obtenidos y determina cuál método produce un resultado más lógico, mostrando si el texto fue cifrado con César o Atbash.
Fig. 8
• Función para actualizar el estado del sistema: Muestra mensajes en la interfaz indicando si el proceso fue correcto o si hubo algún error, cambiando el texto y el color del indicador para informar al usuario.
Fig. 9
• Función principal de ejecución del programa: Obtiene las opciones seleccionadas por el usuario, valida el alfabeto, aplica el cifrado o descifrado correspondiente y muestra el resultado. Además, ejecuta la detección automática del tipo de cifrado y actualiza los indicadores en pantalla.
Fig. 10
• Evento del botón Ejecutar: Asocia el botón principal con la función de ejecución para que el sistema procese el texto cuando el usuario presiona el botón.
• Evento del botón Eliminar repetidos: Limpia el conjunto de caracteres definido por el usuario eliminando duplicados, valida el resultado y muestra un mensaje indicando si el alfabeto quedó correcto.
Fig. 11
• Evento del botón Intercambiar entrada y salida: Permite cambiar el texto de entrada por el resultado obtenido para facilitar el descifrado o realizar nuevas pruebas sin volver a escribir el mensaje.
• Evento del botón Copiar salida: Copia el texto generado al portapapeles del sistema para que el usuario pueda pegarlo en otro documento o aplicación.
