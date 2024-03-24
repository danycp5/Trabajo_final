# Tema:
# Anotación del genoma bacteriano de *Staphylococcus aureus* resistentes a la meticilina 

**Autores:** 
+ Adriana Aguirre
+ Daniela Calderón
+ Patricia Dávalos

**Fecha:**  febrero de 2024

## PROBLEMA

*Staphylococcus aureus* es la especie patógena más prominente dentro de su género y es responsable de muchas infecciones, tanto adquiridas en la comunidad como en entornos hospitalarios. El enfoque actual en el estudio de este microorganismo se debe a su alta incidencia y a su capacidad de causar brotes de infecciones nosocomiales, especialmente cuando se trata de cepas resistentes a la meticilina. 

## ANTECEDENTES
La resistencia a los antibioticos representa una prioridad en la salud pública a nivel mundial. Entender su impacto frente a los importantes cambios demográficos que están ocurriendo globalmente es una área de conocimiento esencial que requiere ser abordada. Según estimaciones de la Organización Mundial de la Salud, se prevé que para el año 2050 una de cada cinco personas en el mundo tendrá 60 años o más. Es sabido que la incidencia de infecciones bacterianas aumenta con la edad y varía según el género. El incremento de las infecciones en grupos etarios avanzados resulta en una mayor exposición a los antibióticos y un mayor contacto con ambientes médicos, los cuales son reconocidos como puntos críticos de transmisión de bacterias resistentes. Sin embargo, no se observa un aumento simple de la resistencia en todos los patógenos según la edad. Comprender cómo estas interacciones impulsan la dinámica de las infecciones resistentes a los medicamentos es crucial para entender la mejor manera de abordar la resistencia a antibioticos (walterlow NR, et al., 2024).

El empleo de antibióticos, la exposición a ambientes sanitarios con alta incidencia de transmisión y las modificaciones en la actividad del sistema inmunitario difieren en función de la edad y el género del individuo. A pesar de ello, la mayoría de los estudios sobre la resistencia a los antimicrobianos no toman en cuenta los factores demográficos y únicamente ofrecen datos sobre la prevalencia de la resistencia a nivel nacional (Gagliotti C, et al., 2018).


Las cepas resistentes a la meticilina (SARM) fueron identificadas casi inmediatamente después de la introducción de la meticilina en el tratamiento médico. Los primeros casos de brotes de infección nosocomial se registraron en hospitales europeos a principios de la década de 1960. Desde entonces, la prevalencia de estas cepas ha ido en aumento en la mayoría de las regiones del mundo. En nuestro país, los estudios sobre los aislados de SARM muestran un aumento significativo, pasando de un 1,5% en 1986 a un rango del 18 al 23% en 1996. Este incremento ha llevado a que ciertas áreas hospitalarias, especialmente aquellas consideradas de alto riesgo como las Unidades de Cuidados Intensivos, se conviertan en zonas endémicas para este tipo de infección. Algunas investigaciones realizadas en ciertos periodos incluso han reportado cifras de hasta un 40%  (Grupo de Trabajo EPINE, 1995; Cercenado et
al.,1997).
La infección causada por *Staphylococcus aureus* es de gran importancia clínica y representa un desafío significativo para la salud pública. La presencia de *S. aureus* resistente a la meticilina dificulta el tratamiento de infecciones graves, lo que resulta en un aumento de la morbilidad, mortalidad y costos adicionales. Además, contribuye significativamente a la carga de resistencia a los antimicrobianos.

## OBJETIVOS
+ Evaluar la calidad de las secuecuencias de *Staphylococcus aureus* mediante la herramienta virtual Galaxy.
+ Elaborar el ensamblaje de la secuencia Empleando la herramienta virtual Bakta para modificar la secuencia de *Staphylococcus aureus*.
+ Interpretar los resultados obtenidos.
    
## FLUJO DE TRABAJO

