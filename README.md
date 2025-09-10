**現在テスト中のため、内容の正確性は保証されません。**

# 災害時被害マップ / Disaster Damage Map

このリポジトリは、災害時の被害箇所を地図上に可視化し、避難所の避難者数を共有するためのプロジェクトです。  
This repository is a project to visualize disaster damage locations on a map and share the number of evacuees at shelters.  
Folium を用いて生成した HTML 地図を GitHub Pages で公開しています。  
The HTML map generated using Folium is published via GitHub Pages.  

## 公開中の地図 / Live Map
https://yujiuchi.github.io/disaster-map/disaster.html

## 避難者数 / Number of Evacuees
避難所ごとの避難者数を CSV および HTML 表形式で公開しています。  
The number of evacuees at each shelter is published both as CSV and as an HTML table.  

- CSV: https://yujiuchi.github.io/disaster-map/evacuees.csv  
- HTML Table: https://yujiuchi.github.io/disaster-map/evacuees.html  

## 注意事項 / Disclaimer
本リポジトリの地図は、災害時に入力された情報を元に作成しています。  
This map is based on information entered during disaster situations.  
内容の正確性・最新性について保証するものではありません。  
It does not guarantee accuracy or timeliness of the information.  


## 使用技術/ Technologies Used
- python 
- FormBridge + kintone
- GitHub Pages

```mermaid

flowchart TD
sm1(smartphone)-->|take pictures and upload|fv1
fv1(FormBridge)-->|auto|kin1(kintone)
kin1-->|Python + Rest API|folium
folium-->|Python + PyGithub|git(Github-Pages)
sm2(smartphone)-->|input data|fv2
fv2(FormBridge)-->|auto|kin2(kintone)
kin2-->|Python + Rest API|pandas
pandas-->|Python + PyGithub|git

```
