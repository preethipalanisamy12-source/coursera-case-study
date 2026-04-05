# Data Integrity Audit: FitBit Fitness Tracker Data

## 1. Dataset Overview

**Source:** Fitbit Fitness Tracker Data (CC0: Public Domain)

**Provider:** Distributed via Mobius on Kaggle.

**Contents:** Personal fitness tracker data from 30 eligible Fitbit users who consented to the submission of personal tracker data.

**Data Points:** Includes minute-level output for physical activity, heart rate, steps and sleep monitoring.

## 2. ROCCC Assessment
To verify the data's integrity and credibility, I have evaluated the dataset using the **ROCCC** (Reliable, Original, Comprehensive, Current, Cited) framework.

*   **Reliable:** **Low/Medium.** While the data was collected from consenting users, the sample size is limited to only **30** participants. This small sample size may introduce bias and may not be representative of the entire population of women interested in wellness.

*   **Original:** **Low.** This is a **third-party dataset**. It was not collected directly by Bellabeat but was made available through a public Kaggle repository.

*   **Comprehensive:** **Medium.** The dataset provides detailed information on steps, heart rate, and sleep. However, it lacks critical demographic information—specifically **gender and age**—which is a significant gap for a company like Bellabeat that focuses on products for women.

*   **Current:** **Low.** The data was collected in **2016**. Given that health and technology trends evolve rapidly, this data may no longer accurately reflect current consumer habits or the capabilities of modern smart devices.

*   **Cited:** **High.** The data is clearly cited as a **Public Domain (CC0)** dataset available through Mobius.


## 3. Strategic Alignment & Bridging the Gaps

To ensure the final recommendations are actionable and align with Bellabeat’s mission as a **high-tech manufacturer of health-focused products for women** , I have identified several critical misalignments between the available third-party dataset and the core business task:

*   **Geographic Metadata vs. Global Scalability:** While Bellabeat’s objective is to become a **larger player in the global smart device market** , the Fitbit dataset lacks geographic identifiers. Since Bellabeat has already **opened offices around the world**, the absence of location data prevents the analysis of region-specific wellness trends necessary to tailor localized marketing strategies for international markets.

*   **Feature Disparity (Stress & Mindfulness):** The primary focus of this analysis is the **Leaf tracker**, which is designed to track **activity, sleep, and stress**. Because the Fitbit dataset provides no data on stress or mindfulness habits, the analysis cannot fully evaluate how consumers engage with one of the Leaf’s key value propositions.

*   **Reproductive Health Demographic Gap:** A central pillar of Bellabeat's brand is **empowering women** with knowledge about their **reproductive health** and menstrual cycles. The Fitbit dataset is "demographically silent" on these factors, creating a significant gap in understanding how reproductive health influences the daily habits and wellness trends of Bellabeat's target audience.

*   **Subscription & Retention Metrics:** Bellabeat aims to grow its **subscription-based membership**, which provides personalized guidance on nutrition and health. The provided dataset tracks raw activity output but lacks insight into **user motivation or engagement** with structured programs. To truly **"unlock new growth opportunities"**, the analysis must eventually consider data that connects physical activity to membership-driven wellness goals.

*   **Digital Marketing Integration:** Bellabeat focuses **extensively on digital marketing**, including Google Search, Instagram, and Facebook. While the dataset identifies *when* users are physically active, it does not track *digital consumption habits*. To provide high-level recommendations that **influence marketing strategy**, the analysis must bridge the gap between **peak user activity trends** and optimal timing for digital ad placement.

## 4. Privacy, Security, and Accessibility

*   **Privacy:** The data consists of "personal tracker data," but the sources indicate that users gave their consent for submission.

*   **Licensing:** The dataset is under a **CC0: Public Domain** license, allowing for open use and analysis for this business task.

*   **Security:** The data is stored in a secure local folder ("Coursera Case study") and will be managed using version control (Git) to maintain a transparent record of all changes.

## 5. Final Conclusion on Data Integrity

