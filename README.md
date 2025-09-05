# Drug_Side_Effects_Analysis
Drug Data Analysis 

Project Overview  
This repository contains a comprehensive pipeline to assess data quality and analyze a drug dataset encompassing drug–condition relationships, side-effect patterns, ratings and reviews, safety profiles, network structure, clustering behavior, and visualizations.

---

Table of Contents  
1. Prerequisites  
2. Installation  
3. Data Quality Assessment  
4. Analysis Modules  
5. Outputs  
6. Key Insights  
7. Recommendations  
8. File Structure  
9. Contact

---

Prerequisites  
- Python 3.8+  
- pandas, NumPy, scikit-learn, NetworkX, Matplotlib or Seaborn  

---

Installation  
git clone https://github.com/yourorg/drug-data-analysis.git  
cd drug-data-analysis  
pip install -r requirements.txt  

---

Data Quality Assessment  
- Missing Values per Column:  
  - side_effects: 4.23%  
  - generic_name: 1.47%  
  - drug_classes: 2.80%  
  - brand_names: 41.39%  
  - rx_otc: 0.03%  
  - pregnancy_category: 7.81%  
  - alcohol: 53.02%  
  - related_drugs: 50.12%  
  - rating: 45.89%  
  - no_of_reviews: 45.89%  
- Sample Data Snapshot:  
  Includes drug_name, medical_condition, side_effects, generic_name, drug_classes, brand_names, activity, rx_otc, pregnancy_category, csa, alcohol, related_drugs, rating, no_of_reviews, drug_link, and medical_condition_url.

---

Analysis Modules  

1. Drug–Condition Relationships  
- Top 10 Conditions by Drug Options: Pain, Colds & Flu, Acne, Hypertension, Osteoarthritis, Hayfever, Eczema, AIDS/HIV, Diabetes (Type 2), Psoriasis  
- Drugs Treating Multiple Conditions: 15 drugs; triamcinolone treats 3 conditions  

2. Side-Effect Patterns  
- Most Common Side Effects:  
  - lips (2,273)  
  - tongue (2,129)  
  - hives (1,940)  
  - swelling of your face (1,713)  
  - vomiting (1,273)  
- Drug Classes Analyzed: 274  

3. Ratings & Reviews  
- Rating Statistics: mean 6.81, median 7.00, std 2.31, range 0–10  
- Top 10 Drug Classes by Average Rating: e.g., Antibiotics/antineoplastics, Amylin analogs, Estrogens  
- Top 10 Conditions by Average Rating: Swine Flu (8.65), Gout (8.53), Eczema (8.27), etc.  
- Review Statistics: total 119,053, mean 75.1, median 12.0  
- Most Reviewed Drugs: phentermine (2,934), bupropion/naltrexone (2,013), Contrave (1,939), escitalopram (1,471), etc.  

4. Safety Profile  
- Pregnancy Category Distribution: C 1,382; B 509; N 436; D 228; X 129; A 18  
- Controlled Substances Schedules: N 2,688; Schedule 2 101; 3 26; 4 71; 5 20; M 16; U 9  
- Alcohol Interaction: 1,377 drugs  
- Prescription Status: Rx 1,998; Rx/OTC 604; OTC 328  
- Safety Score: mean 2.60 (range –3 to 6)  

5. Network Analysis  
- Nodes & Edges: 2,959 nodes (2,912 drugs + 47 conditions), 2,928 edges  
- Top Central Drugs: triamcinolone, clindamycin, erythromycin, doxepin, ciclesonide, etc.  
- Network Density: 0.0007  

6. Clustering Analysis  
- Clusters (4):  
  - Cluster 0 (817 drugs): Acne, Upper respiratory combinations, rating 8.27, reviews 9.53  
  - Cluster 1 (800 drugs): Pain, Analgesic combinations, rating 8.23, reviews 14.95  
  - Cluster 2 (564 drugs): Colds & Flu, Upper respiratory combinations, rating 7.80, reviews 10.05  
  - Cluster 3 (750 drugs): Hypertension, Atypical antipsychotics, rating 5.30, reviews 145.38  

---

Outputs  
- Comprehensive Visualization: drug_analysis_comprehensive.png  
- Insights Report: drug_analysis_insights.txt  

---

Key Insights  
- Data completeness: 85.1%  
- Most treated condition: Pain (264 drugs)  
- Versatile drugs: 15  
- High-rated class: Antibiotics/antineoplastics (avg 10.0)  
- Pregnancy-safe (A/B): 527 of 2,702 (19.5%)  
- Rx vs OTC: 68.2% Rx, 20.6% Rx/OTC, 11.2% OTC  

---

Recommendations  
- Target underrepresented conditions for drug development  
- Explore drivers of top-class ratings  
- Improve safety of low-scoring drugs  
- Leverage multipurpose drugs for cost efficiency  
- Mitigate common side effects via formulation or alternatives  

---

File Structure  
data/  
  └ raw_dataset.csv  
notebooks/  
  ├ 01_data_quality.ipynb  
  ├ 02_relationships.ipynb  
  ├ 03_side_effects.ipynb  
  ├ 04_ratings_reviews.ipynb  
  ├ 05_safety_profile.ipynb  
  ├ 06_network_clustering.ipynb  
  └ 07_visualization.ipynb  
outputs/  
  ├ drug_analysis_comprehensive.png  
  └ drug_analysis_insights.txt  
requirements.txt  
README.md  

---
