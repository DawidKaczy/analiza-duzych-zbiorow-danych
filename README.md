# Analiza dużych zbiorów danych

Semestr zimowy 2026/2027

Materiały z laboratoriów: notebooki, skrypty i małe pliki przykładowe.

## Zawartość

- `lab_01` — wczytywanie i dzielenie dużych plików (pandas, multiprocessing, filesplit)
- `lab_02` — wprowadzenie do Daska
- `lab_03` — Dask bags, delayed i futures oraz lokalny klaster
- `lab_04` — Dask w Machine Learning (`dask-ml`, `joblib`, `xgboost.dask`)
- `lab_05` — wstęp do Apache Spark / PySpark (lokalnie lub Docker)
- `lab_06` — PySpark DataFrames (CSV, agregacje, Parquet)

## Środowiska

Każdy lab ma własny `requirements.txt`. Lab 05 używa **osobnego** venv (Python 3.11), bo PySpark 4 nie idzie dobrze z Pythonem 3.14.

### Laby 1–4 (Dask / pandas) — Python 3.14

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r lab_01/requirements.txt
pip install -r lab_02/requirements.txt
pip install -r lab_03/requirements.txt
pip install -r lab_04/requirements.txt
```

Możesz instalować tylko wybrane laby.

### Lab 5 (PySpark) — Python 3.11 + Java 17/21

```bash
py -3.11 -m venv .venv_spark
.\.venv_spark\Scripts\Activate.ps1
pip install -r lab_05/requirements.txt
```

Szczegóły uruchomienia (lokalnie / Docker): `lab_05/readme.md`.

Lab 6 korzysta z tego samego środowiska. Dodatkowo:

```bash
pip install numpy tqdm
```

Notatnik: `lab_06/02_pyspark_dataframes.ipynb`. Opis: `lab_06/readme.md`.

Duże pliki CSV i Parquet są w `.gitignore`. Zostają lokalnie i nie wchodzą do repozytorium.
