# 🗄️ Online kurz Big Data (Veľké Dáta), Apache Spark, Hive, Apache Hadoop, Apache Airflow

> Praktický kurz pre začiatočníkov – RDD, DataFrame, SparkSQL a distribuované spracovanie dát

---

## 📘 Obsah kurzu

01. [**🔍 Úvod do veľkých dát a Apache Spark**](#uvod-spark)
02. [**🧱 Práca s RDD a DataFrame**](#rdd-dataframe)
03. [**🧠 Spark SQL a dopyty nad dátami**](#spark-sql)
04. [**⚙️ Nastavenie prostredia a Spark UI**](#nastavenie)
05. [**📊 Načítanie dát a transformácie**](#transformacie)
06. [**📚 Zdroje a odporúčania pre Apache Spark**](#zdroje)

---

<a name="uvod-spark"></a>

# 🔍 1. Úvod do veľkých dát a Apache Spark

Apache Spark je výkonný open-source engine na spracovanie veľkých dát v reálnom čase. Podporuje paralelné výpočty v pamäti a je široko používaný v oblasti dátovej analytiky, strojového učenia a streamovania.

---

## 📊 Čo sú veľké dáta – model 5V

Veľké dáta sú charakterizované nasledujúcimi 5 vlastnosťami:

| 🆔 **Vlastnosť** | 📌 **Popis**                                 | 💡 **Príklad**                                |
|------------------|----------------------------------------------|-----------------------------------------------|
| 📦 Volume         | Objem dát – terabajty až petabajty           | Transakčné dáta, záznamy zo senzorov          |
| ⚡ Velocity       | Rýchlosť generovania dát                     | Dátové toky z IoT zariadení, streamy videa    |
| 🧩 Variety        | Rôznorodosť dát – štruktúrované aj neštrukt. | CSV, JSON, obrázky, logy, XML                 |
| ✅ Veracity       | Vierohodnosť a kvalita dát                   | Chýbajúce hodnoty, nekonzistentné záznamy     |
| 💰 Value          | Hodnota, ktorú je možné z dát získať         | Analýzy zákazníkov, predikcie, odporúčania    |

---

## ⚙️ Prečo Apache Spark?

| 💡 Vlastnosť         | 🔥 Apache Spark                                      |
|----------------------|-----------------------------------------------------|
| 💾 Spracovanie       | V pamäti (in-memory), rýchlejšie ako Hadoop         |
| 🧠 Programovací model| RDD, DataFrame, SQL, MLlib, GraphX                  |
| 🌐 Podpora jazykov   | Python, Scala, Java, R                              |
| 📈 Využitie          | Batch, stream, interaktívne, strojové učenie        |
| 📚 Ekosystém         | Bohatá dokumentácia, rozšírenia, kompatibilita     |

---

## 🏗️ Architektúra Apache Spark

- **Driver Program** – riadi vykonávanie a vytvára DAG
- **Cluster Manager** – prideľuje zdroje (napr. YARN, Kubernetes)
- **Executors** – vykonávajú úlohy a spracúvajú dáta
- **Tasks** – jednotky paralelného výpočtu

🌀 **DAG (Directed Acyclic Graph)** – reprezentuje logiku výpočtu ako necyklický graf závislostí.

---

## 🧱 Moduly Apache Spark

| Modul            | Popis                                             |
|------------------|---------------------------------------------------|
| `Spark Core`     | Základné API, správa pamäte a plánovanie výpočtu |
| `Spark SQL`      | Dopytovanie cez SQL a DataFrame API              |
| `Spark MLlib`    | Nástroje pre strojové učenie                     |
| `Spark Streaming`| Streamové (real-time) spracovanie                |
| `GraphX`         | Grafové výpočty a analýzy                        |

---

## 📦 Podporované formáty a zdroje dát

- **Formáty**: CSV, JSON, Parquet, Avro, ORC
- **Zdroje**: HDFS, S3, JDBC, Kafka, lokálne súbory, NoSQL databázy

---

## 🧠 Príklady využitia

| 🏢 Odvetvie        | 📈 Prípad použitia                              |
|--------------------|--------------------------------------------------|
| FinTech             | Detekcia podvodov v reálnom čase                |
| E-commerce          | Odporúčacie systémy, personalizácia ponúk       |
| Zdravotníctvo       | Predikcia diagnóz na základe historických dát   |
| Výroba / IoT        | Prediktívna údržba, sledovanie výkonu strojov   |
| Marketing           | Segmentácia zákazníkov, analýza správania       |

---

## ✅ Zhrnutie

- Apache Spark je ideálny nástroj pre prácu s veľkými dátami v rôznych formátoch.
- Ponúka vysoký výkon, škálovateľnosť a bohatý ekosystém nástrojov.
- Je vhodný pre dávkové aj real-time aplikácie v mnohých oblastiach.

---

<a name="rdd-dataframe"></a>
# 🧱 2. Práca s RDD a DataFrame v Apache Spark

Apache Spark umožňuje dve hlavné abstrakcie pre prácu s dátami: **RDD (Resilient Distributed Dataset)** a **DataFrame**. V tejto kapitole si vysvetlíme rozdiely, výhody a praktické príklady použitia oboch.

---

## 🧠 Čo je RDD?

**RDD (Resilient Distributed Dataset)** je nízkoúrovňová, nemenná kolekcia objektov, ktorá sa distribuuje medzi uzly v klastri.

### ⚙️ Vlastnosti RDD:

- Immutability – nemenné štruktúry
- Paralelné spracovanie
- Fault-tolerance – automatická replikácia a zotavenie
- Podpora funkcionálnych operácií ako `map()`, `filter()`, `reduce()`

### 🧪 Príklad: Základná práca s RDD

```python
rdd = spark.sparkContext.parallelize([1, 2, 3, 4, 5])
rdd_squared = rdd.map(lambda x: x * x)
print(rdd_squared.collect())  # Výstup: [1, 4, 9, 16, 25]
```

---

## 📄 Transformácie a akcie na RDD

| Typ operácie   | Príklad           | Popis                                       |
|----------------|-------------------|---------------------------------------------|
| Transformácia  | `map()`, `filter()`| Vytvára nový RDD                            |
| Akcia          | `collect()`, `count()` | Spustí výpočet a vráti výsledok do drivera  |

---

## 📘 Čo je DataFrame?

**DataFrame** je vyššia abstrakcia nad RDD s metadátami (schema), podobná Pandas alebo SQL tabuľke.

### 🧾 Výhody DataFrame:

- Optimalizácia pomocou Catalyst engine
- Výrazne rýchlejšie spracovanie ako RDD
- Možnosť používať SQL-like syntax
- Automatické spracovanie schémy

### 🧪 Príklad: Vytvorenie DataFrame

```python
from pyspark.sql import Row

df = spark.createDataFrame([Row(meno="Anna", vek=25), Row(meno="Ján", vek=32)])
df.show()
```

---

## 🔁 Bežné operácie s DataFrame

```python
df.filter(df.vek > 30).select("meno").show()
df.groupBy("vek").count().show()
```

| Operácia          | Syntax                                     | Popis                           |
|-------------------|--------------------------------------------|----------------------------------|
| Filtrovanie       | `df.filter(df.vek > 30)`                   | Výber podľa podmienky           |
| Výber stĺpcov     | `df.select("meno", "vek")`                 | Výber konkrétnych stĺpcov       |
| Agregácia         | `df.groupBy("vek").count()`                | Skupinové výpočty               |
| Triedenie         | `df.orderBy("vek", ascending=False)`       | Zoradenie podľa hodnoty         |

---

## 🔁 Porovnanie RDD vs. DataFrame

| Vlastnosť             | RDD                                 | DataFrame                         |
|------------------------|--------------------------------------|------------------------------------|
| API štýl              | Funkcionálny (map, reduce)           | Deklaratívny (SQL-like)            |
| Optimalizácia         | Bez optimalizácie                    | Catalyst + Tungsten optimizácia    |
| Výkon                 | Pomalší                              | Rýchlejší                          |
| Čitateľnosť           | Nižšia (viac kódu)                   | Vyššia (kompaktnejší kód)          |
| Prístup k schéme      | Nie                                  | Áno                                |

---

## 🔃 Prechod z RDD na DataFrame a späť

```python
# RDD → DataFrame
from pyspark.sql import Row
rdd = spark.sparkContext.parallelize([Row(meno="Eva", vek=29)])
df = spark.createDataFrame(rdd)

# DataFrame → RDD
rdd2 = df.rdd
```

---

## 🧪 Ukážka práce s CSV súborom ako DataFrame

```python
df_csv = spark.read.csv("data/osoby.csv", header=True, inferSchema=True)
df_csv.printSchema()
df_csv.select("meno", "vek").show()
```

---

## ✅ Zhrnutie

- **RDD** poskytuje nízkoúrovňovú kontrolu nad dátami, vhodné na zložité transformácie.
- **DataFrame** poskytuje vyšší výkon, čitateľnosť a podporu SQL.
- V moderných aplikáciách sa odporúča používať **DataFrame API**, ak nie je potrebné niečo špecifické z RDD.

---

