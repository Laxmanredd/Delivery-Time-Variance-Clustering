# 🚚 Delivery Time Variance Clustering

## 📌 Project Overview

This project focuses on analyzing delivery performance by grouping delivery records into clusters based on **delivery time patterns**. The main goal is to understand how deliveries behave in terms of average delivery time, time variability, and weekday vs. weekend differences.

The project simulates delivery data stored in **MySQL**, processes it using **Python**, and applies **Hierarchical Clustering** to identify similar delivery patterns. The complete workflow is implemented in a single **Google Colab notebook**.

---

## 🎯 Objectives

* Prepare and process delivery timestamp data
* Compute delivery time-based features
* Identify delivery behavior patterns using clustering
* Visualize clusters using a dendrogram
* Export final delivery-to-cluster mapping

---

## 🧰 Technologies Used

* **Python**
* **Google Colab**
* **pandas** – data manipulation
* **scipy** – hierarchical clustering
* **seaborn & matplotlib** – data visualization
* **MySQL (conceptual design)** – data source simulation

---

## 🗂️ Dataset Description

The dataset represents delivery logs with pickup and drop-off timestamps.

**Fields used:**

* `delivery_id` – Unique delivery identifier
* `pickup_time` – Timestamp when delivery started
* `dropoff_time` – Timestamp when delivery was completed

> Note: Due to Google Colab environment limitations, MySQL extraction is simulated by creating the same dataset directly in Python. The MySQL table schema is included for conceptual completeness.

---

## ⚙️ Feature Engineering

From the raw timestamps, the following features are created:

* **Delivery Time (minutes)** – Difference between pickup and drop-off
* **Average Delivery Time** – Mean delivery duration per delivery ID
* **Delivery Time Variance** – Variability in delivery duration
* **Weekend Indicator** – Whether the delivery occurred on a weekend

These features are normalized before clustering.

---

## 📊 Clustering Approach

* **Clustering Method:** Hierarchical Clustering
* **Linkage Method:** Ward’s method
* **Distance Metric:** Euclidean (after normalization)
* **Output:** Dendrogram and cluster labels

Hierarchical clustering was chosen because it provides clear visual insights into how delivery records group together based on time behavior.

---

## 📈 Visualizations

* Dendrogram showing hierarchical relationships between deliveries
* Cluster-wise summary statistics

---

## 📁 Project Files

* `Delivery_Time_Variance_Clustering.ipynb` – Complete implementation
* `delivery_cluster_mapping.csv` – Final output mapping each delivery to a cluster
* `README.md` – Project documentation

---

## ✅ Final Deliverables

* End-to-end clustering pipeline in Python
* Clear visualization of delivery clusters
* Exportable CSV file for further analysis

---

## 🧠 Key Learnings

* Practical feature engineering from time-based data
* Handling real-world constraints in cloud environments
* Applying hierarchical clustering for behavioral analysis
* Interpreting clusters for business insights

---

## 🚀 How to Run

1. Open the `.ipynb` file in **Google Colab**
2. Run all cells sequentially
3. Download the generated CSV file from the Colab environment

---

## 👤 Author

**Laxman Reddy**
B.Tech – Computer Science (Data Science)

---

## 📌 Future Enhancements

* Use real MySQL database via cloud connection
* Increase dataset size for stronger clustering
* Add cluster evaluation metrics
* Extend analysis with delivery agent or location data

---

⭐ If you found this project useful, feel free to star the repository!
