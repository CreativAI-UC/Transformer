# Tensorflow Tutorial - Transformer model for language understanding



https://www.tensorflow.org/tutorials/text/transformer?hl=es

Ventajas del modelo:

- No hace supuestos sobre realciones temporales a traves de la data.
- Computo paralelo para las capas de output. En contraste con las RNN que se calculan secuencialmente.
- Los elementos distantes pueden afectarse sin necesidad de pasar por varis capas como en la CNN o la RNN. https://arxiv.org/pdf/1903.03878.pdf

Algunas cosas a tener en cuenta:

- ensFor a time-series, the output for a time-step is calculated from the *entire history* instead of only the inputs and current hidden-state. This *may* be less efficient.
- If the input *does* have a temporal/spatial relationship, like text, some positional encoding must be added or the model will effectively see a bag of words.

## Setup

```python
!pip install -q tf-nightly
import tensorflow_datasets as tfds
import tensorflow as tf

import time
import numpy as np
import matplotlib.pyplot as plt
```

## Dataset

```python
examples, metadata = tfds.load('ted_hrlr_translate/pt_to_en', with_info=True, as_supervised=True)

train_examples, val_examples = examples['train'], examples['validation']
```

```
...
```

## Positional Encoding

Este es un encoding que embedding en el que las palabras quedan cerca segun su cercania en significado y ademas por su cercanía en las oraciones. Por lo que palabras que se usan juntas en general quedaran muy cerca en el encoding. Más ingfo acá: https://github.com/tensorflow/examples/blob/master/community/en/position_encoding.ipynb

