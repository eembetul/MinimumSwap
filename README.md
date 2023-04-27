# MinimumSwap
Given an array of n distinct elements. Find the minimum number of swaps required to sort the array in strictly increasing order.



This line declares a function named minSwaps that takes a reference to a vector of integers as input and returns an integer.

int n = nums.size(); declares an integer variable n and initializes it with the size of the input vector nums.

vector<pair<int,int>> v(n); creates a vector of pairs named v with size n. Each element of the vector is a pair of integers.

The for loop initializes v with the index and value of each element in nums. For example, if nums is {3, 1, 5, 2}, v will be initialized with {(3,0), (1,1), (5,2), (2,3)}.

sort(v.begin(), v.end()); sorts the vector v in ascending order based on the value of the first element in each pair.

vector<bool> visited(n, false); creates a vector of booleans named visited with size n, initializing all values to false.

int ans = 0; initializes an integer variable ans to 0, which will be used to keep track of the minimum number of swaps required.

The for loop iterates over each element in nums.

Inside the loop, if (visited[i] || v[i].second == i) checks if either the current element has already been visited or if the current element is already in the correct position. If either condition is true, the loop skips to the next iteration.

If the current element is not in the correct position, the code enters the following while loop.

int j = v[i].second; initializes an integer variable j to the index of the element in nums that should be at the current position.

visited[j] = true; sets the value of the boolean element in visited corresponding to the index j to true, indicating that the element has been visited.

i = j; sets the value of the loop variable i to j, so the loop will continue with the element that was just moved to the current position.

ans++; increments the ans variable to count the number of swaps made.

After all elements have been visited, the function returns the value of ans, which represents the minimum number of swaps required to sort the vector.

I hope this helps! Let me know if you have any questions.
