# 仿网易音乐播放器
## 效果动图
![音乐播放器](demo.gif)

## js逻辑
- 添加歌曲列表
	> 把存储在数组对象中的歌曲添加到页面中

- 绑定事件
	- 绑定上一曲、下一曲 播放 暂停
	- 绑定 歌曲进度条 和 音量条
	- 绑定 播放模式
	- 绑定 列表切歌

## css 样式
- cd 旋转
> 设置 cd外背景 cd 和 唱片处于一个同心圆层叠

		.midXY {
    		position: absolute;
    		left: 50%;
    		top: 50%;
    		transform: translateX(-50%) translateY(-50%);
		}
> 设置经过一定时间旋转一定角度

		cd.interval = setInterval(function() {
			cd.dregree = (cd.dregree + 0.25) % 360
			var style = `translateX(-50%) translateY(-50%) rotateZ(${cd.dregree}deg)`
			cd.style.transform = style
		}, 20)

- 列表 明暗交替排列
> 通过加入 even 和 odd样式

		.odd {
	    	background: #ececef;
		}
		.even {
		    background: #fff;
		}

## html语义化
- HTML5 新增语义化标签
header footer article section

## HTML5
- audio 音频标签 
