```
const Promise = function Promise (exectuor) {
	// 等待状态 pending resolved rejected 
	this.status = 'pending';
	// 执行正常回调完成的操作集合 参考jq的on方法
	this.resolveCallbacks = [];
	// 执行异常回调完成的操作集合
	this.rejectCallbacks = [];
	// 接受数据
	this.data = null;
	let resolve = (value) => {
		if (this.status === 'pending') {
			this.status = 'resolved';
			for(let i =0, len = this.resolveCallbacks.length; i < len; i++) {
				this.resolveCallbacks[i]();
			}
		}
	}
	try {
	
		setTimeout(function(){
			executor(resolve, reject);
		})
	} catch(e) {
	
	}
}

Promise.prototype.then = function (onResolve = function () {}, onReject = function () {}) {
	this.resolveCallbacks.push(onResolve)
	this.rejectCallbacks.push(rejected);

	return new Promise(function () {
	})
}

```
