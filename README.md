# Gombafelismerő és osztályozó rendszer
# Projekt leírása

Ez a projekt egy mélytanulás alapú képosztályozási feladat, amelynek célja:

Többosztályos osztályozás – 100 különböző gombafaj azonosítása képek alapján.

Bináris osztályozás – annak eldöntése, hogy a gomba mérgező vagy nem mérgező.

Az adathalmaz az ImageCLEF 2021 versenyből származik, amely különböző minőségű és felbontású gombaképeket tartalmaz taxonómiai metaadatokkal.

# Kihívások

A fajok közötti finom vizuális különbségek felismerése.

Mérgező és nem mérgező kategóriák közötti tévesztések csökkentése.

Google Colab korlátozott erőforrásaihoz való alkalmazkodás.

# Megvalósítás

A csapat három különböző modellt készített:

Saját CNN modell (baseline, nulláról felépítve).

ResNet50 alapú modell – előre betanított hálózat felhasználásával (100 faj osztályozása).

Bináris osztályozó modell – mérgező vs. nem mérgező gombák.

# Adatfeldolgozás

Top 100 faj kiválasztása a képek számossága alapján.

Képek szűrése és előfeldolgozása (128×128 méret, normalizálás, transzformációk).

CustomDataset osztály implementálása a képek és címkék kezelésére.

# Modell architektúra

Baseline CNN: 2 konvolúciós réteg + pooling + teljesen összekapcsolt réteg.

ResNet50: előre betanított modell, új osztályozó réteggel kiegészítve.

Bináris modell: egyszerűbb architektúra, két kimeneti osztállyal.

# Eredmények

Csökkentett adathalmazon (100 faj × 50 kép/faj): ~8% pontosság.

Teljes adathalmaz esetén becsült pontosság: 70–80% (multiclass), 65–75% (bináris).

Macro F1-score várhatóan 0.7–0.8 lehet további optimalizálással.

# Használat

A projekt Google Colab környezetre optimalizált.

Töltsd fel a tanító adatokat (ZIP + metaadat CSV).

Futtasd a notebookokat a következő sorrendben:

Adat előfeldolgozása (top100 kiválasztása, szűrés).

Modell betöltése és tanítása.

Eredmények kiértékelése.

# Csapattagok és hozzájárulás

Kiss Hunor – baseline modell, folyamatfelügyelet

Bologa Eduárd – pretrained modellek implementálása

Kozma Szabolcs András – pretrained modellek optimalizálása

Pünkösti Györk – modellek futtatása, eredmények validálása

Minden csapattag 25%-ban járult hozzá a projekthez.
