# Plant-Pathogen-classification-using-domain-adaptive-Feature-Extraction
This project explores the use of domain-adaptive feature extraction for plant pathogen classification. The approach aims to leverage the knowledge learned from a large, general-purpose dataset (source domain) to improve performance on a smaller, specific dataset (target domain) related to plant pathogens.

Methodology:

Fine-tuning ResNet50: The pre-trained ResNet50 model, known for its strong image classification capabilities, is fine-tuned on the Plant Village dataset (source domain). This allows the model to adapt to visual features relevant to plant health.
Feature Extraction: The fine-tuned ResNet50 is used as a feature extractor. For each image in the plant pathogen dataset (target domain), the model generates a vector representation capturing key characteristics.
Small DNN Training: A small Deep Neural Network (DNN) is trained on the extracted features from the plant pathogen dataset. This DNN learns to classify the plant diseases based on the informative features provided by the fine-tuned ResNet50.
Results:

The small DNN trained with domain-adaptive features achieves competitive performance compared to the fine-tuned ResNet50 model directly applied to the plant pathogen dataset. Here's a comparison of the results:

Small DNN:
Training Loss: steadily decreases from 0.1877 to 0.0535 across epochs.
Training Accuracy: increases from 0.9367 to 0.9805, demonstrating effective learning.
Validation Accuracy: reaches 0.9303, indicating good generalization on unseen data.
Fine-tuned ResNet50 (Plant Pathogen):
Training Loss: shows a similar decreasing trend but with higher initial values compared to the small DNN.
Training Accuracy: follows a similar pattern to the small DNN but with slightly lower values.
Validation Accuracy: reaches a maximum of 0.9075, lower than the small DNN's validation accuracy.

Key Takeaways:

Domain-adaptive feature extraction using a fine-tuned ResNet50 proved to be an effective approach for plant pathogen classification.
The small DNN trained on the extracted features achieved comparable or even better performance than the fine-tuned ResNet50 model, demonstrating the efficiency of this method.
This approach offers advantages:
Reduced training time and computational resources required compared to directly training a complex model like ResNet50 on the smaller dataset.
Improved generalization to unseen data in the target domain (plant pathogen classification).

Future Work:

Explore the use of different pre-trained models as feature extractors to identify the most suitable architecture for this task.
Investigate techniques for further optimizing the feature extraction process and the small DNN architecture.
Test the performance of this approach on other plant disease classification datasets to assess its generalizability.
