# Personalised Workout Recommendation System

This project implements a personalised workout recommendation system using a combination of Long Short-Term Memory (LSTM) networks, Reinforcement Learning (DQN), and an optional Large Language Model (LLM) interface.

The system processes Fitbit activity and sleep data to estimate user fatigue, recommends an appropriate workout intensity, and provides a user-friendly explanation of the recommendation.

---

## Running the Notebook

This notebook is developed and tested using **Google Colab**.

If running in Colab, ensure the dataset files are uploaded to:
content/data/


---

## Required Files

Place the following files inside the `content/data/` directory:

- `dailyActivity_merged.csv`
- `minuteSleep_merged.csv`

These files are required for data preprocessing and model training.

---

## Pipeline Overview
Fitbit data → Data preprocessing → LSTM fatigue prediction → RL workout recommendation → LLM / fallback explanation


---

## LLM (Gemini) Setup (Optional)

The project includes an optional Large Language Model (LLM) interface using Google Gemini to generate natural-language explanations.

To enable this feature:

1. Obtain a Gemini API key from Google AI Studio  
2. In Colab, open the **Secrets panel (🔑 icon)**  
3. Add a new secret:  
   - **Name:** `GEMINI_API_KEY`  
   - **Value:** your API key  
4. Enable notebook access for the secret  

---

## Fallback Mode

If a Gemini API key is not available or the API is not accessible, the system will automatically use a **local fallback explanation module**.

This ensures the full system (LSTM + RL + explanation) remains functional without external dependencies.

---

## Notes

- The fatigue score used in this project is a synthetic proxy and not a direct physiological measurement.  
- The project is designed as a proof-of-concept for personalised fitness recommendation systems.  
- All components of the pipeline can run without requiring the LLM API.  

---

## End of README
