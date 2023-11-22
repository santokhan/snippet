# JavaScript date handler by [Santo](https://github.com/santokhan)

```javascript
let m = "2023-12"

function handleDate(monthInput: string, payload: 'prev' | 'next'): string {
    const date = new Date(monthInput);
    if (payload === 'next') {
        date.setMonth(date.getMonth() + 1);
    } else {
        date.setMonth(date.getMonth() - 1);
    }
    let m = date.getMonth();
    const monthList = ['01', '02', '03', '04', '05', '06', '07', '08', '09', '10', '11', '12']
    return [date.getFullYear(), monthList[m]].join("-");
}

console.log(handleDate(m, 'prev'));
console.log(handleDate(m, 'next'));
```
