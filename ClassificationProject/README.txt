YouTube Video Classification:
All data is from Kaggle( USvideos.csv, CAvideo.csv, UScategory.json, CAcategory.json)
'Get_duration_video.ipynb': using YouTubeAPIv3 to get all the duration of video
'GLOVE_data_processing.inydb': using GLoVE for word embedding, after that saving file into processed_data.cs
'SentenceBertDataProcessing,inydb': Using SBERT for word embedding and data cleaning using Panda, after that saving to 'data_with_embedding_csv.csv' and 'data_with_embedding_fix.pk'l
'SBERT_MBNN_training.inydb': training Multi Branches neural network using data_with_embedding_fix.pkl and save the model to file 'duration_neural_network.h5'
'xgboost_model_training.inydb': training xgboost model using 'data_with_embedding_fix.pkl' and save the model to file 'xgboost_model.pkl'
'US_test-with_XGBoost.inydb': testing xgboost model on USvideo to check accuracy
'Input_SBERT_MBNN.inydb': classify videos by plug in input as the URL of the video using MBNN model
'Input_SBERT_xgboost.inydb': classify videos by plug in input as the URL of the video using xgboost model

HOW TO USE MODEL TO CLASSIFY VIDEO:
Step 1: install all the libary in requirements.txt 
Step 2: install 'xgboost_model.pkl' and 'duration_neural_network.h5' and also install all the file 'scaler_category_xgb.pkl','scaler_category.pkl','scaler_days.pkl','scaler_days_xgb.pkl'
'scaler_duration.pkl', 'caler_duration_xgb.pkl', 'scaler_text.pkl', 'scaler_text_xgb.pkl'      
Finally, run all cell in the file 'Input_SBERT_xgboost.inydb' if you want to classify using xgboost model, 'Input_BERT_MBNN.inydb' if you want to classify using MBNN model. Make sure you have all the require file in 1 folder when you use jupyter notebook or google colab or any IDE because the code in 2 file that i mention all use the file in Step 2. Run all cell then type in  the URL of the video you want to classify. Result will be like in the 'example.png' file

data from this linkhttps://drive.google.com/drive/folders/12U1VtZVBnvrPJOrE4Rxh4QIeGLH_AZz1?fbclid=IwY2xjawL-0exleHRuA2FlbQIxMABicmlkETBwQkMwZHMzbDZpV0NhMEFKAR4k6guEuO_lUIkTKF4gNYGfAtkqPbtt6h8YVIu_5e3nZATwRlk3_T8arZBvmw_aem_471TjXJc2y62NkFQ2LYrjw: