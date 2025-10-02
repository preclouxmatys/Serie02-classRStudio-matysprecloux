# README – IEAP Series 02 (RStudio)

## Project description

This project was conducted as part of **IEAP-2025 Series 02 RStudio**.  
The goal was to practice **correlation, regression, and hypothesis testing** using two datasets:  

1. **Clinical dataset** on upper limb non-use after stroke (PANU, SANU, EENU).  
2. **Lifestyle dataset** on snoring stereotypes (age, weight, height, alcohol, sex, snore, tabac).  

## Content of the notebook
### Part 1 – Clinical dataset: Upper limb non-use
1. Descriptive statistics for PANU, SANU, EENU.  
2. Correlation analysis (Spearman) → weak but significant correlation between PANU and SANU.  
3. Linear regressions → PANU as a function of SANU and EENU.  
4. Interpretation: PANU is more strongly linked to EENU (elbow extension) than SANU (shoulder anteposition).

### Part 2 – Statistical background
- Definitions of mean, median, variance, standard deviation, normal distribution.  
- Shapiro-Wilk tests to assess normality.  
- Discussion on parametric vs non-parametric tests.  

### Part 3 – Experimental dataset: Before/After performance
- Paired t-test (n = 8).  
- Significant improvement After vs Before (mean diff = 2.5, p ≈ 0.001).  
- Boxplots with paired lines illustrate the effect.  

### Part 4 – Snoring stereotypes

1. **Are snorers fatter?**  
   - Compared weight between snorers and non-snorers.  
   - Both normality tests rejected → Wilcoxon.  
   - Result: *No significant difference*.  

2. **Do snorers drink more?**  
   - Alcohol consumption compared between groups.  
   - Not normal → Wilcoxon.  
   - Result: *Snorers drink significantly more alcohol (p ≈ 0.009)*.  

3. **Do snorers smoke more?**  
   - Contingency table (Snore × Tabac).  
   - χ² and Fisher tests.  
   - Result: *No significant difference*.  

4. **Are men fatter?**  
   - Weight compared between sexes (t-test/Wilcoxon).  
   - Result: *Men tend to weigh more (depending on normality assumption)*.  

5. **Do women smoke less?**  
   - Contingency table (Sex × Tabac).  
   - χ²/Fisher.  
   - Result: *No significant association detected*.  

6. **General correlations**  
   - Explored age, weight, height, alcohol.  
   - Example: *weight ~ height* (positive correlation), *age ~ alcohol* (negative correlation).  
   
### Key results
- **Clinical dataset**: PANU correlates more strongly with EENU (elbow extension non-use) than with SANU.  
- **Before/After experiment**: Significant performance improvement after treatment (p ≈ 0.001).  
- **Snoring stereotypes**:  
  - Snorers drink significantly more alcohol (p ≈ 0.009).  
  - No significant difference for weight or smoking.  
  - No significant sex-related differences in smoking; men tend to weigh more.

### Limitations 

**- Missing values in the clinical dataset (especially SANU/EENU).**
**- Small sample sizes (n=8 for Before/After).**
**- χ² test sometimes limited by low counts → Fisher used.**
**- Correlations/regressions do not prove causality.**