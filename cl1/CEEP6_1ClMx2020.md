#### César Elimiano Escalona Prado
##### Tarea 6.1

`ssh -Y bioinfo1@genoma.med.uchile.cl`


##### Creé un Directorio

>mkdir Cescalona_2020
>>cd Cescalona_2020

### 1

###### #####################################R1############################################

###### Crudo

##### A) Conocer no de lecturas (unix)
`zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz | echo $((`wc -l`/4))`

###### Respuesta=16190

##### B) Previsualizar las primeras 40 líneas del mismo archivo fastq

`zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz | head -40 > Head40_S16_R1.fastq`

 `less Head40_S16_R1.fastq (para ver el arvhivo generado)`

##### C) Ubicar la lectura 3 e identificar la información disponible

`zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz  | sed -n '9,12p;13q' > lines3_S16_R1.fastq`

`less lines3_S16_R1.fastq`
##### Desgloce ID
###### [@M03564]Instrumento:
###### [2]RunId:
###### [000000000-D29D3]FlowCellId:
###### [1]CarrilFlowCell:
###### [1101]NoTituloFlowCellyCarril:
###### [16471]CordenadaClusterX:
###### [1371]CordenadaClusterY 
###### [1]MiembroPar:
###### [N]Filtroado (de otroa manera):
###### [0]CtrlBits(-)ON:
###### [CAGATCCA+TAGACCTA']Secuencia Indice
###### Identificador---->@M03564:2:000000000-D29D3:1:1101:16471:1371 1:N:0:CAGATCCA+TAGACCTA'
###### Secuencia-------->TCTATTCCTCGCAGATCTGCAAGGTGCGAGGGGGCGCCCCGGGACTTGTGGGGATTCAGCTGGCACGGCCTGGGCAGGGGTCTGCTTGGAGGTCGCGGTGAAGGCTGAGGAGTGGTTTGGGGTCCAGGTCTCGGGAGTGGTGGGGTTGGCTTAGGGCTCAGGATCAGAACTTCAGTGGAGGATGGCTCGGGGGTAGGGGTATAGTTGGGGTCTGGGTTGGGGTGCCAGGTCACGCTTGGGGTACCTGCCGG
###### sequenciaYid----->+
###### Calidad---------->BBBBBFFFFFBBGGGGGGGGGGHGGHHGGGGGGGGGGGGGGGGGGHHHGFGGGGGHHGHHHHHGGHGGGGGGHGHHGGGGGGHHHHHHGHHGGHGGGGCGFHHHHHHHHGHGHHG;EHGFGGFGHHHGFFGGGGGGGEGGFGGGGC=BFFEFFFFFFFABFFBBFFFBFFFFFFFFFFFFFDFFEFFFFFFFF-.EEF.;;FFF/FFFFF99BBBF/;;BFF.-ABFFFFFFFF?DFEFFF.AFFFFFFFF

###### traducción calidad (10 bases) 33 33 33 33 33 37 37 37 37 37

###### filtrado
##### A)
`zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz | echo $((`wc -l`/4))`
###### Respuesta=12955
##### B)
`zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz | head -40 > Head40filtrado_S16_R1.fastq`
`less Head40_S16_R1.fastq`
##### C)
`zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz  | sed -n '9,12p;13q' > 
lines3filtrado_S16_R1.fastq`

`less lines3filtrado_S16_R1.fastq`
##### Desgloce ID
###### [@M03564]Instrumento:
###### [2]RunId:
###### [000000000-D29D3]FlowCellId:
###### [1]CarrilFlowCell:
###### [1101]NoTituloFlowCellyCarril:
###### [14841]CordenadaClusterX:
###### [5591]CordenadaClusterY 
###### [1]MiembroPar:
###### [N]Filtroado(de otra manera):
###### [0]CtrlBits(-)ON:
###### [CAGATCCA+TAGACCTA']Secuencia Indice
###### Identificador---->@M03564:2:000000000-D29D3:1:1101:14841:5591 1:N:0:CAGATCCA+TAGACCTA
###### Secuencia-------->TAAAATGTGCCAAGAACTGTGCTACTCAAGCACCAGGTAATGAGTGATAAACCAAACCCATGCAAAAGGACCCCATATAGCACAGGTACATGCAGGCACCTTACCATGGAAGCCATTGTCCTCTGTCCAGGCATCTGGCTGCACAACCACAATTGGGTGGACACCCTGGATCCCCAGGAAGGAAAGAGCATTCAAAGTGTCAAAGTAGGACTACTGGAACTGTCACT
###### sequenciaYid-----> +
###### Calidad---------->CCCCCFFFFFFFGGGGGGGGGGHHHHHHHHHHHHHHGHHHHHGHDGHHHHHHHHHHHGGGHHHHGHHHGHHHGGGHHGHHHHHHHHFGHHHHHHHHGHHGHHHHHHHGHHHGHHHHHHHHHHHHHHHHHHHHHHHHHHHHGGHHHHGGGGHHHHHHHGGGHHHHGGHHHHHHHHGGGGHFHGFHHHHHHHHHHHHHGFGHHHHHHFGHHGHFFHHHHHHHGHHGHGG

###### traducción calidad (10 bases) 38 38 38 38 38 37 37 37 37 37



