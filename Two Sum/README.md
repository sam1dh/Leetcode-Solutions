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
    <li>Space Complexity : O(n) </li>
  </ul>
<p>
  <h3>Steps to Solve:</h3>
</p>
<ul>
  <li>Generate all the possible pairs.</li>
  <li>Check the sum of each pair.</li>
  <li>Return the True if the pair that matches the target. Otherwise False.</li>
</ul>

<h1>Code :</h1>

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