[Pipeline](https://app.diagrams.net/#Hdanycp5%2FTrabajo_final%2Fpipeline%2FDiagrama%20sin%20t%C3%ADtulo.drawio#%7B%22pageId%22%3A%22lsY_AHojMyWDu4EsEvxC%22%7D)

## MÉTODOLOGÍA
Priemro se utilizó la base de datos NCBI para buscar la secuencia cruda de *Staphylococcus aureus*, después se realizó el analisis de calidad utilizando fastqc. 
Una vez analizada la calidad, se prosedió a utilizar la herramienta galaxy, en la cual se cambió el nombre a historial como se observa en la figura 1. 
!....

Seguido, se cargó la secuencia a la plataforma como se observa en la figura 2 y se realizó la configuración de la herramienta Bakta, la cual consistió en ir a  "Opciones de entrada/salida": y dar clicc en  "La base de datos de bakta" y seleccionar, la más reciente "La base de datos de amrfinderplus". despues en la más reciente Archivo de parámetros "Seleccionar genoma en formato fasta": Archivo de contig En "Anotación opcional": "Mantener encabezado original del contig (--keep-contig-headers)": S ( ver figura 3).
!...
!...

Para configurar los output en la herramienta bakta, se dió clic en "Selección de los archivos de salida": "Selección de archivos de salida": Archivo de anotación en TSV Anotación y secuencia en GFF3 Secuencias de nucleótidos de características como FASTA Resumen como TXT Gráfico del resultado de la anotación como SVG. Como se observa en la figura 4.

Posteriormente, se realizó el analisis de la secuencia en archirvo fasta y se hizo un resumen de las anotaciones como TSV simples y legibles por humanos. Seguidamente, se realizó la anotación de la secuencia en GFF3 para describir genes y otras características de secuencias biológicas.



## RESULTADOS

En la herramienta bakta, como se observa en la figura 5, se obtuvieron 44 contigs como entrada con una duración del borrador del genoma de 2.911.349 pb, un poco más corto que los 2.914.567 pb esperados, además, se encontró 2.717 CDS, un poco más que los 2.704 CDS esperados y de proteínas pequeñas 5 SORF, también, se encontró otros componetes como: 
![image](https://github.com/danycp5/Trabajo_final_Omicas_G2/assets/163198034/3babcc7c-bbf9-4ca9-b716-bea4322e3c21)

En el analisis de la secuencia en archivo fasta se observó que exsistieron 2884 secuencias, en las cuales se encontraba ARNt, ARNm, ARNr, ncARN, CDS y SORF ( figura 6). Además, en el resumen obtenido en las anotaciones se encuentró Sequence Id, Type, Start, Stop, Strand, Locus Tag, Gene, Product, DbXrefs, las cuales contenian 2.916 líneas ( figura 7).

Se observó que existe 51k+ (número de líneas en el GFF), como se observa en la figura 8






## CONCLUSIONES



## REFERENCIAS
+ Waterlow NR, Cooper BS, Robotham JV, Knight GM. Antimicrobial resistance prevalence in bloodstream infection in 29 European countries by age and sex: An observational study. PLoS Med. 2024 Mar 14;21(3):e1004301. doi: 10.1371/journal.pmed.1004301. PMID: 38484006; PMCID: PMC10939247
+ Gagliotti C, Högberg LD, Billström H, Eckmanns T, Giske CG, Heuer OE, et al. Infecciones del torrente sanguíneo por Staphylococcus aureus: tendencias divergentes de aislados resistentes y susceptibles a la meticilina, UE/EEE, 2005 a 2018. Eur Secur. 2021 18 de noviembre ; 26 ( 46 ): 2002094. doi: 10.2807/1560-7917.ES.2021.26.46.2002094
+ Grupo de Trabajo EPINE. Prevalencia de las infecciones nosocomiales en los hospitales españoles EPINE 1990-1994.
Barcelona: Vaqué Rafart J. (ed.), 1995.
