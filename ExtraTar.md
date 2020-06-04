my question surged from homework [6.1](https://github.com/u-genoma/BioinfinvRepro/blob/master/Unidad6/Tutorial_Control_de_calidad_de_lecturas_NGS.md), this exercise explicitly asked “How to count fastq reads ussing Unix commands?”

For answering this question I found the next [link](https://www.biostars.org/p/139006/) at Biostars

```
# When the file is saved as .fastq  

echo $(cat yourfile.fastq|wc -l)/4|bc

# When the file is saved as .gz  

 echo $(zcat yourfile.fastq.gz|wc -l)/4|bc
```
The lines above count the number of lines and divide them by 4.

As explained at the forum, each fastq read comprises of 4 lines,so if you count the total number of lines you'll get number of reads multiplied by 4, therefore yo only need to count the lines at the file and divide them by 4 for have the actual number of reads.
