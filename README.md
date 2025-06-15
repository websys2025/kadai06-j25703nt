[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/J1qyflp_)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19785385&assignment_repo_type=AssignmentRepo)
## 第6講目の演習課題
### 課題6-1．eStat-APIを使って、人口推計以外のデータを取得するプログラム kadai6-1.py を作成せよ。
* リファレンスを参照して、任意のデータを自分で選ぶこと。
* 作成したファイルは自分で追加すること。
* 取得したデータの種類、エンドポイントと機能、使い方などを、コード内にコメントで記述すること。
* import requests

APP_ID = "c6ee3aa7dcd05fdc7bc69d838ba441822b756ee9"
API_URL  = "https://api.e-stat.go.jp/rest/3.0/app/json/getStatsData"#統計表データ取得用のエンドポイント

params = {
    "appId": APP_ID,
    "statsDataId":"0003349246",#若者に関する調査
    "cdArea":"00000",
    "metaGetFlg":"Y",
    "cntGetFlg":"N",
    "explanationGetFlg":"Y",
    "annotationGetFlg":"Y",
    "sectionHeaderFlg":"1",
    "replaceSpChars":"0",
    "lang": "J"  # 日本語を指定
}



#response = requests.get(API_URL, params=params)
response = requests.get(API_URL, params=params)#requests.get() で API にリクエスト送信。
# Process the response
data = response.json()#.json() でレスポンスをJSON型に変換。
print(data)#出力

### 課題6-2．世の中のオープンデータを調査し、そこから一つ選んで、データを取得するプログラム kadai6-2.py を作成せよ。
* 作成したファイルは自分で追加すること。。
* 参照するオープンデータの名前と概要、エンドポイントと機能、使い方などを、コード内にコメントで記述すること。

### 課題提出方法（期限：6/15）
* 随時、作業内容をコミットして、自分の課題リポジトリに履歴を残すこと。
* 上記の課題が完成したら、プルリクエストを使って提出すること。
* 教員、TA/SAが確認したらフィードバックする。
