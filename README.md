<!--
 * @Author: w_gd
 * @Date: 2023-07-14 17:02:22
 * @LastEditors: wang_gd 931017900@qq.com
 * @LastEditTime: 2023-07-14 17:41:48
 * @FilePath: /cocosengine/README.md
 * @Description: 
 * 
 * Copyright (c) 2023 by ${git_name_email}, All Rights Reserved. 
-->
# CocosEngine 2023-07-14
   1. 将游戏资源解压至读写目录下的engine文件下 
      activity.getFilesDir().getAbsolutePath()+ File.separator + "engine";
   2. 初始化引擎适配器 解析实现自定义接口 详情第四点
        Cocos2dxHelper.initCustomAdapter(new Cocos2dxHelper.CustomAdapter(){
            @Override
            public Object engineCallInterface(String model) {
                return null;
            }
        });
   3. 启动 CocosEngineActivity
        Intent intent = new Intent(MainActivity.this, CocosEngineActivity.class);
        intent.addFlags(Intent.FLAG_ACTIVITY_REORDER_TO_FRONT);
        startActivity(intent);
        finish();
   4. 待实现接口  
        JSONObject paramObj = JSONObject.parseObject(model);
        Object callData = null;
        String key = paramObj.getString("key");
        key等于 "openWeb","faceBookLogin"........
        //        openWeb(paramObj.getString("url"), paramObj.getString("title"), paramObj.getIntValue("time"));
        //        faceBookLogin();
        //        faceBookShareLink(paramObj.getString("url"), paramObj.getString("quote"));
        //        faceBookShareMessenger(paramObj.getString("url"), paramObj.getString("quote"));
        //        postFacebookEvent(paramObj.getString("eventName"), paramObj.getString("eventValue"), paramObj.getString("eventParam"));
        //        afCustomEvent(paramObj.getFloatValue("value"), paramObj.getString("type"), paramObj.getString("currency"));
        //        getAFChannel();
        //        getAFUserId();
        //        getAFData();
        //        setAFCustomerId(paramObj.getString("userId"));
        //        creatEasyFloatBtn(paramObj.getString("id"), paramObj.getIntValue("type"), paramObj.getString("textFiled"));
        //        dismissEasyFloatBtn(paramObj.getString("id"));
        //        showOrHideEasyFloat(paramObj.getString("tag"), paramObj.getIntValue("type"));