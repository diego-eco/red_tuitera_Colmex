# A Twitter Social Network Analysis of Colmex Economist

Este repositorio contiene el código y datos utilizados en el [análisis de la comunidad tuitera del Colmex (Click para ver el análisis completo)](https://diego-eco.github.io/files/redes_colmex.html). [Click aquí para ver un resumen en Twitter](https://twitter.com/diego_lopezt/status/1400140781072130050)

El código se divide en 3 Jupyter Notebooks:

- **1_datos_api_twitter** limpia la encuesta de [Google Forms](https://docs.google.com/forms/d/e/1FAIpQLSc-IxQDgLAiIE6_u2uE1rc72hFy4f30zEZbYxa4vv75VPuaJQ/viewform?usp=send_form) y genera el archivo b_colmex_limpio.csv con los datos de la encuesta limpios. Posteriormente implementa un `for{}` que descarga los datos para todos los usuarios desde la [API de Twitter](https://developer.twitter.com/en) (requiere bearer token de developer registrado). La base resultante se guarda en c_red_colmex_completa.csv.

- **2_análisis_descriptivo** toma las dos bases anteriores y genera las estadística descriptiva de la red interna Colmex, las figuras resultantes están en la carpeta *figures*.

- **3_red_dirgida 3_red_nodirgida** utiliza `networkx` y `graph-tool` para generar y analizar las redes dirigidas y no dirigidas de la comunidad Colmex. [graph-tool](https://graph-tool.skewed.de/) es una librería basada en C++ hecha para GNU/Linux|MacOS. Para utilizarla en Windows es necesario crear una imagen vía Docker. Un tutorial para hacer esto está [disponible aquí](https://diego-eco.github.io/files/instrucciones_graphtool.pdf).

