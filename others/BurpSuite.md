# Burp Suite

色々できるローカルプロキシツール

基本的に付けっ放しにしておいたほうが楽な気がする。

## 基本的な使い方
- ブラウザにローカルプロキシとして登録しておいて、リクエストの内容などを見たくなったら`Proxy > HTTP history`を見る
- ProxyのInterceptをonにして、Repeaterにリクエストを送って、リクエストを編集して送信するのが便利
- 同様にして、Intruderににリクエストを送って、brute forceとかするのも便利

## 応用

### responseを書き換える
Proxy > Options > Match and Replace
![スクリーンショット 2020-05-28 9 08 22](https://user-images.githubusercontent.com/44139130/83084817-0c162200-a0c5-11ea-8bc2-e1550487a4bb.png)
