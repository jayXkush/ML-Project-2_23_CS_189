# Decision Log

### Missing Values
- **Age**: Imputed using median (robust to skewness).
- **Embarked**: Imputed using mode (most common port).
- **Cabin**: 77% missing. Instead of dropping, created `CabinFlag` to indicate availability.

### Outliers
- **Fare**: Distribution highly skewed. Applied log transformation to reduce skewness.

### Feature Engineering
- Extracted `Title` from passenger names (e.g., Mr, Mrs, Miss) to capture social status.
- Created `FamilySize = SibSp + Parch + 1` to model family influence.
- Derived `IsAlone` as binary variable (1 if passenger had no family, else 0).

### Encoding
- Applied one-hot encoding to categorical variables: `Sex`, `Embarked`, `Title`.

### Scaling
- Applied log-transform on `Fare` and considered MinMax/Standard scaling for Age and Fare during model building.

### Feature Selection
- Plan to compare correlation-based selection with model-based importance (e.g., Random Forest feature importance).
