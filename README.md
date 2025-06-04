
---

## 📊 Milestone 1: Business-Level Analysis

### 🔧 Objectives:
- Analyze Arizona businesses using Spark SQL.
- Derive performance metrics by category, city, and ZIP code.

### 🔍 Core Spark Transformations:
- `spark.read.json()`
- `groupBy("city").count()`
- `filter(col("stars") >= 4.0)`
- `join()` operations to link reviews and business metadata

### 📈 Key Findings:
- **Tucson** has the highest business density.
- Niche services like `'Axe Throwing'` and `'Jewelry Repair'` have perfect 5.0 ratings.
- ZIP Code **85719** yields the most positive review counts.

---

## 👤 Milestone 2: User-Level Analysis

### 🔧 Objectives:
- Investigate user activity, elite status, influence on ratings, and review patterns.

### 🔍 Core Spark Transformations:
- `select("user_id", "elite", "review_count", "compliment_*")`
- `withColumn("year", year("date"))`
- `filter(col("review_count") > 100)`
- Time-series grouping using `groupBy("year").count()`

### 📈 Key Findings:
- Users like **Fox** and **Victor** contributed 17k+ reviews.
- **Elite users consistently rated higher (avg. 5.0 stars)** than non-elite users.
- Tip analysis revealed **Michael** posted over **4,000 tips** alone.
- Users like **Jonathan** and **Manny** had high influence but diverged from business average ratings.

