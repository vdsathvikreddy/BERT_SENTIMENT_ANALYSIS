# SST-5 Sentiment Analysis with DistilBERT

A Streamlit app to predict sentiment (Very Negative, Negative, Neutral, Positive, Very Positive) for input sentences using a fine-tuned DistilBERT model on the SST-5 dataset.

## Setup
1. Install dependencies: `pip install -r requirements.txt`
2. Fine-tune locally: `python3 sst5_bert.py`
3. Upload model to Hugging Face: `api.upload_folder(folder_path="sst5_distilbert", repo_id="vdsr/sst5-distilbert", repo_type="model")`
4. Run locally: `streamlit run app.py`
5. Deploy on Streamlit Cloud.

## Files
- `sst5_bert.py`: Fine-tunes DistilBERT.
- `app.py`: Streamlit app for prediction.
- `requirements.txt`: Dependencies.
- Model hosted at: `https://huggingface.co/vdsr/sst5-distilbert`

## Notes
- Trained on 10,000 phrases, 1 epoch, ~17 minutes (CPU).
- Test accuracy: ~0.669.
- Inference: ~0.029 seconds/phrase (CPU).