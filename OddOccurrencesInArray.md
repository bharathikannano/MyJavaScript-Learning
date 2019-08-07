Task description
A non-empty array A consisting of N integers is given. The array contains an odd number of elements, and each element of the array can be paired with another element that has the same value, except for one element that is left unpaired.

For example, in array A such that:

  A[0] = 9  A[1] = 3  A[2] = 9
  A[3] = 3  A[4] = 9  A[5] = 7
  A[6] = 9
the elements at indexes 0 and 2 have value 9,
the elements at indexes 1 and 3 have value 3,
the elements at indexes 4 and 6 have value 9,
the element at index 5 has value 7 and is unpaired.
Write a function:

function solution(A);

that, given an array A consisting of N integers fulfilling the above conditions, returns the value of the unpaired element.

For example, given array A such that:

  A[0] = 9  A[1] = 3  A[2] = 9
  A[3] = 3  A[4] = 9  A[5] = 7
  A[6] = 9
the function should return 7, as explained in the example above.

Write an efficient algorithm for the following assumptions:

N is an odd integer within the range [1..1,000,000];
each element of array A is an integer within the range [1..1,000,000,000];
all but one of the values in A occur an even number of times.



```javascript
function solution(A) {
    // write your code in JavaScript (Node.js 8.9.4)
    let newArray = [];
    A.forEach(function(value) {
  if(newArray.includes(value)){
            newArray.splice(newArray.indexOf(value),1);
        }else{
            newArray.push(value);
        }
});
    return newArray[0];
}

```

## Other Way

```javascript
A.sort().filter((v,ind,arr) => {
if(arr[0] === a[1]){
arr.splice(0,2);
}});

return A[0];

```

```javscript

<div id="circle" onclick="incSize()"></div>

#circle{
    height: 50px;
    width: 50px;
    border: 1px solid red;
    border-radius: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}  

function incSize(){
  if((window.innerHeight > document.getElementById('circle').offsetHeight) && (window.innerWidth > document.getElementById('circle').offsetWidth)){
    
   document.getElementById("circle").style.height = document.getElementById('circle').offsetHeight+50+'px';
   document.getElementById("circle").style.width = document.getElementById('circle').offsetWidth+50+'px';
    
  }else{
    
   document.getElementById("circle").style.height = '50px';
   document.getElementById("circle").style.width = '50px';
  
  }
}
```
