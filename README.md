# Editor de imagenes
 
-----------------------------------------------------------------
#Dependencias:

cv2(opencv-python)
PIL
numpy
matplotlib
scipy
pylab
nt_toolbox
tkinter
-----------------------------------------------------------------

#MENU ARCHIVO:

Cuenta con 2 opciones:

-Abrir: sirve para importa la imagen a procesar hacia el editor, mediante su busqueda en las carpertas del ordenador del usuario.

-Salir: permite cerrar la ventana "Editor de Imagenes".

#MENU PROC_GLOBALIMAGENES:

Cuenta con 6 opciones:

-Estructura .bmp: Permite observar la estructura de una imagen con extensión .bmp por lo cual, la imagen que abramos tiene que tener dicha extensión. Se visualizará su estructura en el terminal.

-rgb a grises: como su nombre lo indica permite convertir la imagen abierta a escala de grises.

-Contraste: Mediante la barra de contraste podemos indicar el nivel que queremos contrastar la imagen para luego hacer clic en la opción contraste con esto se logrará como resultado la imagen original y la imagen contrastada al nivel que se halla colocado.

-Ecualizar: Mediante esta función podemos aplicar una ecualizar a la imagen original gracias a la libreria equalizeHist de opencv.

-Brillo: Mediante la barra de control de imagenes podemos indicar  el nivel de brillo que se desea en la imagen para luego hacer clic en la opción brillo con esto se logrará como resultado la imagen original y la imagen con el brillo al nivel que se halla colocado.
 
-Umbralizar: Utilizando la barra de control de imagenes podemos indicar el valor del umbral para generar la imagen en blanco y negro.

#MENU TRANS_LOCALES:

cuenta con 14 opciones:

-Suavisar: es un filtro simple que suaviza la imagen segun el tamaño del kernel y los coeficientes.

-Filtro Promedio: En este filtro a diferencia del suavizado se puede modificar el kernel mediante la barra de control de imagenes (procurar que sean valores impares, por ejemplo: 1, 3, 5, etc.) y de esa manera genera una suavizado mediante el promedio de los pixeles vecinos.

-difuminada: permite difuminar la imagen, se puede también utilizar la barra de control de imagenes para modificar el kernel de la misma manera que en el filtro promedio, se utiliza la función blur de la libreria cv2 para esta opción.

-bordes: Para realizar la función bordes invocamos a la función Canny de cv2 para realizar los bordes de la imagen deseada.

-ejemplo de bordes: Se inserto una función de ejemplo para analizar mejor el uso de la opción canny, en la cual se aplica un filtro gaussiano, un filtro de canny y un contador de bordes para obtener el número de objetos de la figura.

-Filtro Sobel: Se aplica la función Sobel de cv2 para obtener este filtro. Se puede modificar el kernel mediante la barra de control de imagenes.

-Filtro Laplace: Se aplica la función Laplacian de cv2 para obtener este filtro. 

-Filtro Gaussiano: Se aplica la función GaussianBlur de cv2 para obtener este filtro. Se puede modificar el kernel mediante la barra de control de imagenes. 

-Filtro Mediana: se aplica la función medianBlur para obtener este filtro. Se puede modificar el kernel mediante la barra de control de imagenes. 

-Dilatada: permite dilatar una imagen mediante la función dilate. La barra de Contraste y N° de iteracciones permite controlar cuantas veces se ha de dilatar la imagen.

-Erosionada: permite erosionar una imagen mediante la función erode. La barra de Contraste y N° de iteracciones permite controlar cuantas veces se ha de erosionar la imagen.

-Cierre: Es una dilatación seguida de una erosión, para lo cual utilizamos la función cv2.MORPH_CLOSE que esta dentro de la función cv2.morphologyEx. Se puede controlar el nivel del kernel con la barra de control de imagenes.

-Apertura: Es una erosión seguida de una apertura, para lo cual utilizamos la función cv2.MORPH_OPEN que esta dentro de la función cv2.morphologyEx. Se puede controlar el nivel del kernel con la barra de control de imagenes.

-Esqueletizada: permite obtener el esqueleto de la imagen elegida, mediante 4 procesos dentro de un while: erosión, dilatación, sustracción, y por último la unión bitwise_or para obtener con esto la esqueletización y salir del bucle.

#MENU TRANS_GEOMETRICAS:

Cuenta con 3 opciones:

-Rotación: permite rotar una imagen un ángulo determinado mediante la función getRotateMatrix2D y luego con la función warpAffine. Este ángulo se puede elegir con la barra de control de imagenes.

-Traslación: permite trasladar una cantidad de pixeles la imagen original mediante la función np.float32 y luego con la función warpAffine, en este caso para elegir la posición final de traslación se tiene que modificar en el código el valor de "M".

-Transformación Afin: permite ver una imagen en perspectiva mediante la función getAffineTransform. Para hacer algun cambio en la perspectiva se tienen que modificar los puntos 1 y 2 en el código.

#MENU DOMINIO FRECUENCIAL:

-Transformada Wavelet: Permite obtener la imagen comprimida según la resolución y el nivel de escala que uno modifique en el código:

	n=nivel de resolución
	Jmin=escala


