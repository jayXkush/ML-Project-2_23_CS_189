# Data Card

### Dataset
Titanic passenger dataset (Kaggle).
Target: Survived (0 = No, 1 = Yes).

### Features
- Pclass: Passenger class
- Name: Used to extract Title
- Sex: Encoded (male/female)
- Age: Imputed + scaled
- SibSp, Parch: Used to create FamilySize
- Ticket: Not engineered further
- Fare: Log-transformed + scaled
- Cabin: Converted into CabinFlag
- Embarked: Mode-imputed, encoded
- Engineered: Title, FamilySize, IsAlone

### Known Biases
- Skewed by gender and social norms (women/children survival).
- First-class passengers more represented.
- Cabin missingness limits location insights.