# The Ilustrated GPT-2

link http://jalammar.github.io/illustrated-gpt2/

Una gran diferencia con BERT, es que ocupa el decoder del transformer, que es autoregresivo, mientras que BERT usa el encoder.

GPT-2 se entrena para que de como output un solo token a la vez

![image-20200414223647183](/home/greg/.config/Typora/typora-user-images/image-20200414223647183.png)

Si se le quiere preguntar algo, se le da la pregunta simplemente y el modelo ira respondiendo palabra por palabra.

![image-20200414224413468](/home/greg/.config/Typora/typora-user-images/image-20200414224413468.png)

## The Decoder-Only Block