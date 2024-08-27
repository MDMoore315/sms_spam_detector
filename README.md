# sms_spam_detector

## Create the SMS Classification Function

The `sms_classification` function was created in the `gradio_sms_text_classification` file through:
- Setting the text message column as the features variable
- Setting the "label" column as the target variable
- Splitting the data into training and testing sets with a test size of 33%
- Building a pipeline to transform the test data to compare to the training data
- Fitting the model to the transformed training data and
- Returning a model

The SMSSpamCollection.csv file was loaded into a DataFrame and the `sms_classification` function is called with the result set to the `text_clf` variable

## Create the SMS Prediction Function

The `sms_prediction` function is used to predict the classification of a new SMS text by:
- Creating a variable to  hold the prediction of a new SMS text
- Using a conditional statement to determine if the message is "ham" or "spam"
  - If "ham" a message indicating it is not spam is displayed
  - If "spam" a message indicating it is spam is displayed

## Create the Gradio Interface Application

After creating an interface application that includes an labelled input of  for the user to fill and output textbox that will identify the result the SMS messages below were tested and their outputs identified

### Use the following text messages to test your application.
1. You are a lucky winner of $5000!
2. You won 2 free tickets to the Super Bowl.
3. You won 2 free tickets to the Super Bowl. Text us to claim your prize.
4. Thanks for registering. Text 4343 to receive free updates on medicare.

### Outputs
1. The text message: "You are a lucky winner of $5000!", is not spam.
2. The text message: "You won 2 free tickets to the Super Bowl.", is not spam.
3. The text message: "You won 2 free tickets to the Super Bowl. Text us to claim your prize.", is spam.
4. The text message: "Thanks for registering. Text 4343 to receive free updates on medicare.", is spam.
