# q1

```
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for(let i=0; i<nums.length - 1 ; i++){
        for(let l=i+1; l<nums.length; l++){
            if ( nums[i] + nums[l] == target ) {
               return [i,l];
            }
        }
    }
};
```

# q2

```
/**
 * @param {number} x
 * @return {number}
 */
var reverse = function(x) {
  if ( x > -10 && x < 10 ) { return x; }  
  if ( x > Math.pow(2,31) -1 || x < Math.pow(-2,31) +1 ){ return 0;}  
  let n_str = String(x);
  let arr = [];
  for (let i =0; i < n_str.length;i++){
    arr[i] = n_str[i];
  }
  let m_flag = (arr[0] == '-') ? true:false;
  if(m_flag){arr.shift();}
  let ans = arr.reverse();
  let a = 0;
  for (i=0;i<ans.length;i++){
    a = a + ans[i] * Math.pow(10,ans.length - (1+i));
  }
  if (m_flag){ a = a * -1;}
  if ( a > Math.pow(2,31) -1 || a < Math.pow(-2,31) +1 ){ return 0;} 
    return a;   
};
```
