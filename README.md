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

-Estructura .bmp: Permite observar la estructura de una imagen con extensi�n .bmp por lo cual, la imagen que abramos tiene que tener dicha extensi�n. Se visualizar� su estructura en el terminal.

-rgb a grises: como su nombre lo indica permite convertir la imagen abierta a escala de grises.

-Contraste: Mediante la barra de contraste podemos indicar el nivel que queremos contrastar la imagen para luego hacer clic en la opci�n contraste con esto se lograr� como resultado la imagen original y la imagen contrastada al nivel que se halla colocado.

-Ecualizar: Mediante esta funci�n podemos aplicar una ecualizar a la imagen original gracias a la libreria equalizeHist de opencv.

-Brillo: Mediante la barra de control de imagenes podemos indicar  el nivel de brillo que se desea en la imagen para luego hacer clic en la opci�n brillo con esto se lograr� como resultado la imagen original y la imagen con el brillo al nivel que se halla colocado.
 
-Umbralizar: Utilizando la barra de control de imagenes podemos indicar el valor del umbral para generar la imagen en blanco y negro.

#MENU TRANS_LOCALES:

cuenta con 14 opciones:

-Suavisar: es un filtro simple que suaviza la imagen segun el tama�o del kernel y los coeficientes.

-Filtro Promedio: En este filtro a diferencia del suavizado se puede modificar el kernel mediante la barra de control de imagenes (procurar que sean valores impares, por ejemplo: 1, 3, 5, etc.) y de esa manera genera una suavizado mediante el promedio de los pixeles vecinos.

-difuminada: permite difuminar la imagen, se puede tambi�n utilizar la barra de control de imagenes para modificar el kernel de la misma manera que en el filtro promedio, se utiliza la funci�n blur de la libreria cv2 para esta opci�n.

-bordes: Para realizar la funci�n bordes invocamos a la funci�n Canny de cv2 para realizar los bordes de la imagen deseada.

-ejemplo de bordes: Se inserto una funci�n de ejemplo para analizar mejor el uso de la opci�n canny, en la cual se aplica un filtro gaussiano, un filtro de canny y un contador de bordes para obtener el n�mero de objetos de la figura.

-Filtro Sobel: Se aplica la funci�n Sobel de cv2 para obtener este filtro. Se puede modificar el kernel mediante la barra de control de imagenes.

-Filtro Laplace: Se aplica la funci�n Laplacian de cv2 para obtener este filtro. 

-Filtro Gaussiano: Se aplica la funci�n GaussianBlur de cv2 para obtener este filtro. Se puede modificar el kernel mediante la barra de control de imagenes. 

-Filtro Mediana: se aplica la funci�n medianBlur para obtener este filtro. Se puede modificar el kernel mediante la barra de control de imagenes. 

-Dilatada: permite dilatar una imagen mediante la funci�n dilate. La barra de Contraste y N� de iteracciones permite controlar cuantas veces se ha de dilatar la imagen.

-Erosionada: permite erosionar una imagen mediante la funci�n erode. La barra de Contraste y N� de iteracciones permite controlar cuantas veces se ha de erosionar la imagen.

-Cierre: Es una dilataci�n seguida de una erosi�n, para lo cual utilizamos la funci�n cv2.MORPH_CLOSE que esta dentro de la funci�n cv2.morphologyEx. Se puede controlar el nivel del kernel con la barra de control de imagenes.

-Apertura: Es una erosi�n seguida de una apertura, para lo cual utilizamos la funci�n cv2.MORPH_OPEN que esta dentro de la funci�n cv2.morphologyEx. Se puede controlar el nivel del kernel con la barra de control de imagenes.

-Esqueletizada: permite obtener el esqueleto de la imagen elegida, mediante 4 procesos dentro de un while: erosi�n, dilataci�n, sustracci�n, y por �ltimo la uni�n bitwise_or para obtener con esto la esqueletizaci�n y salir del bucle.

#MENU TRANS_GEOMETRICAS:

Cuenta con 3 opciones:

-Rotaci�n: permite rotar una imagen un �ngulo determinado mediante la funci�n getRotateMatrix2D y luego con la funci�n warpAffine. Este �ngulo se puede elegir con la barra de control de imagenes.

-Traslaci�n: permite trasladar una cantidad de pixeles la imagen original mediante la funci�n np.float32 y luego con la funci�n warpAffine, en este caso para elegir la posici�n final de traslaci�n se tiene que modificar en el c�digo el valor de "M".

-Transformaci�n Afin: permite ver una imagen en perspectiva mediante la funci�n getAffineTransform. Para hacer algun cambio en la perspectiva se tienen que modificar los puntos 1 y 2 en el c�digo.

#MENU DOMINIO FRECUENCIAL:

-Transformada Wavelet: Permite obtener la imagen comprimida seg�n la resoluci�n y el nivel de escala que uno modifique en el c�digo:

	n=nivel de resoluci�n
	Jmin=escala


