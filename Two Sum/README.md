<h1> Two Sum </h1>
<p>
  You will be Given an array <b>arr[] of n integers </b> and a <b>target value</b>
</p>
<p>
  <h3>Task :</h3> Find whether there is a <b>pair of elements in the array whose sum is equal to target.</b>
</p>

![Solution Explanation](./carbon.png)
<p>
  <h2>Brute Force Approach:    </h2>
  <ul>
    <li>Time Complexity : O(n<sup>2</sup>) </li>
    <li>Space Complexity : O(1) </li>
  </ul>
<p>
  <h3>Steps to Solve:</h3>
</p>
<ul>
  <li>Generate all the possible pairs.</li>
  <li>Check the sum of each pair.</li>
  <li>Return the True if the pair that matches the target. Otherwise False.</li>
</ul>

<h1>Code: </h1>

```cpp
bool twoSum(vector<int> &arr, int target)
{
    int n = arr.size();
    // Iterate through each element in the array
    for (int i = 0; i < n; i++)
    {
        // For each element arr[i], check every
        // other element arr[j] that comes after it
        for (int j = i + 1; j < n; j++)
        {
            // Check if the sum of the current pair
            // equals the target
            if (arr[i] + arr[j] == target)
            {
                return true;
            }
        }
    }
    // If no pair is found after checking
    // all possibilities
    return false;
}
```
<p>
  <h2>Better Approach:</h2>
</p>
  <ul>
    <li>Time Complexity : O(nlog(n))</li>
    <li>Space Complexity : O(1) </li>
  </ul>
<p>
  <h2>Steps to Solve:</h2>
</p>
<h3> Using Two Pointer Technique :</h3>
Disclaimer : The array must be sorted.
<ul>
  Initialize: <b>Left = 0</b>, <b>Right = n – 1</b> Where n is size of the array
<ul>
 Run a loop <b>while Left < Right,</b>, do the following inside the loop

  <li>Compute current <b>sum</b> , <h3>Sum= arr[left] + arr[right] </h3></li>
  <li>If the <b>Sum</b> equals the <b>Target</b>, we’ve found the pair.</li>
  <li>If the <b>Sum</b> is less than the <b>Target</b>, move the <b>Left </b> pointer to the right to increase the sum.</li>
  <li>If the <b>Sum</b> is greater than the <b>Target</b>, move the <b>Right </b> pointer to the left to decrease the sum.</li>

</ul>
<h2>
    Visualization :
</h2>
<div style="display: flex; overflow-x: scroll; gap: 30px;">
    <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240930115147/two-pointer-tech-1.webp" alt="Two Pointer Technique" width="450" heigth="400"> 
    <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240930115143/two-pointer-tech--2.webp" alt="Two Pointer Technique" width="450">
    <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240930115144/two-pointer-tech--3.webp" alt="Two Pointer Technique" width="450">
   <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240930115145/two-pointer-tech--4.webp" alt="Two Pointer Technique" width="450">
   <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240930115146/two-pointer-tech--5.webp" alt="Two Pointer Technique" width="450">
   <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240930115146/two-pointer-tech--6.webp" alt="Two Pointer Technique" width="450">
</div>






