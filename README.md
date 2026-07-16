## データ
QM9データセット（Ramakrishnan et al., 2014）を使用。
DeepChemが公開しているCSV（https://deepchemdata.s3-us-west-1.amazonaws.com/datasets/qm9.csv）から取得。
"""
QM9のSMILES＋バンドギャップCSV（例: input_data/qm9_smiles_gap_eV.csv）を読み込み、
以下3種類の分子表現をそれぞれ別々のCSVとして出力するスクリプト。

  1. RDKit記述子       -> input_data/qm9_descriptors.csv
  2. Morganフィンガープリント -> input_data/qm9_morgan_fp.csv
  3. MACCSキー          -> input_data/qm9_maccs_keys.csv

各出力CSVには先頭2列として smiles, gap_eV を含める（学習時にそのまま特徴量とラベルに分けやすいように）