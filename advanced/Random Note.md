---
banner: "template/media/banner2.jpg"
banner_x: 0.5
banner_y: 0
---

## 随机读书笔记

```dataviewjs
//使用时修改关键词即可
const term = "#Quote"
const files = app.vault.getMarkdownFiles()
const arr = files.map(async ( file) => {
const content = await app.vault.cachedRead(file)
const lines = content.split("\n").filter(line => line.contains(term))
return lines
})

function generateArray (start, end) { return Array.from(new Array(end + 1).keys()).slice(start) }

Promise.all(arr).then(values => {
	//不包含本文
	let noteArr = values.flat().filter(note => !note.includes("term"))
	//生成一个连续数值的数组
	let arrNum = generateArray(0,noteArr.length-1)
	let result = [ ]
	let ranNum = 3
	
	for (let i = 0; i < ranNum; i++) {
		var ran = Math.floor(Math.random() * (arrNum.length - i))
		result.push(arrNum[ran])
		arrNum[ran] = arrNum[arrNum.length - i - 1]
	}
	
	for(let i=0; i< result.length;i++){
		let j = result[i]
		dv.paragraph(`${noteArr[j]}`)
	}
})
```
