# Tema:
# Anotación del genoma bacteriano de *Staphylococcus aureus* resistente a la meticilina 

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
![Figura_1](imagenes/fig 1.png)



Seguido, se cargó la secuencia a la plataforma como se observa en la figura 2 y se realizó la configuración de la herramienta Bakta, la cual consistió en ir a  "Opciones de entrada/salida": y dar clicc en  "La base de datos de bakta" y seleccionar, la más reciente "La base de datos de amrfinderplus". despues en la más reciente Archivo de parámetros "Seleccionar genoma en formato fasta": Archivo de contig En "Anotación opcional": "Mantener encabezado original del contig (--keep-contig-headers)": S ( ver figura 3).
!...
!...

Para configurar los output en la herramienta bakta, se dió clic en "Selección de los archivos de salida": "Selección de archivos de salida": Archivo de anotación en TSV Anotación y secuencia en GFF3 Secuencias de nucleótidos de características como FASTA Resumen como TXT Gráfico del resultado de la anotación como SVG. Como se observa en la figura 4.

Posteriormente, se realizó el analisis de la secuencia en archirvo fasta y se hizo un resumen de las anotaciones como TSV simples y legibles por humanos. Seguidamente, se realizó la anotación de la secuencia en GFF3 para describir genes y otras características de secuencias biológicas.

Bakta ofrece una cantidad considerable de datos, principalmente relacionados con CDS o  ARNy, sin embargo, es probable que algunas anotaciones estructurales importantes, como los plásmidos, no estén incluidas es por eso que se realizó la identificación de plásmidos en los contigs previamente realizados, para esto se utilizó al herramienta **PlasmidFinder** (figura 10).
Después, se utilizó el archivo plasmid.fasta que que contenía las secuencias que mejor coincidian del genoma utilizado y el archivo hit_in_genome.fasta ue contenía los genes plasmídicos que mejor coincidián de la base de datos. ( figura 15)

Se utilizó la herramienta IntegronFinder para detectar integrones y ISEScan para detectar los elementos IS ( secuencia de inserción) los cuales estan presentes en la anotación estructural adicional de la bacteria.
Para la visualización de la anotación se utilizó lasidendificadas por Bakta, las secuencias de plásmidos identificadas por PlasmidFinder, los integrones identificados por IntegronFinder y los elementos IS identificados por ISEscan. Se utilizó la herramienta JBrowse, la cual necesitó que los archivos anteriormente mencionados esten en formato GFF y para esto se formateó las salidas de las secuerncias de los integrones y plasmidos como se muestra en las figuras 24-30.


## RESULTADOS

En la herramienta bakta, como se observa en la figura 5, se obtuvieron 44 contigs como entrada con una duración del borrador del genoma de 2.911.349 pb, un poco más corto que los 2.914.567 pb esperados, además, se encontró 2.717 CDS, un poco más que los 2.704 CDS esperados y de proteínas pequeñas 5 SORF, también, se encontró otros componetes como: 

| Comonetes  | Bakta | Hikichi et al2019 |
| ------------- | ------------- |  ------------- |
| ARNt | 57 | 61 |
| ARNm de transferencia | 1 | 1 |
| ARNr | 9  | 5 |
| mcRNA | 95  | sin información |


En el analisis de la secuencia en archivo fasta se observó que exsistieron 2884 secuencias, en las cuales se encontraba ARNt, ARNm, ARNr, ncARN, CDS y SORF ( figura 6). Además, en el resumen obtenido en las anotaciones se encuentró Sequence Id, Type, Start, Stop, Strand, Locus Tag, Gene, Product, DbXrefs, las cuales contenian 2.916 líneas ( figura 7).

Se observó que existe 51k+ (número de líneas en el GFF), como se observa en la figura 8. 

En la figura 9 se visualiza la trama de anotación del genoma circular, en la cual el círculo inicial muestra el contenido de GC en cada ventana deslizante de todas las secuencias, donde el color verde indica valores por encima del promedio y el color rojo indica valores por debajo. En el segundo círculo se muestra la tendencia del contenido de GC en tonos naranja y azul. Además, Se han representado todas las características en dos anillos que muestran la hebra delantera y trasera de afuera hacia adentro, con las secuencias codificantes en gris (los demás colores son complicados de diferenciar).

