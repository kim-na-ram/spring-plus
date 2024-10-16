# SPRING PLUS
## 유저 닉네임 검색 API
### 성능 개선 전
![JMeter_성능개선전](https://github.com/user-attachments/assets/dbd1287f-fa03-4776-ab39-c96844b1fccc)
* 평균 367ms
* 최소 337ms
* 최대 416ms

<br/>

### 성능 개선 후
#### Redis Cache
![JMeter_성능개선후_redis](https://github.com/user-attachments/assets/d83139b4-5899-4dc8-8b3a-1b9ed577c08d)
![JMeter_성능개선후_redis_cache_miss](https://github.com/user-attachments/assets/38737678-8b4b-4b02-b53d-8ca9fbb1d728)
* Cache Miss 의 경우
  * 323ms
* Cache Hit 의 경우
  * 3ms ~ 4ms

<br>

#### DB Index
![JMeter_성능개선후_인덱스](https://github.com/user-attachments/assets/130e1e21-cffa-400e-92a6-1d77d9e0116a)
* 평균 4ms 
* 최소 3ms
* 최대 12ms

<br>

#### Redis Cache + DB Index
![JMeter_성능개선후_인덱스_redis](https://github.com/user-attachments/assets/d459bcbe-b4cf-4ca4-b359-884d5f8e07e4)
![JMeter_성능개선후_인덱스_reids_cache_miss](https://github.com/user-attachments/assets/9ab04c57-2fb9-4f52-9578-986abdff3568)
* Cache Miss 의 경우
  * 31ms
* Cache Hit 의 경우
  * 2ms ~ 6ms

<br>

#### Ehcache
![JMeter_성능개선후_ehcache](https://github.com/user-attachments/assets/7c69eb3d-518d-4108-9f52-6a7e7da9cc45)
![JMeter_성능개선후_ehcache_cache_miss](https://github.com/user-attachments/assets/bae1f7a3-b447-47ab-980e-f56fd1dd9399)
* Cache Miss 의 경우
  * 487ms
* Cache Hit 의 경우
  * 2ms ~ 6ms

<br>

#### Ehcache + DB Index
![JMeter_성능개선후_인덱스_ehcache](https://github.com/user-attachments/assets/1e338c93-8c38-496f-94d3-c851168baf73)
![JMeter_성능개선후_인덱스_ehcache_cache_miss](https://github.com/user-attachments/assets/39cce56d-e453-40ef-829c-73986d1b306a)
* Cache Miss 의 경우
  * 9ms
* Cache Hit 의 경우
  * 2ms ~ 4ms