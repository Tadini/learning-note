```
const Promise = function Promise (exectuor) {
	// 等待状态 pending resolved rejected 
	let status = 'pending';
	// 完成
	this.resolveCallbacks = [];
}

```
