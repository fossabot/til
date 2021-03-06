## EffetiveType

Display connection performance

```
console.log(navigator.connection.effectiveType); // 4G
```

> Possible values for effectiveType are 'slow-2g', '2g', '3g', or '4g'. 

Useful for example to determine if the content should be prefech or not

You can even monitor the connection change using event listener

```
function onConnectionChange() {
    const { rtt, downlink, effectiveType,  saveData } = navigator.connection;

    console.log(`Effective network connection type: ${effectiveType}`);
    console.log(`Downlink Speed/bandwidth estimate: ${downlink}Mb/s`);
    console.log(`Round-trip time estimate: ${rtt}ms`);
    console.log(`Data-saver mode on/requested: ${saveData}`);
}

navigator.connection.addEventListener('change', onConnectionChange)
```

## Bitwise operators

 - `Number(12).toString(2)` convert `12` into binary (1100)
 - `9 | 12` compare and return new binary user OR statement,
Example, 9=1001 and 12=1100. Comparing if one or both is `1`, will produce `1`. (1100 | 1001 = 1101)
 - `9 & 12` compare and return new binary using AND statement,
Example, 9=1001 and 12=1100. Comparing if both are 1 will produce `1`. (1100 & 1001 = 1000)
 - `9 ^ 12` comapre and return new binary using exclusive or. Will produce `1` only if one of the is `1`. (1100 ^ 1001 = 0101)


### References

 - [Adaptive Serving using JavaScript and the Network Information API][0]

[0]:  https://dev.to/addyosmani/adaptive-serving-using-javascript-and-the-network-information-api-331p
