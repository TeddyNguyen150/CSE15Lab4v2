1.
![image](https://github.com/TeddyNguyen150/CSE15Lab4v2/assets/156158048/f9cfc21a-dcdf-4fbf-8142-5b6fda014506)

Hi, I was trying to get the dot product of 2 vectors. In this case, I want to take the dot product of a 2 vectors, one in a higher dimension than the other.
It should return a number since a 3 dimensional vector can exist in 4 dimensions but it gives me NaN.

Thank you!

2. 
The problem may be that you are trying to take the magnitude of vector2 in the dimension of vector1. In this case vector1's dimension is lower than vector2
so it doesn't take the highest dimension. So you may have to add "0" values to the end of the lowest vector in order to match the highest dimension. Also
the reason you are getting NaN is because the first 3 points of vector2 is 0, and since you are taking the magnitude in the 3rd dimension, it will be 0, then
when running similar, you are running a number / 0 which is NaN.

3. 
![image](https://github.com/TeddyNguyen150/CSE15Lab4v2/assets/156158048/eda6dddb-427b-4968-8dae-999852c197fe)

The bug was in fact that I was taking the magnitude of vector2 in respect to vector1's dimension. I fixed this by adding elements at the end of the lowest dimension.

Thank you!

4.
test.sh
![image](https://github.com/TeddyNguyen150/CSE15Lab4v2/assets/156158048/0dfe318a-70f3-4fd1-bbca-f8f7337ce544)

Before:
![image](https://github.com/TeddyNguyen150/CSE15Lab4v2/assets/156158048/28c7ed3d-1c4f-4c7d-925b-d56db01519ac)

After:
![image](https://github.com/TeddyNguyen150/CSE15Lab4v2/assets/156158048/cc9c8fd8-a181-4827-ae1f-7c5335cb6a9f)

To fix the bug we had to make the lowest dimension vector into the highest one, then once they're in the same dimension we can now properly take the magnitude.




Reflection:
I thought the auto grader was pretty cool. I thought it was pretty cool how we learned how they worked in general because we don't really think about how they work,
we just use them. I also thought it was interesting how simple they are, it really is just run tests and get the scores based off them, I thought it would've been a lot more.
