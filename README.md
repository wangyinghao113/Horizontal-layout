# Horizontal-layout
css可实现手机端横向可滑动导航条
```
第一种方法  多了一层容器
.contain{
		overflow-x:auto; 
		&::-webkit-scrollbar {
        width: 0;
        height: 0;
    }
	}
	.contain .box{
        width: max-content; //手机端专用 最大的容器宽度
        display:-webkit-box; //与flex用一个即可，与兼容性有关，flex兼容性较好点，手机端两个都可以
        //display: flex; //flex可兼容到ie10 ， ie9之前都无力了，
	}
	.contain .box .con{
		margin: 20px;
	}
第二种方法
.box2{
	display: flex;
	overflow-x:auto; 
	&::-webkit-scrollbar {
        width: 0;
        height: 0;
    }
	}
.box2 .con{
	margin: 20px;
	display: table;
}
	
<div class="contain">
	<div class="box">
		<div class="con">我是第一个栏目</div>
		<div class="con">我是第二个栏目</div>
		<div class="con">我是第三个栏目</div>
		<div class="con">我是第四个栏目</div>
		<div class="con">我是第五个栏目</div>
		<div class="con">我是第六个栏目</div>
		<div class="con">我是第七个栏目</div>
	  ......
	</div>
</div>
<div class="box2">
		<div class="con">我是第一个栏目</div>
		<div class="con">我是第二个栏目</div>
		<div class="con">我是第三个栏目</div>
		<div class="con">我是第四个栏目</div>
		<div class="con">我是第五个栏目</div>
		<div class="con">我是第六个栏目</div>
		<div class="con">我是第七个栏目</div>
	  ......
	</div>
```
