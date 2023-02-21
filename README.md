# JRE_timetables
JR東日本の時刻表データです。  
※非公式のデータであり、一切の正確性は保証されていません。最新の情報はJR東日本公式サイトなどを確認して下さい。

# データ形式・時刻表データの追加について
編集著作物に当たらない、以下のようなこのリポジトリ独自の形式でPRを投げて下さい。  
trainSchedulesの中のデータは、timeを24時間表示で、typeとdstをtrainTypesとtrainDestinationsのindexで表して下さい。
```json
{
   "stationName":"サンプル駅",
   "lineName":"サンプル線",
   "trainTypes":[
      "普通",
      "快速",
      "特別快速"
   ],
   "trainDestinations":[
      "サンプル4駅",
      "サンプル5駅"
   ],
   "isHoliday":true,
   "trainSchedules":{
      "513":
         {
            "type":0,
            "dst":1
         },
      "605":
         {
            "type":1,
            "dst":0
         },
       "630":
         {
            "type":2,
            "dst":1
         },
      "1500":
         {
            "type":1,
            "dst":0
         }
   }
}
```
## 前後の電車を調べる方法(Python)
```python
import json

with open("day.json") as f:
   data = json.load(f)

schedules = data["trainSchedules"]
# 調べたい時刻を24h形式で
target_time = 617

# 調べたい時刻をappendし、sort
departure_times = [int(key) for key in schedules]
departure_times.append(target_time)
departure_times.sort()

# 調べたい時刻のリストの中でのindexを取得
target_time_index = departure_times.index(target_time)

previous_train_time = departure_times[target_time_index - 1]
next_train_time = departure_times[target_time_index + 1]
```
