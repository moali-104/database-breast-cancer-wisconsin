# database-breast-cancer-wisconsin
<!DOCTYPE html>
<html>
<head>
<title>Breast Cancer Wisconsin (Diagnostic) Data Set Analysis</title>
</head>
<body>

<h1>Breast Cancer Wisconsin (Diagnostic) Data Set Analysis</h1>

<p>This project analyzes the Breast Cancer Wisconsin (Diagnostic) Data Set to classify tumors as malignant or benign based on various features. The analysis involves data loading, preprocessing, feature selection, and training different classification models.</p>

<h2>Dataset Information</h2>
<p>The dataset contains features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. The features describe characteristics of the cell nuclei present in the image.</p>

<h3>Classes:</h3>
<ul>
  <li>Malignant (denoted by 0)</li>
  <li>Benign (denoted by 1)</li>
</ul>

<h3>Features:</h3>
<ul>
  <li>radius_mean: Mean of distances from the center to points on the perimeter.</li>
  <li>texture_mean: Standard deviation of gray-scale values.</li>
  <li>perimeter_mean: Mean of perimeter values.</li>
  <li>area_mean: Mean of area values.</li>
  <li>smoothness_mean: Mean of local variation in radius lengths.</li>
  <li>compactness_mean: Mean of perimeter^2 / area - 1.0</li>
  <li>concavity_mean: Mean of severity of concave portions of the contour.</li>
  <li>concave points_mean: Mean for the number of concave portions of the contour.</li>
  <li>symmetry_mean: Mean of symmetry.</li>
  <li>fractal_dimension_mean: Mean of the "coastline approximation" - 1.</li>
  <li>radius_se: Standard error for radius.</li>
  <li>texture_se: Standard error for texture.</li>
  <li>perimeter_se: Standard error for perimeter.</li>
  <li>area_se: Standard error for area.</li>
  <li>smoothness_se: Standard error for smoothness.</li>
  <li>compactness_se: Standard error for compactness.</li>
  <li>concavity_se: Standard error for concavity.</li>
  <li>concave points_se: Standard error for concave points.</li>
  <li>symmetry_se: Standard error for symmetry.</li>
  <li>fractal_dimension_se: Standard error for fractal dimension.</li>
  <li>radius_worst: Worst or largest radius value.</li>
  <li>texture_worst: Worst texture value.</li>
  <li>perimeter_worst: Worst perimeter value.</li>
  <li>area_worst: Worst area value.</li>
  <li>smoothness_worst: Worst smoothness value.</li>
  <li>compactness_worst: Worst compactness value.</li>
  <li>concavity_worst: Worst concavity value.</li>
  <li>concave points_worst: Worst concave points value.</li>
  <li>symmetry_worst: Worst symmetry value.</li>
  <li>fractal_dimension_worst: Worst fractal dimension value.</li>
</ul>

<h2>Data Loading and Exploration</h2>
<p>The dataset was loaded from the UCI Machine Learning Repository and basic data exploration was performed, including displaying the head, info, and descriptive statistics of the dataset. It was confirmed that there are no duplicate rows in the dataset.</p>
<p>The 'Diagnosis' column was encoded using Label Encoding, where 'M' (Malignant) is mapped to 1 and 'B' (Benign) is mapped to 0. The distribution of the target classes was visualized using a countplot.</p>

<h2>Shuffling and Splitting</h2>
<p>The dataset was split into training, validation, and testing sets to prepare for model training and evaluation.</p>

<h2>Preprocessing</h2>
<p>The features were scaled using StandardScaler to standardize the data before training the models.</p>

<h2>Feature Selection</h2>
<p>The correlation matrix was used to identify the features most correlated with the target variable ('Diagnosis'). The top 2 features were selected for the analysis.</p>

<h2>Model Training and Evaluation</h2>
<p>Several classification models were trained and evaluated, including:</p>
<ul>
  <li>Support Vector Classifier (SVC) with linear, RBF, and polynomial kernels.</li>
  <li>Logistic Regression.</li>
</ul>
<p>The accuracy of each model on the test set was calculated and compared using a bar plot.</p>
<p>GridSearchCV was used to find the best parameters for the SVC model, which resulted in a better accuracy.</p>
<p>The training and prediction times for different scenarios with SVC models were also measured and visualized.</p>

</body>
</html>
