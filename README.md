# river-semantic-segmentation-tf

## Informacje ogólne

Repozytorium zawiera program pozwalający na trening modelów opartych na konwolucyjnych sieciach neuronowych służacych do segmentacji obszarów rzecznych na zdjęciach satelitarnych skomponowanych z pasm widzialnych RGB.

## Rezultaty


lp. | Model | Accuracy | IoU 
--- | --- | --- | ---
1 | Wejście | - | -
2 | Wzorowe wyjście | 1.0 | 1.0 
3 | VGG_UNET | 0.987783 | 0.872502
4 | RESNET50_UNET | 0.986252 | 0.858671
5 | VGG_SEGNET | 0.984189 | 0.83578 
6 | RESNET50_SEGNET | 0.982243 | 0.818463 
7 | UNET | 0.980608 | 0.801781 
8 | SEGNET | 0.977276 | 0.775857 

Numeracja wierszy w wyższej tabeli odpowiada oznaczeniom na wizualizacji rezultatów dla przykładowego zdjęcia:
![results.png](https://i.postimg.cc/y890Vgkn/results.png)


## Użyte narzędzia
- TensorFlow - framework ML
- OpenCV - biblioteka do przetwarzania obrazów
- NumPy - biblioteka do operacji na macierzach
- neptune - narzędzie logujące

## Dataset

Dataset do pobrania z oddzielnego repozytorium: https://github.com/shocik/sentinel-river-segmentation-dataset

## Uruchomienie
Uruchomienie kodu na własnym komputerze wymaga wykonania następujących kroków przygotowujących:

1. Wprowadzenie danych neptune w pliku [config.cfg](config.cfg).
2. Modyfikacja ścieżki do folderu roboczego w pliku [train_predict.ipynb](train_predict.ipynb):
	```python
	#set workdir
	os.chdir("/content/drive/MyDrive/RiverSemanticSegmentation/")
	```
3. Modyfikacja ścieżki do zbioru danych w pliku [train_predict.ipynb](train_predict.ipynb):
	```python
	#dataset configuration
	dataset_dir = os.path.normpath("/content/drive/MyDrive/SemanticSegmentationV2/dataset/")
	```
