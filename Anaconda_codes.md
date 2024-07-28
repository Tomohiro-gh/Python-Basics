# Anaconda
condaに関する備忘録


#### パッケージのインストール
```sh
conda install PacakgeName

## versionを指定する場合
conda install PacakgeName=X.Y.Z
## ex)
conda install numpy=1.19
```

#### 仮想環境一覧
```sh
conda info --envs
```
#### 環境の確認認できる
```sh
conda info -e　
```

#### 仮想環境の作成
```sh
conda create -n env_name libraries
```
#### 仮想環境の削除
```sh
conda remove -n myenv --all
```

#### プロキシ設定の確認
```sh
conda config --show
```

#### conda本体のアップデート
```sh
conda update -n base -c defaults conda
```

#### condaのパッケージアップデート　（activate後）
```sh
conda update --all
```




#### anaconda3 install 後 最初の設定
```
conda init bash
```

#### condaの削除 : https://cocolofun.co.jp/anaconda-uninstall/
```
conda install anaconda-clean
anaconda-clean --yes

## or

## anaconda3のディレクトリを全て削除する
cd /user/anaconda3
rm -rf ~/anaconda3
```

-----------------
## velocytoのための環境構築 （遺伝研スパコン 24/1/10）
velocyto installation guide ->   http://velocyto.org/velocyto.py/install/index.html
```
conda create -n velo python=3.9.16
conda activate velo

pip install pysam
conda install numpy scipy cython numba matplotlib scikit-learn h5py click

## install velocyto
pip install velocyto
## or
pip install -U --no-deps velocyto  

```
Tips: 
velocyto 0.17 is an alpha release and it is updated often. If you installed with pip make sure you run pip install -U --no-deps velocyto now and then.

Install with conda -> This installation method is NOT currently available. Our plan is make it available upon the 1.0 release.

インストールエラーに関する記述
 from velocyto.commands.velocyto import cli

https://github.com/velocyto-team/velocyto.py/issues/53

https://github.com/velocyto-team/velocyto.py/issues/186

(update 2024/1/19)

python version 3.8.18

velocyto :biocondaでインストール



-----------------
## scVeloのための環境構築
```
conda create -n scVelo python=3.8.16 scvelo notebook
conda activate scVelo

pip install pybind11 hnswlib
pip install python-igraph louvain
conda install -c anaconda openpyxl
```

