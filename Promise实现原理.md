```
const Promise = function Promise (exectuor) {
	// 等待状态 pending resolved rejected 
	let status = 'pending';
	// 执行正常回调完成的操作集合 参考jq的on方法
	this.resolveCallbacks = [];
	// 执行异常回调完成的操作集合
	this.rejectCallbacks = [];
	resolve = 
	try {
	
		setTimeout(function(){
			executor(resolve, reject);
		})
	} catch(e) {
	
	}
}

```
