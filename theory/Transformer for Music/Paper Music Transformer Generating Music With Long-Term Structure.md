# Paper: Music Transformer: Generating Music With Long-Term Structure

12 de Dic, 2018

paper https://arxiv.org/pdf/1809.04281.pdf

demos https://storage.googleapis.com/music-transformer/index.html

## Formato de los datos

### JSB Chorales

Al igual que en coconet (counterpoint by convolution), se usa el formato definido en este link: https://github.com/czhuang/JSB-Chorales-dataset

![image-20200414175521642](/home/greg/.config/Typora/typora-user-images/image-20200414175521642.png)

Si una nota esta callada, la entrada en la matriz es NaN.

El formato no distingue entre notas mantenidas y repetidas. Pero creo que es no debiese ser mayor problema.

En este paper, la grilla se serializa como S1A1T1B1S2A2T2B2...

### Piano-E-Competition

Acá la resolucion del tiempo esta en el orden de milisegundos, por lo que discretizar el tiempo implicaria usar secuencias muy repetitivas de la misma nota seguida

![image-20200414212053401](/home/greg/.config/Typora/typora-user-images/image-20200414212053401.png)

![image-20200414212117043](/home/greg/.config/Typora/typora-user-images/image-20200414212117043.png)

extraido de Oore et al  https://arxiv.org/pdf/1808.03715.pdf