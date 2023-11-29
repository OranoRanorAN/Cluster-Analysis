# cluster-analysis
HW5 for Data Mining

## Dataset Description
- `YikatongMetroData.txt`: Sample data of Shanghai citizens using metro cards for bus and subway travel during a specific period in September 2016 (24 hours). (Randomly sampled 10%, i.e., users with ID ending in "8").

- Field Descriptions:
  - `Price` (0/Non-0): When this field is 0, the record is an entry swipe; when this field is non-0, the record is an exit swipe.
  - `Discount Category` (Discount/Non-discount): According to Shanghai's public transportation card discount policy: "A 1 yuan discount for transfers between subway and bus within 120 minutes. All bus transfers are discounted. There is no discount for subway-to-subway transfers." Thus, when a record is marked as "Discount," it indicates a mode of transportation change (bus to subway or subway to bus).

## Data Analysis
1. Sampling: Due to the algorithm's long runtime, orders with user IDs ending in "888" were sampled, constituting around 1% of the original dataset. The sampling results can be found in "samplelabel.csv."
2. Trip:
  - Generate a dataset `trips.csv` with `Trip` as the unit of analysis, where each record contains information about a trip. A user may have multiple trips in the dataset.
  - Cluster trips for analysis.
3. Passenger:
  - Generate a dataset `passenger.csv` with `Passenger` as the unit of analysis, where each record contains information about a passenger (each user ID appears only once in the data).
  - Cluster passengers for analysis.

Clustering method used is **Hierarchical Clustering**.

For detailed results, refer to **hw5.pdf**.


## 数据集描述
- YikatongMetroData.txt：2016年9月某个周期四(24小 时时间内)上海市民使用公交卡地铁出行的样本数据(随机抽样了 10%，即用户 ID 结尾为“8”的人)

- 字段说明:  
  - 价格(0/非 0):当此字段为 0 时，此条纪录为进站刷卡;当此字段非 0 时， 此条纪录为出站刷卡
  - 优惠类别(优惠/非优惠):根据上海市公交卡优惠政策:“在 120 分钟内地 铁转公交和公交转地铁都优惠 1 元。公交转公交现在全部优惠(所有车辆)。地 铁转地铁没有优惠。”因此，当某条纪录为“优惠”时，说明用户换乘了交通工 具(数据集中未包含公交乘坐信息)。
  
## 数据分析
1. 抽样：因为算法运行时间太长，故抽取用户ID结尾为“888”的订单，占原数据集1%左右，抽样结果见“samplelabel.csv”
2. Trip：
  - 生成以“Trip”为分析单位的数据集“trips.csv”，即每条纪录为一个 Trip 的相关信息，一个用户有可能在数据中出现多个Trips
  - 对于trip进行聚类
3. Passenger：
  - 生成以“Passenger”为分析单位的数据集“passenger.csv”，即每条纪录为一个 Passenger 的相关信息(每个用户ID在数据中仅出现一次)
  - 对于passenger进行聚类

聚类方法为 **层次聚类**

详细结果阐释见 **hw5.pdf**
