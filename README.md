# JRE_timetables
JR東日本の時刻表データです。  
一般的な時刻表予定です。  
※一切の正確性は保証されていません。最新の情報はJR東日本公式サイトなどを確認して下さい。

# 時刻表データの追加について
編集著作物に当たらない、以下のようなこのリポジトリ独自の形式でPRを投げて下さい。  
trainSchedulesの中のデータは、timeを24時間表示で、typeをtrainTypesのindexで表して下さい。
```json
{
   "trainTypes":[
      "普通",
      "快速",
      "特別快速"
   ],
   "trainSchedules":[
      {
         "time":"05:13",
         "type":0
      },
      {
         "time":"06:00",
         "type":1
      },
      {
         "time":"06:30",
         "type":2
      },
      {
         "time":"15:00",
         "type":1
      }
   ]
}
```
