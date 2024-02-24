# MolarSupport-DM
Precision and Accuracy of the distance measurement for Molar Support, our thesis study

About the distance measurement model:
- uses the Euclidean distance formula: distance = sqrt((x2 - x1)^2 + (y2 - y1)^2).
- uses two distinct colors as colors of interest
- takes all the points inside these two distinct regions and calculates the minimum distance between all the points (true distance)

Method:

1. Define the ground truths and store it in a list.
2. Takes the image paths for the segmented images.
3. Runs the distance calculator function and stores it in a list.
4. Run the distance calculator function n number of times to calculate the [precision](#what-is-precision) (refers to the closeness of two or more measurements to each other when repeated measurements are made under the same conditions), using standard deviation and store it in a list.
5. Calculate the [accuracy](#what-is-accuracy)
6. Display the metrics using pandas table.
    - Image name | Ground Truth Distance (mm) | Script Distance (mm) | Precision | Accuracy

# What is precision
- Precision refers to the closeness of two or more measurements to each other when repeated measurements are made under the same conditions.
- In the context of classification or detection tasks, precision measures the proportion of true positive predictions (correctly identified instances) among all positive predictions made by the model.
- Precision can be calculated using the formula: **precision = true positives / (true positives + false positives)**
- Precision focuses on the correctness of the positive predictions made by the model and is not affected by the number of negative predictions.

# What is accuracy
- Accuracy refers to the closeness of a measured value to a known or true value.
- In classification or detection tasks, accuracy measures the proportion of correctly classified instances (both positive and negative) out of the total number of instances.
- Accuracy can be calculated using the formula: **Accuracy = (True Positives + True Negatives) / Total Number of Instances**
- Accuracy considers both correct positive and negative predictions made by the model and provides an overall measure of performance.
