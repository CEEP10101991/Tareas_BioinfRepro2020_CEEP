#### César Elimiano Escalona Prado
##### Tarea 6.1

>ssh -Y bioinfo1@genoma.med.uchile.cl
##CL-MX2020

##### Cree un Directorio con su nombre. Ejemplo

>mkdir Cescalona_2020
>>cd Cescalona_2020

###########################R1################
### 1)
###### Crudo

##### A) Conocer no de lecturas (unix)
>zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz | echo $((`wc -l`/4))

###### Respuesta=16190

##### B) Previsualizar las primeras 40 líneas del mismo archivo fastq

>zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz | head -40 > Head40_S16_R1.fastq

 `less Head40_S16_R1.fastq (para ver el arvhivo generado)`

##### C) Ubicar la lectura 3 e identificar la información disponible

>zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz  | sed -n '9,12p;13q' > lines3_S16_R1.fastq

`less Read3_S16_R1.fastq`

###### filtrado
##### A)
>zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz | echo $((`wc -l`/4))
###### Respuesta=12955
##### B)
>zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz | head -40 > Head40filtrado_S16_R1.fastq
`less Head40_S16_R1.fastq`
##### C)
>zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz  | sed -n '9,12p;13q' > lines3filtrado_S16_R1.fastq
`less Read3filtrado_S16_R1.fastq`
#####################################R2##############################################
### 1)
###### Crudo
#### A)
>zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz | echo $((`wc -l`/4))
####### Respuesta=16190
##### B)
>zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz | head -40 > Head40_S16_R2.fastq
`less Head40_S16_R2.fastq`
##### C)
>zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz  | sed -n '9,12p;13q' > lines3_S16_R1.fastq
`less Read3_S16_R2.fastq`
###### filtrado

##### A)
>zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz | echo $((`wc -l`/4))
###### Respuesta=12955
##### B)
>zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz | head -40 > Head40filtrado_S16_R2.fastq

`less Head40_S16_R2.fastq`

##### C)
>zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz  | sed -n '9,12p;13q' > lines3filtrado_S16_R2.fastq
`less Read3filtrado_S16_R2.fastq`

### 2) FastQC

###### Crudos
>fastqc ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz -o .

>fastqc ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz -o .

###### filtrado
>fastqc ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz -o .

>fastqc ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz -o .

>ls

##### 3) En una nueva ventana de la terminal
>scp bioinfo1@genoma.med.uchile.cl:Cescalona_2020/*
