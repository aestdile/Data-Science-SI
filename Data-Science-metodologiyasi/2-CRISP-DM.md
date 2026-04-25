# 🔬 CRISP-DM Metodologiyasi — Data Science uchun To'liq Qo'llanma

<div align="center">

![CRISP-DM](https://img.shields.io/badge/Metodologiya-CRISP--DM-blue?style=for-the-badge)
![Data Science](https://img.shields.io/badge/Data-Science-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-green?style=for-the-badge)

> **CRISP-DM** *(Cross Industry Standard Process for Data Mining)* — Data Science loyihalarini boshqarishning eng keng tarqalgan sanoat standarti.

</div>

---

## 📌 Nima uchun CRISP-DM?

CRISP-DM quyidagi **10 ta savolga ketma-ketlikda** javob berishni maqsad qiladi:

### 🎯 Muammodan yondoshuvga
1. Aynan qaysi muammoga yechim qidirayapsiz?
2. Yechimga kelish uchun ma'lumotlardan qay yo'sinda foydalanish mumkin?

### 🗄️ Ma'lumotlar bilan ishlash
3. Yechimni topish uchun qanday ma'lumotlar kerak?
4. Ma'lumotlar qayerdan kelayapti (manbalar) va ularni qanday qilib olamiz?
5. Siz to'plagan ma'lumotlar hal qilmoqchi bo'lgan muammoga aloqasi bormi?
6. Ma'lumotlarni sizga kerakli ko'rinishga olib kelish uchun nimalarni bajarish kerak?

### 💡 Yechim topish
7. Ma'lumotlardan foydali xabar olish uchun qay ko'rinishda vizualizasiya qilish mumkin?
8. Yaratilgan model qo'yilgan muammoga yechim berayaptimi yoki kamchiliklarini bartaraf etish kerakmi?
9. Modelni amalda qo'llasa bo'ladimi?
10. Savolga javob berish uchun konstruktiv fikrlarni qabul qila olasizmi?

---

## 🔄 CRISP-DM Sikli

```
                    ┌─────────────────────────┐
                    │   Biznes (faoliyat)ni   │
                    │       o'rganish          │
                    └────────────┬────────────┘
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                   │
              ▼                  ▼                   │
   ┌──────────────────┐  ┌──────────────────┐       │
   │  Jarayonlarni    │→ │    Analitik       │       │
   │   tushunish      │  │   yondoshuv       │       │
   └──────────────────┘  └────────┬─────────┘       │
                                  │                  │
              ┌───────────────────▼──────────────┐   │
              │        MA'LUMOTLARNI O'RGANISH    │   │
              │  ┌─────────────────────────────┐ │   │
              │  │  Ma'lumotlarga qo'yilgan    │ │   │
              │  │         talablar            │ │   │
              │  └──────────────┬──────────────┘ │   │
              │                 │                 │   │
              │  ┌──────────────▼──────────────┐ │   │
              │  │    Ma'lumotlarni yig'ish     │ │   │
              │  └──────────────┬──────────────┘ │   │
              │                 │                 │   │
              │  ┌──────────────▼──────────────┐ │   │
              │  │   Ma'lumotlarni talqin       │ │   │
              │  │          qilish             │ │   │
              │  └──────────────┬──────────────┘ │   │
              └─────────────────┼────────────────┘   │
                                │                     │
                    ┌───────────▼───────────┐         │
                    │  Ma'lumotlarni        │         │
                    │    tayyorlash         │         │
                    └───────────┬───────────┘         │
                                │                     │
              ┌─────────────────▼─────────────────┐   │
              │             Modellash              │   │
              │  (ikki yo'nalishda ishlaydi ↔️)   │   │
              └─────────────────┬─────────────────┘   │
                                │                     │
                    ┌───────────▼───────────┐         │
                    │    Modelni baholash   │         │
                    └───────────┬───────────┘         │
                                │                     │
              ┌─────────────────▼─────────────────┐   │
              │              TAQDIMOT              │   │
              │  ┌─────────────────────────────┐  │   │
              │  │  Loyihani ishga tushurish   │  │   │
              │  └──────────────┬──────────────┘  │   │
              │                 │                  │   │
              │  ┌──────────────▼──────────────┐  │   │
              │  │  Fikr-mulohazalar tahlili   │──┼───┘
              │  └─────────────────────────────┘  │
              └────────────────────────────────────┘
```

---

## 📋 Bosqichlar Batafsil

### 1️⃣ Biznes (Faoliyat)ni O'rganish

| Kichik bosqich | Maqsad |
|----------------|--------|
| Jarayonlarni tushunish | Biznes kontekstini anglash |
| Analitik yondoshuv | Muammoni data science tiliga o'girish |

**Savol:** *"Bu loyiha biznesga qanday foyda keltiradi?"*

---

### 2️⃣ Ma'lumotlarni O'rganish

```
Ma'lumotlarga qo'yilgan talablar
           ↓
Ma'lumotlarni yig'ish
           ↓
Ma'lumotlarni talqin qilish (EDA)
```

**Asosiy vazifalar:**
- 📊 Manbalarni aniqlash
- 🔍 Exploratory Data Analysis (EDA) o'tkazish
- ⚠️ Muammoli joylarni topish (null, outlier, noise)

---

### 3️⃣ Ma'lumotlarni Tayyorlash

> Bu bosqich odatda loyiha vaqtining **60–70%** ini oladi!

```python
# Misol: Asosiy tayyorlash qadamlari
df.dropna()           # Bo'sh qiymatlarni olib tashlash
df.fillna(median)     # Yoki o'rtacha bilan to'ldirish
df.drop_duplicates()  # Takroriy qatorlarni o'chirish
StandardScaler()      # Normalizatsiya
```

**Nima qilinadi:**
- ✅ Tozalash (Cleaning)
- ✅ O'zgartirish (Transformation)
- ✅ Birlashtirish (Integration)
- ✅ Tanlash (Selection)

---

### 4️⃣ Modellash

```
Ma'lumotlarni tayyorlash  ←──────────────────────┐
           ↓                                       │
     Model tanlash                                 │
           ↓                                       │
     Model qurish                                  │
           ↓                                       │
     Model sinovdan o'tkazish ──────────────────────┘
           (natija yaxshi bo'lmasa, qayta)
```

**Mashhur algoritmlar:**

| Muammo turi | Algoritmlar |
|-------------|-------------|
| Klassifikatsiya | Logistic Regression, Random Forest, XGBoost |
| Regressiya | Linear Regression, SVR, Gradient Boosting |
| Klasterlash | K-Means, DBSCAN, Hierarchical |
| NLP | BERT, TF-IDF, Word2Vec |

---

### 5️⃣ Modelni Baholash

**Asosiy metrikalar:**

```
Klassifikatsiya uchun:
  ├── Accuracy
  ├── Precision & Recall
  ├── F1-Score
  └── ROC-AUC

Regressiya uchun:
  ├── MAE  (Mean Absolute Error)
  ├── MSE  (Mean Squared Error)
  └── R²   (R-Squared)
```

---

### 6️⃣ Taqdimot (Deployment)

```
Modelni baholash
       ↓
Loyihani ishga tushurish (Deploy)
       ↓
Fikr-mulohazalar tahlili
       ↓
Keyingi sikl boshlash 🔄
```

**Deploy usullari:**
- 🌐 REST API (Flask, FastAPI)
- ☁️ Cloud (AWS, GCP, Azure)
- 📦 Docker Container
- 🖥️ Dashboard (Streamlit, Gradio)

---

## ⚡ Qisqacha Xulosa

```
CRISP-DM = Biznes → Ma'lumot → Tayyorlash → Model → Baholash → Deploy → 🔄
```

| Bosqich | Vaqt ulushi (taxminan) |
|---------|------------------------|
| Biznesni tushunish | 10% |
| Ma'lumotlarni o'rganish | 15% |
| Ma'lumotlarni tayyorlash | 60% |
| Modellash | 10% |
| Baholash | 3% |
| Deploy | 2% |

---

## 🛠️ Foydali Resurslar

- 📖 [CRISP-DM Official Guide](https://www.the-modeling-agency.com/crisp-dm.pdf)
- 🐍 [Scikit-learn Documentation](https://scikit-learn.org)
- 📊 [Kaggle — Amaliy mashqlar](https://www.kaggle.com)
- 🎓 [Coursera — IBM Data Science](https://www.coursera.org/professional-certificates/ibm-data-science)

---

<div align="center">

**⭐ Foydali bo'lsa, repo'ga star bosing!**

*CRISP-DM — Data Science loyihalarining suyanchig'i*

</div>
