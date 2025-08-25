# utf-horizontal-bar-chart

Ex. (85) - Horizontal chart with UTF characters proportional with max array.


This code performs several operations on an array a and generates a UTF-8 text-based bar chart, where the length of each bar is proportional to the corresponding element in the array <i>a</i> concerning the maximum value in the array. An array <i>a</i> is defined with a set of numeric values. Variables <i>m</i>, <i>t</i>, and <i>max_value</i> are initialized. Variable <i>m</i> represents the total number of characters for each bar in the chart, <i>t</i> will store the final text result, and <i>max_value</i> will keep track of the maximum value in the array. The length of the array <i>a</i> is determined and stored in variable <i>n</i>. A for-loop is used to find the maximum value in the array. It iterates through each element of <i>a</i>, and if the current element is greater than the current <i>max_value</i>, it updates <i>max_value</i> with the current element. Another for-loop is used to create the bar chart. It iterates through each element of <i>a</i> again. Inside the second loop, a variable <i>f</i> is calculated. It represents the length of the current bar and is calculated as (<i>m</i> / <i>max_value</i>) * <i>a</i>[<i>i</i>], which scales the length of the bar based on the ratio of the current element value to the maximum value in the array. Within a nested loop (for-loop with variable <i>k</i>), the code checks if <i>k</i> is less than <i>f</i>. If <i>k</i> is less than <i>f</i>, it appends a filled square character (“▮”) to the string <i>t</i>, indicating the filled portion of the bar. Otherwise, it appends an empty square character (“▯”) to represent the empty portion of the bar. After each bar is constructed, the code adds a newline character to <i>t</i> to start a new line for the next bar. Next, the resulting <i>t</i> variable, containing the text-based bar chart, is printed to the console. This code essentially visualizes the values in the array <i>a</i> by representing them as bars in a simple text format, where the length of each bar is proportional to the value it represents concerning the maximum value in the array.

## Example in Python:

```python
a = [5, 2, 8, 4, 6, 22, 8, 9]

m = 15
t = ''
max_value = 0

n = len(a)

for i in range(n):
    if a[i] > max_value:
        max_value = a[i]

for i in range(n):
    
    f = int((m / max_value) * a[i])
    
    for k in range(m):
        
        if k < f:
            t += '▮'
        else:
            t += '▯'

    t += '\n'

print(t)
``` 


```text
Python output:
▮▮▮▯▯▯▯▯▯▯▯▯▯▯▯
▮▯▯▯▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▯▯▯▯▯▯▯▯▯▯
▮▮▯▯▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▮▮▮▮▮▮▮▮▮▯
▮▮▮▮▮▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▮▯▯▯▯▯▯▯▯▯
```

## Example in Javascript:

```javascript
let a = [5, 2, 8, 4, 6, 22, 8, 9];

let m = 15;
let t = '';
let max = 0;

let n = a.length;

for(let i=0; i<n; i++){
    if(a[i]>max){max=a[i];}
}

for(let i=0; i<n; i++){
    
    f = Math.floor((m/max) * a[i]);
    
    for(let k=0; k<m; k++){
        
        if(k<f){
            t += '▮';
        } else {
            t += '▯';
        }
    }

    t += '\n';
}

print(t);
```

```text
Javascript output:
▮▮▮▯▯▯▯▯▯▯▯▯▯▯▯
▮▯▯▯▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▯▯▯▯▯▯▯▯▯▯
▮▮▯▯▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▮▮▮▮▮▮▮▮▮▯
▮▮▮▮▮▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▮▯▯▯▯▯▯▯▯▯
```

## Example in Matlab:

```matlab
a = [5, 2, 8, 4, 6, 22, 8, 9];
m = 15;
t = '';

maxVal = max(a);
n = length(a);

for i = 1:n
    f = floor((m / maxVal) * a(i));
    
    for k = 1:m
        if k <= f
            t = [t '▮'];
        else
            t = [t '▯'];
        end
    end
    
    t = [t '\n'];
end

fprintf(t);
```

```text
Matlab output:
▮▮▮▯▯▯▯▯▯▯▯▯▯▯▯
▮▯▯▯▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▯▯▯▯▯▯▯▯▯▯
▮▮▯▯▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▯▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▮▮▮▮▮▮▮▮▮▯
▮▮▮▮▮▯▯▯▯▯▯▯▯▯▯
▮▮▮▮▮▮▯▯▯▯▯▯▯▯▯
```

## References

- <i>Paul A. Gagniuc. Coding Examples from Simple to Complex - Applications in Python, Springer, 2024, pp. 1-245.</i>
- <i>Paul A. Gagniuc. Coding Examples from Simple to Complex - Applications in MATLAB, Springer, 2024, pp. 1-255.</i>
- <i>Paul A. Gagniuc. Coding Examples from Simple to Complex - Applications in Javascript, Springer, 2024, pp. 1-240.</i>

***