The Fitbit dataset provides a useful starting point to "gain insight into how consumers use non-Bellabeat smart devices". However, due to the identified limitations in sample size and demographic data, I will follow the CCO’s recommendation to **consider adding another dataset** to address these gaps and ensure the final marketing recommendations are both accurate and actionable for Bellabeat’s target audience.

------------------------------------------------------------------------------------------------------------------------

## 6. Supplementary Dataset: CDC NHANES 2011–2014 Physical Activity Monitor Data

### 6.1 Dataset Overview

**Source:** CDC National Health and Nutrition Examination Survey (NHANES) — Physical Activity Monitor (PAM) Component, 2011–2014 cycles.

**Provider:** Centers for Disease Control and Prevention (CDC), National Center for Health Statistics (NCHS).

**Contents:** Wrist-worn accelerometer data from a nationally representative sample of US adults, merged with a Demographics file containing gender, age, race/ethnicity, and BMI.

**Data Points:** Steps, activity intensity (sedentary, light, moderate-to-vigorous), and daily movement summaries at minute, hour, and day level.

**Download URL:** https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Examination&CycleBeginYear=2013

---

### 6.2 ROCCC Assessment

*   **Reliable:** **High.** Collected by the CDC using a standardized wrist-worn ActiGraph GT3X+ device across thousands of US adults — far more statistically representative than the primary Fitbit dataset.

*   **Original:** **High.** First-party, institutionally collected data via in-person CDC examinations. Not crowdsourced or community-uploaded.

*   **Comprehensive:** **High.** Directly mergeable with the NHANES Demographics file, which provides **gender, age, race/ethnicity, and BMI** — directly addressing the primary Fitbit dataset's demographic gap. Stress, mindfulness, and reproductive health data remain unavailable across all publicly accessible datasets.

*   **Current:** **Low/Medium.** Collected in **2011–2014**. NHANES discontinued the wearable PAM component after this cycle. However, population-level activity patterns (steps, sedentary behavior, sleep) are relatively stable over time, making the demographic stratification it enables still analytically valid for this capstone.

*   **Cited:** **High.** Published and maintained by the CDC/NCHS with full methodology documentation, codebooks, and quality control notes.

---

### 6.3 Role in This Analysis

This dataset is a **supplementary reference layer**, not a primary analysis dataset. It serves two purposes:

*   **Demographic contextualization:** Fitbit trends will be cross-referenced against NHANES female participants to verify whether patterns hold at population scale.
*   **Sample size credibility:** Findings from 30 anonymous Fitbit users are upgraded from anecdotal patterns to population-consistent observations.

---

### 6.4 Privacy, Security, and Accessibility

*   **Privacy:** Fully de-identified by the CDC prior to public release.
*   **Licensing:** Public domain. No licensing restrictions.
*   **Security:** Stored in the same local project folder as the primary dataset, tracked via Git.

---

## 7. Dataset Considered and Excluded: NIH All of Us Fitbit Cohort

**Why it was considered:** Contains Fitbit data from 59,000+ US adults (2015–2023) with full demographic variables — the most current and largest Fitbit-native dataset available.

**Why it was excluded:** Individual-level data requires formal researcher registration and institutional approval via the All of Us Researcher Workbench. Not accessible for a self-directed capstone project.

**Note:** All of Us represents the gold standard for this type of analysis. Its exclusion reflects access constraints, not data quality.

---

## 8. Final Dataset Decision

| Role | Dataset | Source | Access |
|---|---|---|---|
| Primary | FitBit Fitness Tracker Data | Kaggle / Mobius (CC0) | Open download |
| Supplementary | CDC NHANES 2011–2014 PAM | CDC / NCHS (Public Domain) | Open download |

The Fitbit dataset drives all trend analysis as directed by the case study brief. NHANES contextualizes findings against a demographically representative, gender-stratified population. Remaining gaps — stress, reproductive health, digital behavior, and recency — are honest limitations that define the boundaries of this analysis and inform recommendations for future data collection.