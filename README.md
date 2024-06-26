# Automatic Number Plate Recognition and EasyOCR

## Step 0: Environment Setup

- `conda create -n tfobjdetection pip python=3.9`
- `conda activate tfobjdetection`
- `pip install --ignore-installed --upgrade tensorflow==2.11.0`

## Step 1: Download Kaggle Dataset

 - Download Dataset via kaggle API or manually from [KAGGLE](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)
 - Follow the instructions for Downloading via [Kaggle API](https://www.kaggle.com/docs/api)
 - Run `kaggle datasets download -d andrewmvd/car-plate-detection` in the terminal where the project folder is

## Step 2: Move Dataset into a Training and Testing Partition

- Run `python ./1.PrepareDataset.py` locally

## Step 3: Training and Detection

- Upload file `ANPR_and_EasyOCR_ColabRun_v1.ipynb` in Google Colaboratory
- Remember to Upload `archive.tar` file of prepared dataset in the step 2 when running `ANPR_and_EasyOCR_ColabRun_v1.ipynb` in the directory `Tensorflow/workspace/images`
- Note down the latest checkpoint in the folder `Tensorflow\workspace\models\CUSTOM_MODEL_NAME\` e.g. `ckpt-100`. This will be required to enter in scripts `3.DetectFromImage_EasyOCR.py`, `4.DetectFromRealTimeFeed_EasyOCR.py`, `5.DetectFromVideos_EasyOCR.py`, `app.py` where `LOAD_CHECKPOINT = 'ckpt-101'`
- Afer training, Download the compressed file of trained model in the project folder and uncompress it.
- Note: `3.DetectFromImage_EasyOCR.py`, `4.DetectFromRealTimeFeed_EasyOCR.py`, `5.DetectFromVideos_EasyOCR.py` these are optional files.
 
## Step 4: Run the Streamlit UI
 - Run `streamlit run app.py`
 
## Link to Canva Presentation of the Project
 - Go [Canva](https://www.canva.com/design/DAFgKGGexVU/J7sS8TtyEFKXCdyQHrKZlg/edit)
