Achieved a high accuracy of 99.5%, primarily due to its tendency to predict '0' or no rain & 76% for little bit rain.
This project focuses on a Convoluted LSTM approach for weather prediction based on satelite images along with weather station data.

- **Feature Engineering**: Cloud patterns like horizontal and vertical scales were fed into the model just like other Temp, Dew point.

- **Trail - RNN and CNN Integration**: Experimented with a combined RNN and CNN model. The RNN processed time-series data sequences, while the CNN handled individual images per timestamp.

- **Incorporating Class Weights**: Added class weights in training to penalize the model more for incorrect predictions, especially for underrepresented classes. This helped in addressing the class of imbalanced data but didn't completely resolve it.

- **Oversampling Minority Class**: Attempted oversampling the minority class to provide more data for the model. However, the limited representation of these classes limited the effectiveness of this approach.

- **Hybrid LSTM and ConvLSTM Model**: The final breakthrough was developing a hybrid model combining LSTM (for time-series data) and ConvLSTM (for image data). This model processes sequences of images over time, providing a comprehensive understanding of spatio-temporal data, especially in imbalanced datasets.

- **Feature Correlation Reduction**: Tested the removal of highly correlated features to streamline the dataset. Despite some improvements in data clarity, the hybrid LSTM and ConvLSTM model remained superior, effectively leveraging the comprehensive data, including correlated features.
