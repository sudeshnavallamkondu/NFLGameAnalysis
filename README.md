# NFLGameAnalysis
# NFL Game Analysis Project

## Overview

This project analyses NFL play-by-play data to extract meaningful insights and predictions about game outcomes. The analysis involves cleaning the data, calculating post-priori characteristics, and generating feature-engineered datasets for further analysis.

## Directory Structure

nfl_analysis/
│
├── data/
│ ├── raw/ # Original data files
│ │ └── NFL_Play_by_Play_2009-2018.csv
│ ├── processed/ # Post-priori characteristics and feature-engineered datasets
│ │ ├── post_priori.csv
│ │ └── feature_engineered.csv
│
├── src/
│ ├── init.py
│ ├── data_loader.py
│ ├── feature_calculator.py
│ ├── scenario_analyser.py
│
└── main.py

## Modules

### `data_loader.py`

- **Functions**:
  - `load_and_clean_data(file_path: str) -> pd.DataFrame`: Loads and cleans the NFL data.
    - **Args**: `file_path` (str): Path to the raw CSV file.
    - **Returns**: Cleaned DataFrame.
  - `save_processed_data(df: pd.DataFrame, file_path: str) -> None`: Saves processed data to a CSV file.
    - **Args**:
      - `df` (pd.DataFrame): DataFrame to save.
      - `file_path` (str): Path to save the CSV file.

### `feature_calculator.py`

- **Functions**:
  - `calculate_post_priori(df: pd.DataFrame) -> pd.DataFrame`: Calculates post-priori characteristics for home and away teams.
    - **Args**: `df` (pd.DataFrame): Cleaned DataFrame with play-by-play data.
    - **Returns**: DataFrame with post-priori characteristics.
  - `save_post_priori(df: pd.DataFrame, file_path: str) -> None`: Saves post-priori characteristics to a CSV file.
    - **Args**:
      - `df` (pd.DataFrame): DataFrame to save.
      - `file_path` (str): Path to save the CSV file.

### `scenario_analyser.py`

- **Functions**:
  - `calculate_scenario_averages(post_priori: pd.DataFrame) -> pd.DataFrame`: Calculates averages for different scenarios.
    - **Args**: `post_priori` (pd.DataFrame): DataFrame with post-priori characteristics.
    - **Returns**: DataFrame with scenario averages.
  - `calculate_mutual_game_averages(df: pd.DataFrame) -> pd.DataFrame`: Calculates averages for mutual games played between teams.
    - **Args**: `df` (pd.DataFrame): DataFrame containing post-priori data.
    - **Returns**: DataFrame with mutual game averages.
  - `save_feature_engineered(df: pd.DataFrame, file_path: str) -> None`: Saves feature-engineered datasets to a CSV file.
    - **Args**:
      - `df` (pd.DataFrame): DataFrame to save.
      - `file_path` (str): Path to save the CSV file.

## Usage

1. Place the original NFL play-by-play data in the `data/raw/` directory.

2. Run the main script:

   ```bash
   python main.py

3. Processed datasets will be saved in the data/processed/ directory.

    Requirements

        python 3.x
        pandas
        numpy
        

    Install dependencies using pip:

    ```bash
    pip install pandas numpy

