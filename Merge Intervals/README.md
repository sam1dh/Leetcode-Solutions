<h1> Merge Intervals :</h1>
Given an array of time intervals where <b>arr[i] = [start<sub>i</sub>, end<sub>i</sub>].</b>
<h1>Task :</h1>
Merge all the <B>overlapping intervals</B> into one and The result which should have only <b>Mutually Exclusive intervals</b>.
<h1> Example :</h1>

![example](carbon.png)
![example](https://www.interviewbit.com/blog/wp-content/uploads/2021/11/merge-overlapping-intervals-951x1024.png)

<h2> Steps to solve : </h2>
<ul>
  <ul>
    <li>First, Sort the intervals based on their starting points.</li>
       
   <img src="https://www.interviewbit.com/blog/wp-content/uploads/2021/11/contagious-fashion-1024x382.png" alt="example" width="450">
     <li><b>Disclaimer:</b></li>
     <li>If Intervals' starting positions have the same value, then sorting will be based on their ending points.</li>   
    <img src="Index.png" alt="example" width="450" height = "300">    
  </ul>
  <ul>
   <li>After Sorting , It will be easy to Merge intervals by comparing the end point of first interval and Start point of Second Interval </b>.</li>
   <img src="2.png" alt="example" width="450" height = "300">
    <li>  This allows us to easily identify overlapping intervals by comparing each interval with the last merged interval </li>
    <li> Now, Iterate over each interval and if the current interval overlaps with the last merged interval, then merge them both.</li>
    <img src="1.png" alt="example" width="450" height = "300">
    <li> Append the merged interval to the result.</li>
    <img src="Index (2).png" alt="example" width="450" height = "300">
  </ul>
Refernce Link : https://www.geeksforgeeks.org/merging-intervals/#expected-approach-checking-overlapping-intervals-only-onlogn-time-and-o1-space
</ul>
 <h1> Code :</h1>
 
``` cpp
vector<vector<int>> mergeOverlap(vector<vector<int>>& arr) {

    // Sort intervals based on start values
    sort(arr.begin(), arr.end());
  
    vector<vector<int>> res;
    res.push_back(arr[0]);

    for (int i = 1; i < arr.size(); i++) {
        vector<int>& last = res.back();
        vector<int>& curr = arr[i];

        // If current interval overlaps with the last merged
        // interval, merge them 
        if (curr[0] <= last[1])
        {
            last[1] = max(last[1], curr[1]);
        }
        else
        { 
            res.push_back(curr);
        }
    }

    return res;
}
 
````
  <h1>Merging Intervals Logic</h1>
    
   <h2>Given:</h2>
    <pre>
arr = [
    [1, 3],
    [4, 5],
    [6, 7],
    [8, 10]
]
    </pre>
    <h3>Interpretation:</h3>
    <ul>
        <li><code>arr[0][0] = 1</code>, <code>arr[0][1] = 3</code></li>
        <li><code>arr[1][0] = 4</code>, <code>arr[1][1] = 5</code></li>
        <li><code>arr[2][0] = 6</code>, <code>arr[2][1] = 7</code></li>
        <li><code>arr[3][0] = 8</code>, <code>arr[3][1] = 10</code></li>
    </ul>
    <p><code>arr.back()</code> will give the <strong>last element</strong> of the array.</p>
    
  <h2>Suppose:</h2>
    <pre>
res = [[1, 3]]
    </pre>
    <p>Here:</p>
    <ul>
        <li><code>res.back()</code> = <code>[1, 3]</code></li>
        <li><code>res.back()[1] == last[1]</code>, where <code>last = res.back()</code>, gives the <strong>second element</strong> of the last interval.
            <ul>
                <li><code>res.back()[1] = 3</code></li>
                <li><code>last[1] = 3</code></li>
            </ul>
        </li>
        <li><code>res.back()[0] == last[0]</code>, where <code>last = res.back()</code>, gives the <strong>first element</strong> of the last interval.
            <ul>
                <li><code>res.back()[0] = 1</code></li>
                <li><code>last[0] = 1</code></li>
            </ul>
        </li>
    </ul>
    
   <h2>Now, compare:</h2>
    <pre>
arr = [
    [1, 3], [4, 5], [6, 7], [8, 10]
]
    </pre>
    <p>For <code>i = 2</code>:</p>
    <ul>
        <li><code>arr[i][0] == curr[0]</code>: This gives the <strong>first element</strong> of the current interval.
            <ul>
                <li><code>arr[2][0] = 4</code></li>
                <li><code>curr[0] = 4</code></li>
            </ul>
        </li>
        <li><code>arr[i][1] == curr[1]</code>: This gives the <strong>second element</strong> of the current interval.
            <ul>
                <li><code>arr[2][1] = 5</code></li>
                <li><code>curr[1] = 5</code></li>
            </ul>
        </li>
    </ul>
    
  <h2>Compare <code>curr[0] <= last[1]</code>:</h2>
    <ul>
        <li>Example:
            <ul>
                <li><code>curr[0] = 4</code></li>
                <li><code>last[1] = 5</code></li>
                <li><code>4 <= 5</code> is <code>true</code>.</li>
            </ul>
        </li>
    </ul>
    
   <h2>If <code>true</code>:</h2>
    <p>Merge the intervals:</p>
     <p>Swap the end points of the result interval and current interval</p>
    <pre>
last[1] = max(last[1], curr[1]);
    </pre>  
   <h2>Otherwise:</h2>
    <p>Add the current interval to <code>res</code>:</p>
    <pre>
   res.push_back(curr);
    </pre>
    
  <h2>Example:</h2>
    <pre>
Input:
arr = [ [1, 3], [4, 5], [6, 7], [8, 10] ] 
res = [ [1, 3] ]      
Output:
res = [ [1, 3] , [4, 5] ]
This ouput for the Index 2 so you can iterte every interval and Get Result.
  </pre>
    
  <h2>Final Notes:</h2>
    <ol>
        <li>This explanation ensures clarity of the merging process and the role of <code>curr</code> and <code>last</code>.</li>

  </ol>

       