Posterior al analisis en la herramienta PlasmidFinder se encontró 5 secuencias de plásmidos, los cuales estaban ubicados de la sigueinte manera: 3	están en contig00019, 1 en contig00002 y 1 en contig00024. 
Donde todas las secuencias de plásmidos correspondientes a los plásmidos de *Staphylococcus aureus* están todas en contig00019, lo que hace que este contig probablemente sea un plásmido. Además, tiene una longitud de 30.347 pb.
Así mismo, al comparar las secuencias asociadas con  *Staphylococcus aureus* en NCBI se encontró que CP000737, AP003139 (2 veces) corresponden a plásmidos de *Staphylococcus aureus*, AF503772 corresponde a un plásmido de *Enterococcus faecalis*, CP003584 corresponde a un plásmido de *Enterococcus faecium*.

 Los resultados provenientes de los archivos  plasmid.fasta y el archivo hit_in_genome.fasta se observan en las figuras 13 y 14 respectivamente.
 

Los integrones son componentes genéticos que posibilitan a las bacterias ajustarse y desarrollarse rápidamente mediante la captura y expresión de genes nuevos. Un integron típico consta de un gen que codifica una enzima específica de recombinación (intI), un sitio de recombinación cercano (attI) donde se pueden insertar segmentos de genes, y un controlador de transcripción (Pc) que regula la actividad genética en estos segmentos. Para identificar integrones, se recurre a herramientas como IntegronFinder (Néron et al., 2022). En la figura 16 se puede observar que no se encontró encontrado elementos integrones en ningún contig,x, esto podría deberse ya que el genoma es demasiado estable o a que la calidad del ensamblaje no es lo suficientemente buena y se eliminaron algunas partes útiles para la detección de integrones. 

En las figuras 17-21, se observó los resultados de la secuencia de inserción empleando la herramienta ISEScan, la cual permitió detectar los elementos de secuencia de inserción (IS), que es una breve secuencia de ADN que funciona como un elemento transponible básico. Estos IS son los más diminutos, pero también los más comunes de los elementos transponibles autónomos que se encuentran en los genomas bacterianos. Su código genético se limita únicamente a las proteínas relacionadas con la actividad de transposición, lo que los convierte en actores fundamentales en la estructura y la evolución de los genomas bacterianos.

Ademas, como se observa en la figura 22 y 23, la herramienta permitió obtener la secuencia de aminoácidos ORF, detectectando así 20 elementos de insersión (IS), los cuales se encontraron agrupados como se observa en la tabla 2. 

| Contig  | Numero de elemento IS |
| ------------- | ------------- |
| contig00001  | 2  |
| contig00002 | 1 |
| contig00003  | 2  |
| contig00004 | 1 |
| contig00005  | 1  |
| contig00006 | 1 |
| contig00009  | 3  |
| contig00010 | 1|
| contig00011 | 1  |
| contig00012 | 1 |
| contig00019  | 3  |
| contig00027 | 1|
| contig00032  | 1  |
| contig00037 | 1 |

Dectectandose también, las diferentes familias del IS ( tabla 3)
| familia IS  | elemento IS identificado |
| ------------- | ------------- |
| IS1182  |4 |
| IS21|7|
|IS3 |3 |
| IS6 | 5|
| ISL3 | 1  |

En la salida de JBrowse se loggró ver los genes, IS, plásmidos, etc. en los contigs, como se observa en la figura 32.

## CONCLUSIONES



## REFERENCIAS
+ Waterlow NR, Cooper BS, Robotham JV, Knight GM. Antimicrobial resistance prevalence in bloodstream infection in 29 European countries by age and sex: An observational study. PLoS Med. 2024 Mar 14;21(3):e1004301. doi: 10.1371/journal.pmed.1004301. PMID: 38484006; PMCID: PMC10939247
+ Gagliotti C, Högberg LD, Billström H, Eckmanns T, Giske CG, Heuer OE, et al. Infecciones del torrente sanguíneo por Staphylococcus aureus: tendencias divergentes de aislados resistentes y susceptibles a la meticilina, UE/EEE, 2005 a 2018. Eur Secur. 2021 18 de noviembre ; 26 ( 46 ): 2002094. doi: 10.2807/1560-7917.ES.2021.26.46.2002094
+ Grupo de Trabajo EPINE. Prevalencia de las infecciones nosocomiales en los hospitales españoles EPINE 1990-1994.
Barcelona: Vaqué Rafart J. (ed.), 1995.
