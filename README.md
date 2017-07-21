# StepView
一个用自定义View实现的用于签到的小组件。

#  使用
1.布局文件中添加
```
 <com.rensw.stepview.HorizontalStepsViewIndicator
         android:id="@+id/stepView"
         android:layout_width="match_parent"
         android:layout_height="wrap_content"
         android:layout_centerInParent="true" />
  ```
2.填入数据
```
        stepsView = (HorizontalStepsViewIndicator) findViewById(R.id.stepView);
        //名称 签到状态  标记定位  是否有红包
        stepsBeanList.add(new PointBean("第1天", PointBean.STEP_SIGN, false, true));
        stepsBeanList.add(new PointBean("第2天", PointBean.STEP_SIGN));
        stepsBeanList.add(new PointBean("第3天", PointBean.STEP_SIGN, true));
        stepsBeanList.add(new PointBean("第4天", PointBean.STEP_UNSIGN));
        stepsBeanList.add(new PointBean("第5天", PointBean.STEP_UNSIGN,false,true));
        stepsBeanList.add(new PointBean("第6天", PointBean.STEP_UNSIGN));
        stepsBeanList.add(new PointBean("第7天", PointBean.STEP_UNSIGN));
        stepsBeanList.add(new PointBean("第8天", PointBean.STEP_UNSIGN));
        stepsBeanList.add(new PointBean("第9天", PointBean.STEP_UNSIGN));
        stepsView.setStepNum(stepsBeanList);
   ```
 3.点击签到
 ```
 stepsView.signAction();
 or
 stepsView.scrollToDays(6); 跳到指定的位置
  ```
# Preview
![Preview](img/ezgif-3-e528b8da87.gif)