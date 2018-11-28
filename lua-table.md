#lua-table遍历方式

## 1. pairs遍历

- 例子:

```
for key, value in pairs(tbtest) do      
    XXX  
end  
```

> pairs根据tbtest中key的hash值排列的顺序来遍历，并非创建table时各个元素的顺序


## 2. ipairs遍历

- 例子

```
for key, value in ipairs(tbtest) do      
    XXX  
end 
```

> ipairs会从table数组（lua的hash表和数组都是用的table）下标1开始，一直遍历到key不连续为止（即下表非数字）

## 3. i=1,#xxx 遍历

- 例子

```
for i=1, #(tbtest) do      
    XXX  
end  
```

> 这种遍历依赖于#xxx获取到的长度，通常建议用于数组型table，且下表连续