###### #####################################R2##############################################

###### Crudo
#### A)
`zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz | echo $((`wc -l`/4))`
####### Respuesta=16190
##### B)
`zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz | head -40 > Head40_S16_R2.fastq`
`less Head40_S16_R2.fastq`
##### C)
`zcat ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz  | sed -n '9,12p;13q' > lines3_S16_R2.fastq`

`less lines3_S16_R2.fastq`
##### Desgloce ID
###### [@M03564]Instrumento:
###### [2]RunId:
###### [000000000-D29D3]FlowCellId:
###### [1]CarrilFlowCell:
###### [1101]NoTituloFlowCellyCarril:
###### [16471]CordenadaClusterX:
###### [1371]CordenadaClusterY 
###### [2]MiembroPar:
###### [N]Filtroado(de otra manera):
###### [0]CtrlBits(-)ON:
###### [CAGATCCA+TAGACCTA']Secuencia Indice
###### Identificador---->@M03564:2:000000000-D29D3:1:1101:16471:1371 2:N:0:CAGATCCA+TAGACCTA
###### Secuencia-------->GTGCAGAGAGGATCCCAGGATAATCCGGCAGGTACCCCAAGCGTGACCTGGCACCCCAACCCAGACCCCAACTATAACCCTACCCCCGAGCCATCCTCCACTGAAGTTCTGATCCTGAGCCCTAAGCCAACCCCACCACTCCCGAGACCTGGACCCCAAACCACTCCTCAGCCTTCACCGCGACCTCCAAGCAGACCCCTGCCCAGGCCGCGCCAGCTGAATCCCCCCAAGTCCCGGGGCGCCCCCTCGCC
###### sequenciaYid----->+
###### Calidad---------->AAABBFFBFCCFGGGGGGGGGGHHHHFFGGGGHHGHHHGGHGGFAEGHHGHHHGGGGGGGGGGHGGHHGGGGHHHHHHHHGHHHGHGCEGGGBGHHFHHGHHHGGBFDGFGBFGHGHHEHHGFHHFGHBGEGGGGGGGHFGGH.>->DFFCFHHHGG?ACGFAECHEGHHFHHCFGFHGDD9DDF.B9/F0ABBBFFFFAAEFE/.:AA;---;.:A//;//:BB..9-9./;BF-@----;@>DF-A-99

###### traducción calidad (10 bases) 32 32 32 33 33 37 37 33 37 34
###### filtrado

##### A)
`zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz | echo $((`wc -l`/4))`
###### Respuesta=12955
##### B)
`zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz | head -40 > Head40filtrado_S16_R2.fastq`

`less Head40_S16_R2.fastq`

##### C)
`zcat ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz  | sed -n '9,12p;13q' > lines3filtrado_S16_R2.fastq`

`less Read3filtrado_S16_R2.fastq`
##### Desgloce ID
###### [@M03564]Instrumento:
###### [2]RunId:
###### [000000000-D29D3]FlowCellId:
###### [1]CarrilFlowCell:
###### [1101]NoTituloFlowCellyCarril:
###### [14841]CordenadaClusterX:
###### [5591]CordenadaClusterY 
###### [2]MiembroPar:
###### [N]Filtroado(de otra manera):
###### [0]CtrlBits(-)ON:
###### [CAGATCCA+TAGACCTA']Secuencia Indice

###### Identificador---->@M03564:2:000000000-D29D3:1:1101:14841:5591 2:N:0:CAGATCCA+TAGACCTA
###### Secuencia-------->AGTGACAGTTCCAGTAGTCCTACTTTGACACTTTGAATGCTCTTTCCTTCCTGGGGATCCAGGGTGTCCACCCAATTGTGGTTGTGCAGCCAGATGCCTGGACAGAGGACAATGGCTTCCATGGTAAGGTGCCTGCATGTACCTGTGCTATATGGGGTCCTTTTGCATGGGTTTGGTTTATCACTCATTACCTGGTGCTTGAGTAGCACAGTTCTTGGCACATTTTA
###### sequenciaYid----->+
###### Calidad---------->ABBBBFFFFFFFGGGGGGGGGGHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHGGGGGHHHHGHGGHHHHHGGHHHHHHGHGGGGHHHHHHHHHHHHHHHGHHGHHGHHHHHHHHHHHHHGHHHHHHGHGHHHHHHHHHHGHHHHHHHHHHGHHHGGGFHHHHHGHHGHHGFGGGEHHFHHHHHHHHGHHHHFHHGHHHHFGHFGG0GF/<DFH0GFF0GHFHHFC

###### traducción calidad (10 bases) 32 33 33 33 33 37 37 37 37 37
### 2) FastQC

###### Crudos
`fastqc ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R1.fastq.gz -o .`

`fastqc ../181004_curso_calidad_datos_NGS/fastq_raw/S16_R2.fastq.gz -o .`

###### filtrado
`fastqc ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R1_filter.fastq.gz -o .`

`fastqc ../181004_curso_calidad_datos_NGS/fastq_filter/S16_R2_filter.fastq.gz -o .`

`ls`

##### 3) En una nueva ventana de la terminal
`scp bioinfo1@genoma.med.uchile.cl:Cescalona_2020/*`


