```
const Promise = function Promise (exectuor) {
	// 等待状态 pending resolved rejected 
	this.status = 'pending';
	// 执行正常回调完成的操作集合 参考jq的on方法
	this.resolveCallbacks = [];
	// 执行异常回调完成的操作集合
	this.rejectCallbacks = [];
	// 接受胡
	this.data = null;
	let resolve = (value) => {
		if (this.status === 'pending') {
			this.status = 'resolved';
			for(let i =0;)
		}
	}
	try {
	
		setTimeout(function(){
			executor(resolve, reject);
		})
	} catch(e) {
	
	}
}

```
