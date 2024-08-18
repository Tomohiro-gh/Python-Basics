# Python-Basics
Python: 環境設定などをまとめる


## Numpyのversionについて　24/08/18



Velocytoでエラーが出た．
`$ velocyto --help`

```python
AttributeError: module 'numpy' has no attribute 'typeDict'
```


調べてみるとこのような記事が出てくる　→ [AttributeError: module 'numpy' has no attribute 'XXX' エラーの解決ログ](https://qiita.com/yusuke_s_yusuke/items/bf7ce2deb6153ab0123b)

問題となっているのは，　 
> "基本的にnp.intのような書き方をしなければ問題ないです。np.intの代わりにintを使うといった具合です。"

のようなので，　

1. 解決策1. numpyをダウングレード　- > 1.24より下のversion, 例えば1.23.5など．
