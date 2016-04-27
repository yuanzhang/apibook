# 请求参数
名称 	类型 	必选 	描述
client_id 	string 	yes 	申请应用时分配的APP_KEY
access_token 	string 	yes 	乘客认证信息
timestamp 	int 	yes 	时间戳
order_id 	int 	yes 	订单id
sign 	string 	yes 	签名
注意事项

暂无
访问频率限制

    订单接口访问增加频率限制
    司机计费前（status<500）访问限制在 10秒/次
    司机计费后（status>=500）访问限制在 300秒/次
    如果超频：返回 errno: 36003

返回数据



{
    "errno": 0,
    "errmsg": "SUCCESS",
    "data": {
        "order": {
            "id": "4880109188406595918",
            "city": "1",
            "type": 0,
            "passenger_phone": "13269661202",
            "status": 400,
            "driver_name": "张师傅",
            "driver_phone": "18612249028",
            "driver_num": 109,
            "driver_car_type": "日产天籁",
            "driver_card": "冀A**G05",
            "driver_avatar": "http://xxxxx.jpg",
            "driver_order_count": "307",
            "driver_level": "4.9",
            "dlng": 116.307479,
            "dlat": 40.045724,
            "clng": 116.307479,
            "clat": 40.045724,
            "flng": 116.307479,
            "flat": 40.045724,
            "tlng": 116.800012,
            "tlat": 39.689123,
            "extra_info": "微信支付",
            "start_name": "得实大厦",
            "start_address": "得实大厦东门",
            "end_name": "万达广场",
            "end_address": "万达广场西北角",
            "departure_time": "2015-03-11 17:06:58",
            "require_level": "100",
            "strive_level": "100",
            "begin_charge_time": "2015-03-11 15:06:58",
            "finish_time": "2015-03-11 16:06:58",
            "normal_distance": "4.80"
        },
        "price": {
            "total_price": "23.00",
            "detail": [
                {
                    "name": "远途费"或"超出套餐部分远途费",
                    "amount": "12.00",
                    "type": "empty_fee"
                },
                {
                    "name": "高速费",
                    "amount": "35.00",
                    "type": "highway_fee"
                },
                {
                    "name": "路桥费",
                    "amount": "15.00",
                    "type": "bridge_fee"
                },
                {
                    "name": "低速费"或"超出套餐低速费",
                    "amount": "55.00",
                    "type": "low_speed_fee"
                },
                {
                    "name": "夜间费用"或"超出套餐部分夜间费",
                    "amount": "10.00",
                    "type": "night_fee"
                },
                {
                    "name": "正常行驶费用"或"超出套餐部分行驶距离费",
                    "amount": "10.00",
                    "type": "normal_fee"
                },
                {
                    "name": "其他费用",
                    "amount": "10.00",
                    "type": "other_fee"
                },
                {
                    "name": "停车费",
                    "amount": "10.00",
                    "type": "park_fee"
                },
                {
                    "name": "起步价格",
                    "amount": "15.00",
                    "type": "start_price"
                },
                {
                    "name": "加价费用",
                    "amount": "10.00",
                    "type": "tip_fee"
                },
                {
                    "name": "'快车最低消费补足",
                    "amount": "10.00",
                    "type": "limit_pay"
                },
                {
                    "name": "套餐费用",
                    "amount": "110.00",
                    "type": "combo_fee"
                },
                {
                    "name": "快车时长费",
                    "amount": "40.00",
                    "type": "normal_time_fee"
                },
                {
                    "name": "违约费",
                    "amount": "10.00",
                    "type": "cancel_fee"
                },
                {
                    "name": "动态调价费用",
                    "amount": "19.00",
                    "type": "dynamic_price"
                },
                {
                    "name": "等候费",
                    "amount": "10.00",
                    "type": "wait_fee"
                }
            ]
        }
    }
}


