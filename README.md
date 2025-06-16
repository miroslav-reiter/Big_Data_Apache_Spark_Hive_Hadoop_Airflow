# 🗄️ Online kurz Big Data (Veľké Dáta), Apache Spark, Hive, Apache Hadoop, Apache Airflow

> Praktické kurzy – RDD, DataFrame, SparkSQL a distribuované spracovanie dát

## 📘 Obsah kurzu
01. [**🔍 Úvod do veľkých dát a Apache Spark**](#uvod-spark)
02. [**🧱 Práca s RDD a DataFrame**](#rdd-dataframe)
03. [**🧠 Spark SQL a dopyty nad dátami**](#spark-sql)
04. [**⚙️ Nastavenie prostredia a Spark UI**](#nastavenie)
05. [**📊 Načítanie dát a transformácie**](#transformacie)
06. [**📚 Zdroje a odporúčania pre Apache Spark**](#zdroje)

---
<a name="uvod-spark"></a>
# 🔍 1. Úvod do veľkých dát a nástroje pre spracovanie veľkých dát (Apache Spark, Hive, Apache Hadoop, Apache Airflow)

- **Big Data** riešia spracovanie dát, ktoré sú príliš veľké, rýchle alebo rôznorodé pre klasické databázy.
- **Apache Spark** je výkonný engine na rýchle spracovanie.
- **Hive** umožňuje analytikom používať SQL nad dátami v HDFS.
- **Hadoop** poskytuje základnú infraštruktúru pre ukladanie a dávkové výpočty.
- **Airflow** je určený na plánovanie a orchestráciu dátových procesov.

## 📊 Čo sú veľké dáta – model 12V a na čo sú dobré?

**Big Data** označuje veľké objemy dát, ktoré sa vyznačujú vysokou **rýchlosťou**, **objemom**, **rôznorodosťou** a často aj **nízkou kvalitou**. Veľké dáta sa v súčasnosti nedefinujú už len cez základné 3 alebo 5 znakov, ale cez **12 dimenzií (12V)**, ktoré lepšie vystihujú komplexnosť ich spracovania, hodnoty a rizík.

| 🆔 **Vlastnosť** | 📌 **Popis**                                 | 💡 **Príklad**                                |
|------------------|----------------------------------------------|-----------------------------------------------|
| 📦 Volume         | Objem dát – terabajty až petabajty           | Transakčné dáta, záznamy zo senzorov          |
| ⚡ Velocity       | Rýchlosť generovania dát                     | Dátové toky z IoT zariadení, streamy videa    |
| 🧩 Variety        | Rôznorodosť dát – štruktúrované aj neštrukt. | CSV, JSON, obrázky, logy, XML                 |
| ✅ Veracity       | Vierohodnosť a kvalita dát                   | Chýbajúce hodnoty, nekonzistentné záznamy     |
| 💰 Value          | Hodnota, ktorú je možné z dát získať         | Analýzy zákazníkov, predikcie, odporúčania    |
| 🔁 Variability    | Zmena v štruktúre alebo rýchlosti                | Sezónne výkyvy v dátach, nárazové záťaže       |
| 🧠 Visualization   | Potreba zrozumiteľného znázornenia               | Grafy, dashboardy, heatmapy                    |
| 🕵️‍♂️ Validity      | Relevantnosť a konzistentnosť v čase            | Aktuálne vs. historické dáta, verzovanie       |
| 🧱 Volatility     | Trvácnosť a životnosť dát                        | Krátkodobé (cache) vs. dlhodobé ukladanie      |
| 🔐 Vulnerability  | Rizikovosť a citlivosť na bezpečnosť             | Osobné údaje, GDPR, anonymizácia               |
| 🔄 Variance       | Rozdiely v dátach pri rovnakých vstupoch         | Rôzne senzory dávajú iné hodnoty               |
| 🎯 Venue          | Miesto pôvodu, kontext a zdroj dát               | Mobilné zariadenia, cloud, edge, on-prem       |

### 🎯 Na čo sa Big Data používajú?

- Analýza správania zákazníkov (marketing, e-commerce)
- Detekcia podvodov (banky, poistenie)
- Predikcia dopytu a spotreby (výroba, logistika)
- Real-time monitoring (IoT, zdravotníctvo)
- Automatizované rozhodovanie (AI, ML)

## ⚙️ Čo je to Apache Spark a na čo je dobrý?

**Apache Spark** je distribuovaný engine pre spracovanie veľkých dát v pamäti (in-memory). Apache Spark je výkonný open-source engine na spracovanie veľkých dát v reálnom čase. Podporuje paralelné výpočty v pamäti a je široko používaný v oblasti dátovej analytiky, strojového učenia a streamovania. Je výkonný, škálovateľný a flexibilný nástroj pre spracovanie veľkých dát. Je distribuovaný pod **licenciou Apache 2.0**

### ✅ Na čo sa používa?
- Rýchle dávkové a interaktívne spracovanie
- Strojové učenie (MLlib)
- Práca s DataFrame a SQL
- Streamovanie dát v reálnom čase

## 🐝 Čo je to Apache Hive a na čo je dobrý?

**Apache Hive** je SQL-like vrstva nad veľkými dátami uloženými v HDFS alebo iných formátoch.

### ✅ Na čo sa používa?
- Dopytovanie nad dátami pomocou SQL
- Vytváranie tabuliek, ETL procesy
- Integrácia s Hadoopom a Spark SQL
- Reporting a analýzy nad štruktúrovanými dátami


## 🐘 Čo je to Apache Hadoop a na čo je dobrý?
**Apache Hadoop** je ekosystém pre distribuované ukladanie a spracovanie veľkých dát.

### ✅ Na čo sa používa?
- Ukladanie dát pomocou **HDFS** (Hadoop Distributed File System)
- Spracovanie pomocou **MapReduce**
- Využíva sa ako základná vrstva pre Spark, Hive, HBase
- Umožňuje horizontálne škálovanie (viac serverov)


## 🧭 Čo je to Apache Airflow a na čo je dobrý?

**Apache Airflow** je nástroj na plánovanie a riadenie dátových workflowov (DAG – Directed Acyclic Graphs).

### ✅ Na čo sa používa?
- Automatizácia ETL/ELT procesov
- Plánovanie Spark/Hive/Hadoop úloh
- Riadenie závislostí medzi úlohami
- Vizualizácia a monitoring workflowov


## 📊 Porovnávacia tabuľka: Apache nástroje pre Big Data

| Nástroj         | Hlavné využitie                       | Technológia               | Výhody                                 | Nevýhody                                 |
|------------------|----------------------------------------|----------------------------|----------------------------------------|------------------------------------------|
| **Apache Spark** | Rýchle výpočty, ML, stream, SQL       | In-memory distribúcia     | Výkon, univerzálnosť, škálovateľnosť  | Vyššie nároky na pamäť                   |
| **Apache Hive**  | SQL nad veľkými dátami (HDFS)         | SQL-like nad Hadoop       | Známa syntax, vhodné na reporty        | Pomalšie, nie real-time                  |
| **Apache Hadoop**| Ukladanie a dávkové spracovanie       | HDFS + MapReduce          | Robustné, osvedčené riešenie           | Staršie, pomalšie ako Spark              |
| **Apache Airflow**| Riadenie workflowov a plánovanie     | Python, DAG workflow      | Modularita, monitoring, REST API       | Vyššia krivka učenia, komplexné ladenie  |


## ⚙️ Prečo Apache Spark?

| 💡 Vlastnosť         | 🔥 Apache Spark                                      |
|----------------------|-----------------------------------------------------|
| 💾 Spracovanie       | V pamäti (in-memory), rýchlejšie ako Hadoop         |
| 🧠 Programovací model| RDD, DataFrame, SQL, MLlib, GraphX                  |
| 🌐 Podpora jazykov   | Python, Scala, Java, R                              |
| 📈 Využitie          | Batch, stream, interaktívne, strojové učenie        |
| 📚 Ekosystém         | Bohatá dokumentácia, rozšírenia, kompatibilita     |


## 🏗️ Architektúra Apache Spark

- **Driver Program** – riadi vykonávanie a vytvára DAG
- **Cluster Manager** – prideľuje zdroje (napr. YARN, Kubernetes)
- **Executors** – vykonávajú úlohy a spracúvajú dáta
- **Tasks** – jednotky paralelného výpočtu

🌀 **DAG (Directed Acyclic Graph)** – reprezentuje logiku výpočtu ako necyklický graf závislostí.


## 🧱 Moduly Apache Spark

| Modul            | Popis                                             |
|------------------|---------------------------------------------------|
| `Spark Core`     | Základné API, správa pamäte a plánovanie výpočtu |
| `Spark SQL`      | Dopytovanie cez SQL a DataFrame API              |
| `Spark MLlib`    | Nástroje pre strojové učenie                     |
| `Spark Streaming`| Streamové (real-time) spracovanie                |
| `GraphX`         | Grafové výpočty a analýzy                        |


## 📦 Podporované formáty a zdroje dát

- **Formáty**: CSV, JSON, Parquet, Avro, ORC
- **Zdroje**: HDFS, S3, JDBC, Kafka, lokálne súbory, NoSQL databázy


## 🧠 Príklady využitia

| 🏢 Odvetvie        | 📈 Prípad použitia                              |
|--------------------|--------------------------------------------------|
| FinTech             | Detekcia podvodov v reálnom čase                |
| E-commerce          | Odporúčacie systémy, personalizácia ponúk       |
| Zdravotníctvo       | Predikcia diagnóz na základe historických dát   |
| Výroba / IoT        | Prediktívna údržba, sledovanie výkonu strojov   |
| Marketing           | Segmentácia zákazníkov, analýza správania       |


## ✅ Zhrnutie

- Apache Spark je ideálny nástroj pre prácu s veľkými dátami v rôznych formátoch.
- Ponúka vysoký výkon, škálovateľnosť a bohatý ekosystém nástrojov.
- Je vhodný pre dávkové aj real-time aplikácie v mnohých oblastiach.

---

<a name="rdd-dataframe"></a>
# 🧱 2. Práca s RDD a DataFrame v Apache Spark

Apache Spark umožňuje dve hlavné abstrakcie pre prácu s dátami: **RDD (Resilient Distributed Dataset)** a **DataFrame**. V tejto kapitole si vysvetlíme rozdiely, výhody a praktické príklady použitia oboch.


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

## 📄 Transformácie a akcie na RDD

| Typ operácie   | Príklad           | Popis                                       |
|----------------|-------------------|---------------------------------------------|
| Transformácia  | `map()`, `filter()`| Vytvára nový RDD                            |
| Akcia          | `collect()`, `count()` | Spustí výpočet a vráti výsledok do drivera  |


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


## 🔁 Porovnanie RDD vs. DataFrame

| Vlastnosť             | RDD                                 | DataFrame                         |
|------------------------|--------------------------------------|------------------------------------|
| API štýl              | Funkcionálny (map, reduce)           | Deklaratívny (SQL-like)            |
| Optimalizácia         | Bez optimalizácie                    | Catalyst + Tungsten optimizácia    |
| Výkon                 | Pomalší                              | Rýchlejší                          |
| Čitateľnosť           | Nižšia (viac kódu)                   | Vyššia (kompaktnejší kód)          |
| Prístup k schéme      | Nie                                  | Áno                                |


## 🔃 Prechod z RDD na DataFrame a späť

```python
# RDD → DataFrame
from pyspark.sql import Row
rdd = spark.sparkContext.parallelize([Row(meno="Eva", vek=29)])
df = spark.createDataFrame(rdd)

# DataFrame → RDD
rdd2 = df.rdd
```


## 🧪 Ukážka práce s CSV súborom ako DataFrame

```python
df_csv = spark.read.csv("data/osoby.csv", header=True, inferSchema=True)
df_csv.printSchema()
df_csv.select("meno", "vek").show()
```

## ✅ Zhrnutie

- **RDD** poskytuje nízkoúrovňovú kontrolu nad dátami, vhodné na zložité transformácie.
- **DataFrame** poskytuje vyšší výkon, čitateľnosť a podporu SQL.
- V moderných aplikáciách sa odporúča používať **DataFrame API**, ak nie je potrebné niečo špecifické z RDD.

---

<a name="spark-sql"></a>
# 🧠 3. Spark SQL a dopyty nad dátami

Spark SQL je modul Apache Spark, ktorý umožňuje spracovanie štruktúrovaných dát pomocou SQL syntaxe alebo DataFrame API. Kombinuje výkonnosť Spark enginu s jednoduchosťou SQL.


## 📋 Čo je Spark SQL?

Spark SQL umožňuje:

- vykonávať SQL dopyty priamo nad veľkými dátami,
- manipulovať so štruktúrovanými dátami pomocou DataFrame API,
- pracovať s rôznymi zdrojmi dát ako CSV, Parquet, Hive, JDBC.


## 🔧 Vytvorenie DataFrame tabuľky
### 🧪 Príklad: Načítanie CSV a registrácia ako tabuľka

```python
df = spark.read.option("header", "true").csv("data/objednavky.csv")
df.createOrReplaceTempView("objednavky")
```

Po registrácii môžete nad `objednavky` spúšťať SQL dopyty.


## 🧪 Príklady SQL dopytov

```python
# Výber všetkých stĺpcov
spark.sql("SELECT * FROM objednavky").show()

# Filtrovanie podľa hodnoty
spark.sql("SELECT * FROM objednavky WHERE cena > 100").show()

# Skupinové výpočty
spark.sql("SELECT produkt, COUNT(*) AS pocet FROM objednavky GROUP BY produkt").show()
```

## 📊 Porovnanie: SQL vs. DataFrame API

| Operácia                     | SQL syntax                                                    | DataFrame API                                 |
|------------------------------|----------------------------------------------------------------|-----------------------------------------------|
| Výber                        | `SELECT meno FROM zakaznici`                                  | `df.select("meno")`                           |
| Filtrovanie                  | `SELECT * FROM objednavky WHERE cena > 100`                   | `df.filter(df.cena > 100)`                    |
| Agregácia                    | `SELECT AVG(cena) FROM objednavky`                            | `df.agg({"cena": "avg"})`                     |
| Zoskupenie                   | `SELECT produkt, COUNT(*) FROM objednavky GROUP BY produkt`   | `df.groupBy("produkt").count()`              |
| Triedenie                    | `SELECT * FROM objednavky ORDER BY datum DESC`                | `df.orderBy("datum", ascending=False)`        |

## 🗃️ Práca so štruktúrovanými formátmi

### CSV

```python
df = spark.read.option("header", True).csv("data/objednavky.csv")
```

### JSON

```python
df_json = spark.read.json("data/produkty.json")
```

### Parquet

```python
df_parquet = spark.read.parquet("data/transakcie.parquet")
```


## 🧠 Optimalizácia Spark SQL

- **Catalyst Optimizer** – analyzuje a optimalizuje logický plán dopytu.
- **Tungsten Execution Engine** – nízkoúrovňová optimalizácia výpočtov.
- **Predicate Pushdown** – filtruje dáta už pri ich načítavaní.

➡️ Tieto mechanizmy výrazne zvyšujú výkon pri spracovaní veľkých dát.


## 🧪 Pokročilé SQL: JOIN, funkcie, CASE

```sql
-- Join dvoch tabuliek
SELECT o.id, o.produkt, z.meno
FROM objednavky o
JOIN zakaznici z ON o.zakaznik_id = z.id

-- Prípadová logika
SELECT meno,
       CASE WHEN vek >= 18 THEN 'Dospelý' ELSE 'Dieťa' END AS typ
FROM osoby
```

## ✅ Zhrnutie

- Spark SQL umožňuje prístup k dátam pomocou známej SQL syntaxe.
- Podporuje integráciu s rôznymi dátovými formátmi (CSV, JSON, Parquet).
- Výkon zabezpečuje Catalyst a Tungsten optimalizácia.
- SQL dopyty sú často kombinované s DataFrame API v praxi.

---

<a name="#nastavenie"></a>
# ⚙️ 4. Nastavenie prostredia a Spark UI
Táto kapitola sa venuje praktickému nastaveniu Apache Spark v lokálnom aj distribuovanom režime. Ukážeme si tiež, ako funguje Spark UI – webové rozhranie pre sledovanie a ladenie výpočtov.


## 💻 Požiadavky a príprava prostredia

### ✅ Softvérové požiadavky

| Komponent        | Odporúčaná verzia        |
|------------------|--------------------------|
| Apache Spark     | 3.5+                     |
| Java (JDK)       | 17 alebo 21              |
| Python           | 3.10+                     |
| PySpark          | najnovšia (`pip install`)|
| IDE              | Jetbrains Datalore, Jupyter Notebook, Microsoft Visual Studio Code|

### ✅ Inštalácia PySpark

```bash
pip install pyspark
```


## 🗂️ Premenné prostredia

Pri spúšťaní Spark aplikácií je potrebné nastaviť Java prostredie:

```bash
export JAVA_HOME="/path/to/java"
```

Na Windows:

```cmd
set JAVA_HOME=C:\Program Files\Java\jdk-17
```


## 🚀 Spustenie SparkSession v Pythone

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder     .appName("MojaSparkAplikacia")     .getOrCreate()
```

### 🧪 Overenie konfigurácie

```python
print(spark.version)
print(spark.sparkContext.appName)
```


## 🌐 Spark UI – Webové rozhranie

Po spustení aplikácie je dostupné na:

```
http://localhost:4040
```

### 📊 Čo Spark UI zobrazuje?

| Sekcia        | Popis                                           |
|---------------|--------------------------------------------------|
| Jobs          | Prehľad všetkých spustených úloh                 |
| Stages        | Detaily o jednotlivých výpočtových fázach        |
| Storage       | Informácie o RDD a DataFrame v pamäti            |
| Environment   | Nastavenia SparkSession a premenné               |
| Executors     | Zoznam executorov a využitie zdrojov             |
| SQL           | SQL dopyty a ich optimalizované plány            |


## 🧪 Príklad: Spark UI pri spracovaní CSV

```python
df = spark.read.option("header", "true").csv("data/objednavky.csv")
df.groupBy("produkt").count().show()
```

➡️ Počas vykonania vyššie uvedeného dopytu sa automaticky zobrazí job v Spark UI (4040).


## 🧰 Užitočné nastavenia SparkSession

```python
spark = SparkSession.builder     .appName("Aplikacia")     .config("spark.executor.memory", "2g")     .config("spark.sql.shuffle.partitions", "8")     .getOrCreate()
```

| Parameter                        | Popis                                           |
|----------------------------------|--------------------------------------------------|
| `spark.executor.memory`         | Veľkosť pamäte pre každý executor               |
| `spark.sql.shuffle.partitions`  | Počet partícií pri agregáciách a joinoch       |
| `spark.driver.memory`           | Pamäť pre driver proces                         |
| `spark.master`                  | Typ spustenia (napr. `local[*]`, `yarn`, `k8s`) |


## ✅ Zhrnutie

- Spark je možné spustiť lokálne aj na clustri.
- PySpark beží v Jupyteri alebo ako samostatný skript.
- Spark UI poskytuje cenné informácie o výpočtoch a výkone.
- Parametre SparkSession ovplyvňujú výkon a pamäťové požiadavky.

---
a name="transformacie"></a>

# 📊 5. Načítanie dát a transformácie v Apache Spark

Apache Spark umožňuje efektívne načítanie veľkého množstva dát z rôznych zdrojov a ich spracovanie pomocou transformácií. V tejto kapitole sa zameriame na praktické príklady práce so súbormi a najčastejšie transformácie nad DataFrame.


## 📂 Podporované dátové formáty

| Formát   | Funkcia                                 | Príklad                                      |
|----------|------------------------------------------|----------------------------------------------|
| CSV      | `spark.read.csv()`                      | `spark.read.option("header", True).csv(...)` |
| JSON     | `spark.read.json()`                     | `spark.read.json("data/produkty.json")`      |
| Parquet  | `spark.read.parquet()`                  | `spark.read.parquet("data/data.parquet")`    |
| ORC      | `spark.read.orc()`                      | `spark.read.orc("data/data.orc")`            |
| JDBC     | `spark.read.jdbc()`                     | Načítanie z relačnej databázy                |


## 📥 Príklad: Načítanie CSV súboru

```python
df = spark.read.option("header", True).option("inferSchema", True).csv("data/objednavky.csv")
df.printSchema()
df.show(5)
```

## 🔄 Transformácie DataFrame

Spark transformácie sú **lenivé** – nevykonávajú sa ihneď, ale až pri akcii (`show()`, `collect()`, atď.).

### ✅ Bežné transformácie

| Operácia         | Popis                                 | Syntax                                      |
|------------------|----------------------------------------|---------------------------------------------|
| `select()`       | Výber stĺpcov                         | `df.select("produkt", "cena")`              |
| `filter()`       | Filtrovanie riadkov                   | `df.filter(df["cena"] > 100)`               |
| `withColumn()`   | Pridanie nového stĺpca                | `df.withColumn("DPH", df["cena"] * 0.23)`     |
| `drop()`         | Odstránenie stĺpca                    | `df.drop("nepotrebny_stlpec")`              |
| `distinct()`     | Odstránenie duplicitných riadkov      | `df.distinct()`                             |
| `groupBy()`      | Skupinové operácie                    | `df.groupBy("kategoria").count()`           |
| `orderBy()`      | Zoradenie                             | `df.orderBy("cena", ascending=False)`       |


## 🧪 Príklad: Vytvorenie nového stĺpca s DPH

```python
df = df.withColumn("cena_s_DPH", df["cena"] * 1.23)
df.select("produkt", "cena", "cena_s_DPH").show(5)
```


## 🧪 Príklad: Agregácia podľa kategórie

```python
df.groupBy("kategoria").agg({"cena": "avg", "id": "count"}).show()
```


## 🧪 Príklad: Filtrovanie a triedenie

```python
df.filter(df["cena"] > 100).orderBy("cena", ascending=False).show(10)
```


## 📦 Ukladanie transformovaných dát

| Formát   | Ukladacia funkcia                        | Príklad                                      |
|----------|-------------------------------------------|----------------------------------------------|
| CSV      | `df.write.csv()`                         | `df.write.option("header", True).csv(...)`   |
| Parquet  | `df.write.parquet()`                     | `df.write.parquet("output/data")`            |
| JSON     | `df.write.json()`                        | `df.write.json("output/produkty.json")`      |


## ✅ Zhrnutie

- Spark umožňuje pracovať s rôznymi typmi dátových formátov.
- Transformácie sú deklaratívne a spúšťajú sa až pri akciách.
- DataFrame API poskytuje bohatú sadu funkcií na spracovanie dát.
- Dáta je možné exportovať späť vo formáte CSV, JSON, Parquet a ďalších.

---

<a name="zdroje"></a>
# 📚 6. Zdroje a odporúčania pre Apache Spark

V tejto záverečnej kapitole nájdete odporúčané knihy, dokumentáciu, online kurzy a nástroje, ktoré vám pomôžu rozšíriť znalosti o Apache Spark. Tiež uvedieme odporúčania pre prax.

## 📘 Odporúčané knihy

| Názov | Autor | Popis |
|-------|-------|-------|
| *Learning Spark (2nd Edition)* | Jules S. Damji et al. | Výborný úvod do Spark 3 so zameraním na DataFrame API a Structured Streaming |
| *High Performance Spark* | Holden Karau | Optimalizácia výpočtov, efektívne transformácie a výkon |
| *Spark in Action* | Jean-Georges Perrin | Praktické príklady a vysvetlenie základov pre začiatočníkov |
| *Streaming Systems* | Tyler Akidau | Teoretický základ pre spracovanie dátových tokov v reálnom čase |

## 🌐 Online dokumentácia a nástroje

| Zdroj | Odkaz |
|-------|-------|
| Oficiálna dokumentácia | [https://spark.apache.org/docs/latest/](https://spark.apache.org/docs/latest/) |
| API Referencia PySpark | [https://spark.apache.org/docs/latest/api/python/](https://spark.apache.org/docs/latest/api/python/) |
| Spark GitHub | [https://github.com/apache/spark](https://github.com/apache/spark) |
| Databricks Spark Guide | [https://docs.databricks.com/](https://docs.databricks.com/) |

## 🎓 Kurzy a interaktívne platformy

| Platforma | Kurz / Odkaz |
|-----------|--------------|
| VITA Academy | [https://www.vita.sk/](https://www.vita.sk/) – praktické kurzy v slovenčine |
| Datacamp  | Introduction to PySpark |
| Coursera  | Big Data Analysis with Scala and Spark |

## 🛠️ Vývojové prostredia

- **Jupyter Notebook / Lab** – ideálne pre rýchle experimentovanie s PySpark
- **VS Code** – podpora PySpark cez rozšírenia
- **JetBrains DataSpell** – profesionálne IDE na prácu s dátami
- **Databricks Community Edition** – bezplatná platforma pre Spark a ML

## ✅ Odporúčania pre prax

- 🧠 Preferujte **DataFrame API** pred RDD pre výkon a čitateľnosť
- 🔍 Využívajte **Spark UI** (localhost:4040) na ladenie výkonu
- 🛠 Naučte sa optimalizovať dotazy: `cache()`, `repartition()`, `persist()`
- 🗃 Používajte **formát Parquet** pre efektívne ukladanie dát
- 🧪 Testujte na malých vzorkách a nasadzujte na clustri
- 📊 Sledujte **plán vykonania** (explain) pre optimalizáciu dotazov
- 📦 Automatizujte pomocou **Airflow, Prefect alebo Luigi**
- 🧱 Segmentujte pipeline: ETL, transformácie, analytika, ML
- 🔄 Sledujte **verzie Spark a kompatibilitu knižníc**

