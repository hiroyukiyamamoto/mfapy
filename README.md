インストールメモ
----------------------------------------
Anacondaをダウンロード、インストール

Githubからmfapy ( https://github.com/hiroyukiyamamoto/mfapy )をクローンする
	(オリジナルのmfapyはテストでエラーになるので修正済みのものを使用)

Anaconda Promptでmfapyをカレントディレクトリにして以下のコマンドを順番に実行

	conda create -n mfapy python=3.6 numpy scipy matplotlib=2.1 joblib

	conda activate mfapy

	conda install -c conda-forge nlopt

	conda install -c anaconda mkl-service 

	python setup.py install

インストールテスト結果を確認

	python setup.py test

エラーが出なければインストールは完了

nloptがcondaでうまくインストールされないことがあるので、その場合はpipでインストールすると上手くいく(ことがある？)

	pip install nlopt


サンプルスクリプトの実行
----------------------------------------
VSCodeを起動し、Terminal右下の実行環境をPython 3.6.13('mfapy':conda)に変更した後、mfapy/sampleフォルダ内のpythonスクリプトを実行する。


実行済み (リモートPC)
----------------------------------------
(PC1) Example_0_toymodel.py、Example_1_toymodel.py、Example_2_1_Ecoli.py 

(PC2) Tutorial_3_mfapy_functions.py、Tutorial 2_INST-MFAtoymodel.py、Tutorial 1_13C-MFAEcoli.py、Explanation_1_13CMFA_toymodel.py

未検証

Example_2_2_Ecoli_solver_comparison.py、Example_2_3_Ecoli_local_optimum.py、Example_2_2_Ecoli_solver_comparison.py　…

