# obituary-detector
Предобученная нейросеть FastText по классификации новостей: классифицирует некрологи погибших в украинской войне солдат

# Сборка
```sh
head -n -100 obituary-fasttext.txt > obituary-fasttext.train
tail -n 100 obituary-fasttext.txt > obituary-fasttext.valid
fasttext supervised -input obituary-fasttext.train -output obituary_model -epoch 25
fasttext test obituary_model.bin obituary-fasttext.valid
```
