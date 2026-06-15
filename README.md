# EchoPersona

### Unveiling Listening Patterns through Multiple Minimum Support Association Mining

## Overview

EchoPersona is a data mining project that analyzes real-world music listening histories from the Last.fm dataset to discover hidden co-listening patterns, identify niche and popular artist relationships, and generate actionable listener personas.

Traditional Apriori algorithms often fail to capture meaningful patterns involving less popular artists because of a single global support threshold. This project addresses that limitation using the Multiple Minimum Support (MIS) framework and the MSApriori algorithm.

The discovered patterns can be applied to:

* Playlist generation
* Music recommendation systems
* Listener segmentation
* Discovery Mix personalization
* User persona creation

---

## Dataset

Source:

HetRec 2011 Last.fm Dataset

Files used:

* user_artists.dat
* artists.dat
* user_taggedartists.dat
* tags.dat

Dataset statistics:

* ~1,892 users
* ~17,632 artists
* Millions of listening interactions

---

## Project Workflow

### 1. Data Preprocessing

* Load listening history data
* Merge artist names
* Apply playcount threshold
* Construct user-level transactions
* Analyze transaction characteristics

### 2. MIS Design

* Calculate item supports
* Identify popularity distribution
* Assign item-specific MIS values
* Apply Support Difference Constraint (SDC / φ)

### 3. MSApriori Mining

* Generate frequent itemsets:

  * F1
  * F2
  * F3
* Compare candidate generation and pruning
* Evaluate impact of varying φ values

### 4. Association Rule Mining

Generate rules using:

* Minimum confidence = 60%

Metrics:

* Support
* Confidence
* Lift

### 5. Listener Personas

Behavior-driven listener segments are created using discovered association rules.

Example personas:

* The Indie Wanderer
* The Alternative Explorer
* The Classic Rock Loyalist

### 6. Discovery Mix Engine

Design a ranking strategy for selecting the top 50 recommendation rules suitable for deployment in a production recommendation system.

---

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* mlxtend
* Jupyter Notebook

---

## Key Metrics

### Frequent Pattern Mining

* Item Support
* MIS Thresholds
* Support Difference Constraint (φ)

### Rule Evaluation

* Support
* Confidence
* Lift

### Rule Ranking

Final rule score:

Score = 0.30 × Support + 0.35 × Confidence + 0.35 × Normalized Lift

---

Interpretation:

Users who frequently listen to Radiohead are more than twice as likely to also listen to Coldplay compared with the average listener.

---



FAST-NUCES

Spring 2026

Data Mining (DS-3002)
