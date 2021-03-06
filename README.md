## vue-slider

### 目前只支持PC端

### 使用示例

```git
git clone https://github.com/PLDaily/vue-slider.git
```

```git
npm install
```
```git 
//测试
gulp dev
```
```git
//发布
gulp default
```

### 调用示例
```javascript
<style type="text/css">
*{
	padding: 0;
	margin: 0;
}
</style>
<template>
<div id="main">
	<slider :pages="slider_data" :sliderinit="sliderinit">
    </slider>
</div>
</template>
<script>
import Slider from './Slider.vue'
export default {
	components: {slider: Slider},
	data() {
		var sliderinit = {
            width: 710,
            height: 320,
            imgCount: 7,
            dots: true,//是否显示轮番点
            button: true,//是否显示前进后退按钮
            currentPage: 0,//起始页
            changeTime: 5000,//时间间隔
            animateTime: 1000,
            autoplay:true//自动播放
        };
        var slider_data = [
	        {
	        	title: "Colosseo (Colosseum), ca. 75 AD",
	        	src: "../img/feature-colosseo.jpg"
	        },
	        {
	        	title: "Fontana di Trevi (Trevi Fountain), 1762",
	        	src: "../img/feature-trevi.jpg"
	        },
	        {
	        	title: "Arco di Constantino (Arch of Constantine), 315 AD",
	        	src: "../img/feature-arch.jpg"
	        },
	        {
	        	title: "Santa Maria Maggiore",
	        	src: "../img/feature-santamaria.jpg"
	        },
	        {
	        	title: "Colonna Traiana (Trajan’s Column), 113 AD",
	        	src: "../img/feature-trajan.jpg"
	        },
	        {
	        	title: "Il Vittoriano, 1911",
	        	src: "../img/feature-vittoriano.jpg"
	        },
	        {
	        	title: "Locks near Trevi Fountain",
	        	src: "../img/feature-locks.jpg"
	        }
	    ];
	    return {
	    	sliderinit: sliderinit,
	    	slider_data: slider_data
	    }
	}
}	
</script>
```


### sliderinit参数

|  参数名称 | 类型 | 是否必须 |  示例  | 参数说明 | 默认 |
| :-----: | :----: | :--: | :--: | :-----: |:----------: |
| width | number |  是   | 710  | 轮播图的宽度 | 无 |
| height | number |  是   | 320  | 轮播图的高度 | 无 |
| imgCount | number |  是   | 7  | 轮播图图片数量 | 无 |
| dots | boolean |  是   |  true | 轮播图的轮播点 | 无 |
| button | boolean |  是   | true  | 轮播图的前后按钮 | 无 |
| currentPage | number |  是   | 0  | 轮播图的起始页面 | 无 |
| changeTime | number |  是   | 5000  | 轮播图的事件间隔 | 无 |
| animateTime | number |  是   | 500  | 轮播图的动画时长 | 无 |
| autoplay | boolean |  是   | true  | 轮播图是否自动播放 | 无 |



### slider_data参数

|  参数名称 | 参数说明 |
| :-----: | :----: | 
| title | img标签中alt值 | 
| src | img标签中src值 | 


### 具体项目中运用

[vuejs-project](https://github.com/PLDaily/vuejs-project)

### 完善
1.添加默认值
2.适配手机端
3.实现无缝滚动
