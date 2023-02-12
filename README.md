# JRE_timetables
JR東日本の時刻表データです。  
※非公式のデータであり、一切の正確性は保証されていません。最新の情報はJR東日本公式サイトなどを確認して下さい。

# 時刻表データの追加について
編集著作物に当たらない、以下のようなこのリポジトリ独自の形式でPRを投げて下さい。  
trainSchedulesの中のデータは、timeを24時間表示で、typeとdstをtrainTypesとtrainDestinationsのindexで表して下さい。
```json
{
   "stationName": "サンプル駅",
   "lineName": "サンプル線",
   "trainTypes":[
      "普通",
      "快速",
      "特別快速"
   ],
   "trainDestinations": ["サンプル4駅", "サンプル5駅"],
   "isHoliday":true,
   "trainSchedules":[
      {
         "time":"05:13",
         "type":0,
         "dst": 1
      },
      {
         "time":"06:00",
         "type":1,
         "dst": 0
      },
      {
         "time":"06:30",
         "type":2,
         "dst": 1
      },
      {
         "time":"15:00",
         "type":1,
         "dst": 0
      }
   ]
}
```
