We are attempting to reverse an incoming array to our function in place without creating any new variables. The approach we are taking will be solving this problem for optimum time complexity and therefore avoiding the typical method chaining approach below: 

string.split().reverse().join()

Instead I will be implementing a dual pointer method by first setting up the pointers. 

let left = 0; 
let right = input.lenght -1; 

This will give me an index no I can use on the array input and increment and decrement as we go. For that we'll need a while loop: 

while (left <=right){
 let temp = input[left];
  input[left] = input[right];
  input[right] = temp;
   right--;
   left++;
}

As you can see we're simply swapping the left and right characters by pointing to their position in the input array and then moving our pointers towards the center of the array to repeat the process. Once, left = right the problem is solved! 
