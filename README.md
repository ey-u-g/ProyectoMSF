[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=ey-u-g/ProyectoMSF)
# Proyecto: Sistema gastroinstestinal

## Información de los integrantes
De la torre Gómez Johana Jazmin \[22211751]; l22211751@tectijuana.edu.mx

Garcia Murillo Karla Valeria \[22212385]; l22212385@tectijuana.edu.mx

Lopez Lopez Santiago \[22212260]; l22212260@tectijuana.edu.mx

Urbina Gómez Eliza Yasunari \[22211768]; l22211768@tectijuana.edu.mx

Modelado de Sistemas Fisiológicos 

Ingenería Biomédica 

## Docente 

Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción del proyecto 
<div align="center">
Sistema gastrointestinal 
  
Sistema gastrointestinal - tránsito y actividad peristáltica 
</div>

El sistema gastrointestinal, y en particular el proceso de propulsión y vaciamiento del contenido gástrico, puede describirse mediante un modelo dinámico que represente cómo las contracciones peristálticas impulsan el quimo hacia el intestino delgado. Aunque en la fisiología real intervienen complejos mecanismos neuromusculares y hormonales, el comportamiento global del tránsito puede aproximarse mediante un modelo de segundo orden que capture las relaciones entre la generación de presión peristáltica, el movimiento del contenido, su almacenamiento temporal y la inercia con la que responde ante las ondas contráctiles.


Para establecer esta analogía, se consideran las siguientes correspondencias fisiológicas:

1. Generación activa de presión (fuente peristáltica):
  La musculatura lisa genera ondas periódicas de contracción que producen aumentos rítmicos de   presión. En el modelo eléctrico, este comportamiento se representa mediante una fuente de       presión dependiente del tiempo, cuya oscilación reproduce la dinámica del peristaltismo.

2. Resistencia al flujo del quimo:
  La fricción interna del contenido, la viscosidad y el tono de los esfínteres (como el píloro) dificultan el avance del quimo. Esto se modela mediante resistores (R).
  Un aumento en la resistencia equivale fisiológicamente a un esfínter más cerrado, a un segmento rígido o a un tránsito enlentecido.

3. Distensibilidad del tracto digestivo:
  Los segmentos gástricos e intestinales pueden expandirse y almacenar temporalmente volumen antes de ser movilizado por la siguiente onda peristáltica. Esta propiedad se representa mediante capacitancia (C).
  Un valor alto de C indica mayor elasticidad; uno bajo refleja rigidez o mala capacidad de acomodación.

4. Inercia del bolo alimenticio:
  El contenido no cambia su velocidad de forma instantánea debido a su masa e inercia. Este comportamiento se representa mediante inductancia (L).
  La inductancia captura la resistencia del quimo a acelerarse o desacelerarse en respuesta a una onda de presión.

5. Señal de entrada al sistema (actividad peristáltica): 
  En este modelo la señal de entrada es una función periódica de presión, correspondiente a las ondas peristálticas que avanzan a lo largo del tubo digestivo. En términos eléctricos, esta fuente oscilatoria obliga a las dos mallas RLC a responder dinámicamente con un patrón pulsátil y amortiguado.


## Caso: Trastorno de hipomotilidad gástrica

Los trastornos de hipomotilidad se caracterizan por una disminución de la fuerza, coordinación o frecuencia de las contracciones peristálticas. Cuando estas ondas se vuelven débiles o inefectivas, el estómago no genera la presión necesaria para impulsar el contenido hacia el intestino delgado. Esto produce un vaciamiento lento, acumulación prolongada del quimo y síntomas como saciedad temprana, distensión abdominal, náuseas y plenitud postprandial.
La causa de la hipomotilidad puede variar: disfunción neuromuscular primaria, daño del nervio vago, miopatías gastrointestinales, alteraciones metabólicas o el efecto de medicamentos que reducen el tono del músculo liso. Independientemente del origen, el resultado fisiológico es similar: menor generación de fuerza propulsora y una respuesta dinámica del sistema más lenta y debilitada, que modifica el patrón normal de tránsito y compromete la eficiencia del vaciamiento gástrico.

## Descripción del sistema 

El flujo del quimo sigue este recorrido fisiológico:

Onda peristáltica → segmento que se contrae → segmento que se distiende → esfínter o resistencia distal → movimiento del contenido

El circuito equivalente sigue la misma lógica:
1. La onda peristáltica se modela como una fuente de presión oscilatoria.
2. El segmento contraído incluye inductancia y resistencia (L₁, R₁).
3. El segmento distal posee capacitancia, inductancia y resistencia (C, L₂, R₂).
4. Ambos segmentos están acoplados mediante una resistencia (Rₐ), que representa la interacción entre regiones contiguas.
5. El flujo resultante sale hacia el siguiente segmento intestinal.

## Lista de archivos incluidos en el repositorio
1. Ensayo gráfico
2. Cuaderno computacional de MATLAB [.mlx]
3. Modelado de Simulink [.slx]
4. Imágenes de las simulaciones [.pdf y .png]
5. Imagen con los parámetros del controlador
6. Evidencia del análisis matemático: función de transferencia, error en estado estacionario y estabilidad en lazo abierto.
7. Diagrama fisiológico en BioRender

## Referencias
\[1] Guyton, A. C., & Hall, J. E. (2020). Textbook of Medical Physiology (14.ª ed.). Elsevier.
— Describe la generación de presión peristáltica, motilidad gástrica, función pilórica y distensibilidad del tracto digestivo.

\[2] Johnson, L. R. (Ed.). (2019). Gastrointestinal Physiology (9.ª ed.). Elsevier.
— Explica la actividad peristáltica, control neuromuscular y tránsito gastrointestinal.

\[3] Camilleri, M. (2021). Gastroparesis: Etiology, clinical manifestations, and diagnosis. New England Journal of Medicine, 384(2), 138–147.
— Revisa causas y fisiopatología de la hipomotilidad y vaciamiento gástrico lento.

\[4] P. A. Valle, Syllabus para Modelado de Sistemas Fisiológicos, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[5] M. C. Khoo, Physiological Control Systems Analysis Simulation, and Estimation, 2nd ed. Piscataway, New Jersey, USA: IEEE Press, 2018, Section 4, Page 93.

\[6] N. S. Nise, Control Systems Engineering, 8th ed. Hoboken, New Jersey, USA: John Wiley & Sons, 2020.
