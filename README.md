# libAOP
项目的根gradle：

dependencies {
        
        classpath 'com.hujiang.aspectjx:gradle-android-plugin-aspectjx:2.0.10'
 }
 
allprojects {

	repositories {
	
		maven { url 'https://jitpack.io' }
		
	}
	
}
  
moudle里面的配置：

apply plugin: 'android-aspectjx'
  
dependencies {

  	implementation 'com.github.Ghitbug:libAOP:V1.0.1'
	
 }
  
aspectjx {

        include "自己项目的包名", "com.gh.libaop"
	
        //可加可不加，有些第三方库不加会编译会报错
	
        exclude 'com.google', 'com.ut', 'rxhttp', 'com.squareup', 'org.apache', 'versions.9'
	
}

权限用法：

	@Permissions({RxPermissionsTool.PERMISSION_WRITE_EXTERNAL_STORAGE})
	private void test(int position) { 
	
	}

点击用法：

	@SingleClick
	private void test(int position) { 
	
	}
     
