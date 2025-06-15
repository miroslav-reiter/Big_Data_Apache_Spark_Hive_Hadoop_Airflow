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


