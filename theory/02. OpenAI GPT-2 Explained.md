# OpenAI GPT-2: Understanding Language Generation through visualization

link: https://towardsdatascience.com/openai-gpt-2-understanding-language-generation-through-visualization-8252f683b2f8



Modelamiento del lenguaje: https://machinelearningmastery.com/statistical-language-modeling-and-neural-language-models/



- GPT 1 usaba modelamiento del lenguaje clásico, secuencial, adivinando la palabra que sigue
- BERT se entrena basandose en el ejericio de "completar la oracion", por lo que aprende de manera bidireccional. 

Sin embargo, GPT puede generar texto de manera superior a BERT, por su naturaleza secuencial. GPT2 explotó este potencial.

¿Cómo lo lograron?

- Simplemente escalando a 1.5 billones de parámetros.
- Esta version no fue liberada, pero si una de un tamaño de 117 M



## Visualizando GPT-2

código: https://github.com/jessevig/bertviz

![image-20200414163008376](/home/greg/.config/Typora/typora-user-images/image-20200414163008376.png)

GPT-2 usa 144 cabezas de atención (12x12) en la siguiente imagen se pueden visualizar todas:

![image-20200414163124733](/home/greg/.config/Typora/typora-user-images/image-20200414163124733.png)



Un patron interesante es el patron que siemrpe mira a la palabra anterior:

![image-20200414163157910](/home/greg/.config/Typora/typora-user-images/image-20200414163157910.png)



Otro es el patrón que solo mira la palabra inicial, es como un patron nulo:

![image-20200414163223749](/home/greg/.config/Typora/typora-user-images/image-20200414163223749.png)



# Conclusiones

## Libreria para usar transformers pre entrenados conTF2 t pyTorch

https://github.com/huggingface/transformers#installation



Existen modelos como BERT, que entienden texto, traducen, y responden preguntas, y otros especializados en generar texto, como GPT2, que solamente esta entrenado para predecir la siguiente palabra.

Cual sería el ideal para generar melodias? Quizas predecir solamente la siguiente nota es sesgado, y se podria ocupar algo como un "transformer auto encoder" para generar melodias.