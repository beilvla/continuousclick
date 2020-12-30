# continuousclick
java和kotlin防止二次点击（自用）

使用方法 

 dependencies {
        classpath 'com.android.tools.build:gradle:3.5.3'
      
        classpath 'com.hujiang.aspectjx:gradle-android-plugin-aspectjx:2.0.10'
   
    }

//添加这句 

apply plugin: 'android-aspectjx'
添加依赖

implementation 'com.github.beilvla:continuousclick:1.1'

kotlin

你的view.setOnClickListener(
   
@SingleClick(value = 2000L)

//            @SingleClick   默认为true,间隔是1500

fun(_: View) {

 LogUtil.w("MAinAAAA", "${System.currentTimeMillis()} aaa")
 
  }
  
)
        
  你的view.setOnSingleClick {
            log("click btn3")
        }
        
        
        
java

你的view.setOnClickListener(new View.OnClickListener() {

@SingleClick

@Override

public void onClick(View v) {

LogUtil.INSTANCE.d("TIME", System.currentTimeMillis()+"${}");

}

});
