1. ReID部分：识别到人 → 把真实值填进schema_A.json的结构 → 发JSON字符串给UI和数据库模块。 

2. UI部分：收到A → 用x,y,w,h画框 → 拿id去数据库查B里的name和job → 显示在框上。 

3. 数据库部分：收到A → 拿着id查档案表，没有就用schema_B.json建空档案 → 同时把A里的时刻、坐标、id直接写进来访记录表（不需要任何JSON做中间商）